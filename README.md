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

![Image 1](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/RF_2.png) 
![Image 2](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_3.png) 
![Image 3](https://github.com/aadhavjawahar-sys/Skin-classification-Random-Forest/blob/main/images/DF_4.png)

***
