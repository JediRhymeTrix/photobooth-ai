# PhotoBooth.ai

PhotoBooth.ai is a deep learning model that automatically detects when you're posing for a picture and takes a picture automatically at the best possible moment. The model can reliably predict any pose that a person would make when having a picture taken and can differentiate between normal body language and poses for pictures in real-time.

## Data Gathering

The first step in building the model is to gather data. We need images of people posing for pictures as well as images of people just standing around. We will use these images to train our model to recognize the difference between the two.

To gather the data, we use the `requests` library to send GET requests to Google Images and the `beautifulsoup4` library to parse the HTML response. We download the images and store them in a directory called "data", with subdirectories for each label ("pose" and "stand").

## Data Preprocessing

Before training the model, we need to preprocess the data. We use the `Pillow` library to resize all the images to a fixed size and convert them to grayscale. We then split the data into training and validation sets.

## Model Configuration

We use a convolutional neural network (CNN) to train our model. The CNN consists of several convolutional layers, max pooling layers, and fully connected layers. We use the `tensorflow` library to build and train the model.

## Model Execution

We train the model on the preprocessed data and evaluate its performance on the validation set. Once the model is trained, we can use it to make predictions in real-time. We use the `opencv-python` library to capture video frames from a webcam and apply the model to each frame to detect whether the person in the frame is posing for a picture or not. If the person is posing, we automatically take a picture at the best possible moment.

## Getting Started

To get started with the project, clone this repository to your local machine:

```bash
git clone https://github.com/your-username/photobooth-ai.git
```

Then install the required packages:

```bash
pip install -r requirements.txt
```

You can run the Jupyter notebook `photobooth-ai.ipynb` to see the code in action.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
