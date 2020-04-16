#AMAP Docs
AMAP - Advanced Manuscript Analysis Portal - is a software tool to aid the study of manuscripts. This documentation should be helpful in guiding you through the onboarding process, app navigation, and functinality.

```
Table of contents
0. Introduction
1. Getting started

2. Main Menu
3. Functionality (Action Chips)
4. Image View Settings (Plugs)
5. Advanced Topics
```



## 0. Introduction
AMAP is a platform-independent tool that includes a toolbox of document image analysis (DIA) functions. By providing a graphical user interface (GUI), it aims to make elements of traditional programming available to everyone without having to learn an actual programming language. Instead, AMAP uses ***Visual Programming*** to allow its users to generate and combine blocks to build their own image processing solutions. 

AMAP is a joint effort by the Image Processing Department of the University of Hamburg and is partly funded by the DFG (German research association) and SFB (Department of special studies). It is an open-source project.



## 1. Getting started
AMAP Version 2.0 is currently available under https://bv.informatik.uni-hamburg.de/amap and can be used online provided that you have a stable internet connection. This Chapter will help you create your first workspace.


### 1.1 Loading an image
Our first goal is to load some data into the **central workspace** of AMAP where you will perform your DIA tasks. 

To load your image, click the "+" icon on the **main menu** located at the top. Browse and select an image from your computer to upload it. 

> Your image should be in a JPG format for all functions to work properly. To check what image format your image is, upload the image and double click it to flip it over. Check to confirm whether the file name ends in .jpg, jpeg, .JPG, or JPEG.


### 1.2 Action chips
With your image in the workspace, we are all set up to perform some DIA. The "functions menu" on the right contains the respective functions for image processing, whereas the "image settings menu" at the bottom allows for temporal image view settings (see 1.4).

Functions in AMAP are provided as so-called **action chips** which you can generate by double-clicking on an item in one of the dropdowns of the functions menu.

A corresponding action chip will be generated that you can attach to your image to perform its corresponding function. Many blocks allow for  adjustable parameters settings which you can toggle by clicking the gear icon. For instance, the Binarization block at the very top of the functions menu lets you adjust a threshold with a circular slider.

A preview will always show what an image looks like after some function has been performed. You can also detach a chip by double clicking on it.


### 1.3 Chaining action chips
You can also chain compatible action chips which will connect automatically. Incompatible blocks will repel each other. The image preview will now show the state of the imput image after it has gone through the functions of the blocks in the exact order in which you have chained the chips. Hence the block farthest away from the input will reflect the result after passing through all action chips.

Detaching a block here will "split" your chain left of the block which you have clicked.

### 1.4 Plugs
Plugs apply filters that change the appearance of the image / chip that it is attached to ***temporally*** and will not result in any changes reflected in the final result, unlike action chips.


### 1.5 Deleting blocks
To delete a block, activate the trash can at the bottom right by double clicking on it. Now drag-&-drop the block you would like to delete.

> Don't forget to deactivate the trash can after you are done deleting to avoid accidentally dragging and deleting blocks.


### 1.6 Saving your data
You can either export your image processing results or save your workspace to continue your task later. 

To export your results, right-click on the block and select export.

To save your workspace, press the 2nd icon on the main menu. To load your workspace afterwards, press the 3rd icon of the main menu and select your workspace.


## 1.7 How to proceed
You have now been onboarded to the most basic functionality of AMAP. Please refer to Chapters 2-4 for detailed explanations and documentation. Chapter 5 elaborates on Advanced topics such how to work with image stacks (batch operation) and using tools to create an efficient workflow.



## 2. Main Menu
This chapter explains the Main Menu, helping you understand and navigate through the app. 


### 2.1 File operations
The basic file operations are basically what we have already seen in Chapter 1. You can load an image (1), save your workspace (2), and load that workspace (3).

