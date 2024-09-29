# ML dynamic pricing
TensorFlow model to implement dynamic pricing strategy

## Source
This based on the [Dynamic Pricing Dataset](https://www.kaggle.com/datasets/arashnic/dynamic-pricing-dataset).

## Input data transformations
There are several categorical properties in the dataset: *Location_Category*, *Customer_Loyalty_Status*, *Time_of_Booking*, and *Vehicle_Type*. Two types of encoding was used to convert them into numerical properties:

* label encoding was used when it was possible to set the values in logical order (*Customer_Loyalty_Status*, *Vehicle_Type*)
* one-hot encoding was used otherwise (*Location_Category*, *Time_of_Booking*)

Additionaly new property was created by calculating the difference between *Number_of_Drivers* and *Number_of_Riders*.

In all cases original categories were excluded.
