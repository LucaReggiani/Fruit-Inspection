# Fruit-Inspection

This software system aims to locate defects and imperfections on fruits pictures took by Near Infra-Red (NIR) and color camera images. The system performs fruit segmentation and defect detection, russet detection, and kiwi inspection. This README file provides an overview of the project and instructions on how to use the software.

## Project Structure
Three tasks are processed:
 - task1.ipynb
 - task2.ipynb
 - task3.ipynb
 
## Task Instructions
### First Task: Fruit Segmentation and Defect Detection

In the Fruit_Inspection_Task_1 file, there are images of apples with clear external defects. To perform fruit segmentation and defect detection, these steps are followed:

    - Outline the fruit by generating a binary mask:
        Threshold the whole image to remove the background while preserving the fruit borders.
        Fill the holes inside the fruit blob using a flood-fill approach.
        Apply the generated mask to the corresponding NIR and color images.

    - Search for defects on each fruit:
        Extract edges using an edge extraction algorithm.
        Identify areas that exhibit a darker color compared to the neighboring areas of the fruit.

### Russet Detection (Second Task)

In the Fruit_Inspection_Task_2 file, there are images of apples with reddish-brown areas. To perform russet detection, these steps are followed:

    Identify the russet or part of it without false positive areas:
        Try using the Mahalanobis color distance to find a suitable threshold.
        Experiment with different color spaces such as HSV, HSL, and LUV.
        Mahalanobis distance doesn't provide sufficient results, it is used cv.findContours with area thresholding.

### Final Challenge: Kiwi Inspection

In the Fruit_Inspection_Task_3 file, there are images of kiwis. To perform kiwi segmentation and defect detection, these steps are followed:

    Segment the fruits:
        Apply suitable image processing techniques to segment the kiwis from the background.
        Remove the dirt on the conveyor and the sticker from the images.

    Locate the defect in image 000007:
        Analyze the segmented kiwis to identify the defect.
        Implement a suitable algorithm to locate the defect accurately.
 

## Usage

1. Clone the project repository:
git clone <repository-url>

2. Navigate to the project directory:
cd Fruit-Inspection

3. Open the Jupyter Notebook corresponding to the desired task:

jupyter notebook folder/task1.ipynb

Follow the instructions in each notebook to perform fruit segmentation, defect detection, russet detection, and kiwi inspection for each task.

## Conclusion

By following the instructions provided in the Jupyter Notebooks for each task, you can perform fruit segmentation, detect defects, identify russet areas, and inspect kiwis. Feel free to explore and modify the code in each notebook to enhance the system's capabilities.

Happy fruit defect detection!
