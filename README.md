# Vehicle Detection
Project Writeup

### Steps Taken To Complete the Project

We Used HOG-Features and Histogram features of the image to Identify the car in the image/video.So,we first analysed the image data(refer to data_explore)to identify the properties of the images in HOG channel and Histogram Channel.

#### WHY HOG -CHANNEL
Histogram of oriented gradients (HOG) is a feature descriptor used to **detect objects in computer visionand image processing**. The HOG descriptor technique counts occurrences of gradient orientation in localized portions of an image - detection window, or region of interest (ROI).
##### IMPLEMENTATION METHOD

Implementation of the HOG descriptor algorithm is as follows:-

- Divide the image into small connected regions called cells, and for each cell compute a histogram of gradient directions or edge orientations for the pixels within the cell.
- Discretize each cell into angular bins according to the gradient orientation.
- Each cell's pixel contributes weighted gradient to its corresponding angular bin.
- Groups of adjacent cells are considered as spatial regions called blocks. The grouping of cells into a block is the basis for grouping and normalization of histograms.
- Normalized group of histograms represents the block histogram. The set of these block histograms represents the descriptor.
##### HOG IMAGE
![](show/1.png)

**Code Description**

Function Created for fetching Hog feature in the code :-
**get_hog_features(image,oreintation,pixels per cell,cell per block,vis='True/False',feature_vector='True/False')**
argument details is as follow:


- image(image data extracted by using mpimg.imread)
- oreinetation(image oreintation)
- pixels per cell(no of pixels to be searched per cell)
- cell per block(no of cell to created per block to search for features)
- vis()
- feature_vector()


##### Step:-1:Loading Sample data sets to train classifier

The datasets were extracted form udacity datasets into the programme to train the classifier.
**Random Images Displayed From Datasets**
![](show/download.png)	

### Step 2:- Analysing Certain Features of the datasets
**HOG_Feature**
Exratacting Hog Features by calling hog_function

Similarly calling respective functions to Analyse Histogram and Spatial features of the image

### Step 3:- Creating Datasets of all the classified features to train the classifier
by using single_

###Step 4:-Using Sklearn library to train the classifier

###Step 5:- Using Window Sliding and Window Search Technique To Search and Perdict the images for car/non-cars using the classifier
###Step 6:-Drawing the boxes on the Predicted Images
###Step 7:-Using Heatmap function to make sure the image predicted is of a car

### Image Examples
**Step 6:Image Prediction Example**

![](show/2.png)

**Step 7:Heat Maps Image Example**

![](show/5.png)
![](show/6.png)



**Histogram Features image Graph**

![](show/3.png)

**Spatial Images**

![](show/4.png)


> test_results:- Test Video
> project_result:- Project Video