### 2.1.1 Image stack
You can also load multiple images while browsing through your computer. This will load a stack of images rhat you can unstack and stack again as you like.


### 2.2 Ruler, Protractor
You can use geographic tools such as a ruler (4) and a protractor (5) that will be loaded into the workspace.

The ruler has two draggable dots connected by a straight line. The line's length is displayed in pixels and changes according to how you move the dots.

The protractor consists of three dots. The middle dot, which is connected to the other two dots by sa traight line each, displays the angle in degrees the two lines shape at this dot. All dots can be dragged.


### 2.3 Selection rectangle
This tool lets you select a rectangular subregion or region of interest (ROI) within some image. You can apply this tool at any "stage" of your image processing where you have an image preview. All subsequent chips will be apply their functions on the ROI you have selected.


### 2.4 Toggable objects
You can toggle the visibility of all objects (6), or toggle the visibilility of some elements.

Toggle lines (8) lets you toggle the lines.

Hide image icons (11) will hide the image icons of blocks when you don't need them.


## 2.5 Information display
There are also some information diplay menus.

The logs (9) will toggle a history of action you have done on the left side. You can see all the details regarding what function with what parameters you have used, and when you did it. 

Show scale and tilt (10) displays the scale of an image relative to its original size and its tilt (rotation) in degrees.



## 3 Functionality (Action chips)
Here we will inspect the functionality and parameters of the action chips (right menu) in detail. Some more general image settings provided as plugs (bottom menu) will be explained in Chapter 4.


### 3.1 Binarization
Type: Image Processing
Input: Image
Output: Image
Parameters: Threshold (range 0 - 255)
Functionality: Image binarization maps all image pixel values of the input image to a binary range of 0 (black pixels) and 1 (white pixels). The threshold defines the lower bound at which a value of 1 should be assigned. Binarization takes the mean of all RGB colour channels.


### 3.2 Histogram Eq Color
Type: Image Processing
Input: Image
Output: Image
Parameters: None
Functionality: It does something to enhance the image.


### 3.3.1 NonLocal Denoising
Type: Image Processing
Input: Image
Output: Image
Parameters: filter_strength, template, filter_strength_color, search
Functionality: It removes noise.

### 3.3.2 Add Random Noise
Type: Image Processing
Input: Image
Output: Image
Parameters: type(gaussian), mean, std
Functionality: Adds random noise.


### 3.3.1 Blur
Type: Image Processing
Input: Image
Output: Image
Parameters: mean, std
Functionality: Blurs the image.

### 3.3.2 Gaussian Blur
Type: Image Processing
Input: Image
Output: Image
Parameters: mean, std
Functionality: Blurs the image.

### 3.3.3 Median Blur
Type: Image Processing
Input: Image
Output: Image
Parameters: mean, std
Functionality: Blurs the image.

### 3.3.4 Bilateral Filter
Type: Image Processing
Input: Image
Output: Image
Parameters: 
Functionality:


### 3.4.1 Canny
Type: Feature Detection
Input: Image
Output: Image with features
Parameters:
Functionality: Detects features

### 3.4.2 Good Features to Tra
Type: Feature Detection
Input: Image
Output: Image with features
Parameters:
Functionality: Detects features

### 3.4.3 ORB keypoints
Type: Feature Detection
Input: Image
Output: Image with features
Parameters:
Functionality: Detects features


### 3.5.1 Hough Line
Type: Morphology
Input: Image
Output: Image with stuctural lines
Parameters: 
Functionality: Adds geometric structures to the image.

### 3.5.2 Hough Line Prob
Type: Morphology
Input: Image
Output: Image with stuctural lines
Parameters: 
Functionality: Adds geometric structures to the image.

### 3.5.3 Skeletonize
Type: Morphology
Input: Image
Output: Image with stuctural lines
Parameters: 
Functionality: Adds geometric structures to the image.

