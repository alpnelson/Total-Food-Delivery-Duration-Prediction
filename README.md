# Total-Food-Delivery-Duration-Prediction
Prediction of food delivery duration
Just like any machine learning model, the metric for evaluation it is of utmost importance. During the
initial phase model of building, the mean absolute error (MAE) was used. A major drawback of MAE
for this particular problem is its symmetric nature, i.e., assuming the actual delivery duration is 5 minutes, MAE penalizes a prediction of 4 minutes equally as it would penalize a prediction of 6 minutes.
This makes the MAE (and other similar symmetric loss functions) not suitable for evaluating models
for the problem since the cost of under-prediction is more than that of over-prediction. This function
can updated to account for penalizing too late/early deliveries more than slightly late/early deliveries.
A custom loss function( custom mae ) that takes into consideration the preference of overprediction to under-prediction was developed. After developing and evaluating three models namely:
Random Forest, XGBoost, and Simple Linear Regression models, the Random Forest model performs
the best, in both cases of employing the traditional MAE as well as the custom cost function. With
an MAE of 228 on the validation data-set and 697 on the training data-set, the Random Forest model
was selected. This implies that on the training data, there is an absolute deviation of 228 seconds in
delivery time on average, whereas the average absolute deviation in delivery time on the validation
data is 697 seconds. Further analysis on the validation dataset shows that, for late deliveries, the
