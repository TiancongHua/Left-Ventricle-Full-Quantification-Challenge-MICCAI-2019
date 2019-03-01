# Left-Ventricle-Full-Quantification-Challenge-MICCAI-2019

## Attention! This page is a temporary page for demonstrating challenge information, this chanllenge may start in early April, and the official  website will online in that time.

## Traning data release:
Baidu pan：https://pan.baidu.com/s/1K-tZCZc1t0utKzCrCl7VsQ 
password：ulsi 

## Challenge acronym: LVQuan19

## Challenge description:

This challenge is an extension of Left Ventricle Full Quantification Challenge MICCAI 2018 (LVQuan18), the main difference is that this challenge (LVQuan19) will provide original data without preprocessing for training and testing phases,which is more clinical than the data providing by LVQuan18. The challenge addresses the analysis of left ventricles (LV) in patients undergoing cardiac MRI.To assess the heart's function, the LV's function, morphology and temporal dynamics is of clinical interest. This analysis in clinical routine is time consuming and prone to error and inter-observer variability. In this challenge the extraction of the LV's cavity and myocardium and subsequently the regression of regional wall thicknesses, LV dimensions and the classification of the phase of the cardiac cycle are to be performed. These are common and significant parameters to assess the LV function. The aim of this challenge is to learn effective machine learning models that can estimate a set of clinical significant LV indices (regional wall thicknesses, cavity dimensions, area of cavity and myocardium, cardiac phase) directly from MR images. No intermediate segmentation is required in the whole procedure.


## Key expected outcome of the challenge:
  
  Learn effective machine learning models that can estimate a set of clinical significant LV indices (regional wall thicknesses, cavity dimensions, area of cavity and myocardium, cardiac phase) directly from MR images.
  
## Data Acquirement:

The DIG-Cardiac database consists of 56 cine-MRI images collected from 3 hospitals affiliated with two health care centers (London Healthcare Center and St. Josephs HealthCare). The subjects age from 16 yrs to 97 yrs, with average of 58.9 yrs. The pixel spacings of the MR images range from 0.6836 mm/pixel to 2.0833 mm/pixel, with mode of 1.5625 mm/pixel. Diverse pathologies are in presence including regional wall motion abnormalities, myocardial hypertrophy, mildly enlarged LV, atrial septal defect, LV dysfunction, etc. Each subject contains nF = 20 frames throughout a cardiac cycle. In each frame, LV is divided into equal thirds (basal, mid-cavity, and apical) perpendicular to the long axis of the heart following the standard AHA prescription and a representative mid-cavity slice is selected for this database.

## Ground truth:

Besides the epicardium and endocardium contour obtained through the above procedure, quantification results of LV are also provided, as shown in Figure 1. These quantifications include: areas of the myocardium and LV cavity, three directional LV cavity dimensions, six regional wall thicknesses, and one cardiac phase.
![image](https://github.com/TiancongHua/Left-Ventricle-Full-Quantification-Challenge-MICCAI-2019/blob/master/LVQuan19.png)
Figure 2. Demonstration of the cardiac indices considered in the database. (a) area of myocardium and LV 
cavity. (b) Three LV cavity dimension. (c) Regional wall thickness. (d) Cardiac phase.

## Training data description:

  Number of training cases: 56 2D SAX sequences with a total of 1120 images
  Characteristics of training cases:Pixel level segmentation of the myocardium and values of the LV indices
  (regional wall thickness, dimension, area, phase) for each image.
  Annotation policy for training cases:Delineation of the inner and outer boundary of myocardium for each frame of the
SAX sequences, with papillary muscle excluded.
  Annotators of training data: The inner and outer contours of myocardium were delineated by one experienced engineer in medical imaging and double checked by two cardiac radiologists with more than 10 years experiences.

## Test data description:
  600 images from 30 subjects(other details are similar to training data).

## Evaluation metrics:
Mean Absolute Error (MAE) for tasks of regional wall thicknesses, dimensions,and areas between estimated values and reference values.
Pearson Correlation Coefficient (PCC) for tasks of regional wall thicknesses,dimensions, and area between estimated values and reference values.
Error Rate (ER) for task of cardiac phase between the estimated values and the reference values.

If you want to know more details, please search the website and read the reference papers: https://lvquan18.github.io/.
## Reference:
[1]. Wufeng Xue, Gary Brahm, Sachin Pandey, Stephanie Leung, and Shuo Li. "Full left ventricle quantification via deep multitask relationships learning." Medical Image Analysis 43 (2018): 54-65.

[2]. Wufeng Xue, Andrea Lum, Ashley Mercado, Mark Landis, James Warrington, and Shuo Li. "Full Quantification of Left Ventricle via Deep Multitask Learning Network Respecting Intra-and Inter-Task Relatedness." MICCAI, 2017.