### 3.5.4 Thin
Type: Morphology
Input: Image
Output: Image with stuctural lines
Parameters: 
Functionality: Adds geometric structures to the image.

### 3.5.5 Medial Arts
Type: Morphology
Input: Image
Output: Image with stuctural lines
Parameters: 
Functionality: Adds geometric structures to the image.


### 3.6.1 Tesseract Lines
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.

### 3.6.2 Tesseract Characters
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.

### 3.6.3 Histogram Lines
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.

### 3.6.4 Kraken Lines
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.

### 3.6.5 TopBase Lines
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.

### 3.6.6 MidInter Lines
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.

### 3.6.7 All Lines
Type: Layout Analysis
Input: Image
Output: Image with layout structure
Parameters:
Functionality: Detects the layout of the image.


### 3.7.1 Copy
Type: Propagate actions
Input: Chain of blocks
Output: Chain of blocks
Parameters: None
Functionality: Copies the chain of blocks that it is attached to

### 3.7.2
Type: Propagate actions
Input: Chain of blocks
Output: Result of compilation
Parameters: none
Functionality: Compiles the chain of blocks it is attached to.


### 3.8.1 Skeletonize
Type: Contours
Input: Image
Output: Image with structure
Parameters:
Functionality: Adds a skeleton to the input.

### 3.8.2 Contour
Type: Contours
Input: Image
Output: Image with contours
Parameters:
Functionality: Adds a contour to the input.


### 3.9 Word Spot.
Type: Recognition
Input: Image
Output: Image with ROIs of guessed word entities
Parameters:
Functionality: Highlights areas where the algorithm detects possible candidates for words.


### 3.10 Writer Identification
Type: Classification
Input: Image
Output: Class
Parameters:
Functionality: Tries to identify the scribe of a manuscript.


#### 3.11.1 Manual text
Type: Transcription
Input: Image
Output: Text
Parameters:
Functionality: Lets you label the image with texts you write yourself.

### 3.11.12 OCR text
Type: Transcription
Input: Image
Output: Text
Parameters:
Functionality: Lets you label the image with texts that an algorithm detects.



## 4 Image View Settings (Plugs)
Image View Settings can be found on the bottom menu and can be attached from below to the input chips connected to it. They are simple in that they only adjust one parameter each. They are temporal as they will not apply any actual changes to the exported result.


### 4.1 Brightness
Range: 0% - 400%
Default: 100%
This setting adjusts the brightness according to the value that you set in the slider. Higher values add "whiteness" to the image.


### 4.2 Contrast
Range: 0% - 400%
Default: 100%
This setting adjusts the contrast of your image. Higher values mean that the image pixel values will be pushed to the extremes. I. e., relatively darker pixels will become darker, and relatively brighter pixels will become brighter. Lower contrast values will minimize the difference of the pixel values of darker and brighter pixels.


### 4.3 Grayscale
Range: 0% - 100%
Default: 50%
This setting maps the colour channels of an image to a grayscale channel. The parameter sets the percentage of the grayscale channel. Towards 0%, the input is retained completely, while at 100% the input is completely grayscale.


### 4.4 Invert Colours
Range: 0% - 100%
Default: 50%
This setting maps the colours of the input to their complementary colours with regard to the colour channel(s). For example, a pixel with RGB (100, 200, 0) will be mapped to RGB (155, 55, 255), as the range of each colour channel lies within [0. 255].

At 0%, the input is retained fully, while at 100%, all image pixel values are fully inverted.


### 4.5 Opacity
Range: 0% - 100%
Default: 50%
This setting adjusts the transparency of an image. At 100%, the image is fully visible, while at 0%, the image is invisible.


### 4.6 Hue-Rotate
Range: 0deg - 359deg
Default: 0deg
I have no idea what this thing does.



## 5 Advanced
This chapter deals with some more advanced topics.


### 5.1 Stacking images


### 5.2 Workflows


### 5.3 Fine-tuning


3:37