UC Boulder MSDS course work <br>
DTSA 5511 Deep Learning <br>

## Mini-Project <br> Histopathologic Cancer Detection

This [notebook](https://github.com/elfchildRichter/Histopathologic_Cancer_Detection) utilizes CNNs for histopathologic cancer detection. 

The data sourced from [Kaggle](https://www.kaggle.com/competitions/histopathologic-cancer-detection), consists of a training set with 220,025 tumor tissue images, each 96x96 px, and a test set comprising 57,458 images. 

<br>

## Summary

| Model               | Private Score    | Public Score     |
|---------------------|------------------|------------------|
| simple_cnn        | 0.8397           | 0.9118           |
| cnn_with_dropout  | 0.8944           | 0.9290           |
| cnn_with_bn       | 0.8623           | 0.9065           |
| resnet_cnn        | 0.8849           | 0.9115           |
| modified_resnet   | 0.8731           | 0.9453           |
| cnn_dropout_tuned   | 0.9179           | 0.9401           |

<br>

- The models exhibit a lower performance on the private scores compared to the public scores, which may indicate that the models are overfitting the training data and not generalizing well to unseen data.

- The simple cnn model shows a good performance on the public score, but there is a significant drop when compared to the private score. After the introduction of dropout or batch normalization, an improvement in private score can be observed. The ResNet model shows a good overall performance, and the modified ResNet with regularization achieves a public score of 0.9453. The tuned cnn model with dropout obtains a private score of 0.9179 and a public score of 0.9401.

<br>

## Directions for Improvement

- Increase training data diversity through data augmentation. 

- Use cross-validation to more reliably evaluate model generalization.

- Conduct a broader hyperparameter search to find the most optimized model configuration.

- Adjust the model's complexity to ensure the model is neither overfitting nor underfitting.

- Combine predictions from multiple models to increase performance and stability.
