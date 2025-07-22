Confusion matrix

|                        | Actual Positive    | Actual Negative    |
| ---------------------- | ------------------ | ------------------ |
| **Predicted Positive** | True Positive(TP)  | False Positive(FP) |
| **Predicted Negative** | False Negative(FN) | True Negative(TN)  |

First there is True/False, if we have given or not the correct output
Then there is Positive/Negative, this is what we have predicted
True Positive -> Prediction true and it's right
True Negative -> Prediction false and it's right
False Positive -> Prediction true and it's wrong
False Negative -> Prediction false and it's wrong


**Accuracy** is correct predictions over all predictions:
A=(TP+TN)/(FP+FN+TP+TN)

**Precision** proportion of all the model's positive classifications that are actually positive
P=(TP)/(TP+FP)

**Recall** portion of all actual positives there where classified correctly as positives
R=(TP)/(TP+FN)

**F-Score** is the harmonic mean of precision and recall (like parallel resistor times 2)
F-Score = 2*(P*R)/(P+R)