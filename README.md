# Skin Classification Random Forest model

What do you think of when you hear the term "RGB"? Most think red, green, blue, and leave it at that. But, for anybody who've dabbled in the field of computer science, it brings to mind hexadecimal numbers (0-255 or 00-FF) representing every shade, distinction, and hue of color.

![Interesting RGB selector](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/RF_1.png)

Shifting topic, people's skin colors also have a wide array of vibrant shades. So, I decided to make a **random forest model** that takes in a specified color and outputs whether or not it can be classified as a shade/color of skin or not.

> According to [IBM](https://www.ibm.com/think/topics/random-forest), a Random Forest is "a commonly-used machine learning algorithm, trademarked by Leo Breiman and Adele Cutler, that combines the output of multiple decision trees to reach a single result. Its ease of use and flexibility have fueled its adoption, as it handles both classification and regression problems."

## Data Acquisition and Formatting

While browsing UCI's datasets, I found an interesting one on [Skin Segmentation](https://archive.ics.uci.edu/dataset/229/skin+segmentation) which has 3 features representing the intensity of each color...
- R: An integer from 0-255
- G: An integer from 0-255
- B: An integer from 0-255
and the target variable is whether or not it matches the color of skin
- y: 1 (Skin), 2 (non-Skin)
> Reverted to 0 (Skin) and 1 (non-Skin) to match binary

It has nearly 250,000 datapoints that I split in a 80/20 split for my training and testing datasets respectively.

### Format

For formatting the provided text file, I wrote a bit of code to make it similar to a .csv file.

**Original**

![Image 1](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/RF_2.png) 

*Code*

![Image 2](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_3.png) 

**Datafile**

![Image 3](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_4.png)

***

## Hyper-parameter Tuning

When creating my Random Forest model, I manipulated 3-main hyper-parameters.
- max_depth: Number of questions the model asks before reaching a conclusion
- max_features: Max number of features per Decision Tree model in the forest
- n_estimators: Number of Decision Tree Models in the Random Forest

![Image 4](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_5.png)

***
## Model Accuracy

The accuracy of the skin-identification model was near perfect on the first stage of testing, at about 0.99 for testing. To I adjusted the testing data from its original 75/25 to an 80/20 split to improve its accuracy. Now, it is nearly perfect in its identification.

![Image 5](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_6.png)

## How to interact with the model

To interact with my Random Forest classification model, I made a simple UI with the help of the [gradio](https://gradio.app/) module.

1. Select appropriate RGB colors in the 3 selectors.
2. Click Submit
![Image of the RGB selector](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_7.png)  
3. Look at the output box to determine whether it can be classified as a skin color.
![Skin or not skin? That is the question.](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_8.png)

## Future direction

As a whole, I have no future aspirations or additions to this project as it has a relatively perfect accuracy for the training and testing data, making it a wonderful way to classify skin color. Though, I am open to suggestions from others about how I can improve this project. Thanks for your time!



