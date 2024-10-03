# ML dynamic pricing
TensorFlow model to implement dynamic pricing strategy

## Source
This based on the [Dynamic Pricing Dataset](https://www.kaggle.com/datasets/arashnic/dynamic-pricing-dataset).

## Setup
To run TensorFlow you need Linux OS. I recommend using Ubuntu or Debian. If you don't have a Linux PC you can install Ubuntu on Windows using WSL - just go to the Microsoft Store and search for Ubuntu. You should also be able to use Raspberry Pi with Raspberry Pi OS, but I haven't tested that.

### Install required tools
``` bash
sudo apt install python3 python3-pip python3-venv git
```

### Create Python virtual environment and activate it
``` bash
python3 -m venv mlpricing
source mlpricing/bin/activate
```

### Clone repository
``` bash
git clone https://github.com/szajakubiak/ml_dynamic_pricing.git
```

### Install requirements
``` bash
cd ml_dynamic_pricing
pip install -r requirements.txt
```

### Run Jupyter Lab
``` bash
jupyter lab --no-browser
```
You can skip *--no-browser* if you are using PC with Linux installed as a main OS. In such case web browser will be opened with Jupyter Lab tab. If you are on a virtual Linux machine it's better to start web browser on your main system (Windows in my case) and paste in the adress bar link which you will get in the terminal window starting with *localhost:8888/lab* or *127.0.0.1:8888/lab*. Remember to copy the full link with the access token.

## Input data transformations
There are several categorical properties in the dataset: *Location_Category*, *Customer_Loyalty_Status*, *Time_of_Booking*, and *Vehicle_Type*. Two types of encoding was used to convert them into numerical properties:

* label encoding was used when it was possible to set the values in logical order (*Customer_Loyalty_Status*, *Vehicle_Type*)
* one-hot encoding was used otherwise (*Location_Category*, *Time_of_Booking*)

Additionaly new property was created by calculating the difference between *Number_of_Drivers* and *Number_of_Riders*.

In all cases original categories were excluded.

## Training ML model

### Data split

### Model structure

### Output analysis

## Links
[TensFlow guide](https://www.tensorflow.org/guide)
