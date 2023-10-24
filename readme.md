# DS 4002 Project 2

## Table of Contents
[SRC](#SRC)  - This section contains all the source code for our project, which includes scripts for the [pretrained model](https://github.com/githubharald/SimpleHTR). The main files are main.py and model.py in the folder. The main.py file helps to run the model on an image to output what the handwritten text states and the model.py file contains the code for the model building.

[DATASET](#Dataset)  - This section contains the IAM dataset which the model is trained on. 

[FIGURES](#Figures)  - This section contains all figures from our main analysis phase, as well as descriptions of their key takeaways.

[References](#References)  - This section contains all references that were used throughout the project, as well as links to the MI1 and MI2 Assignments.

## SRC

### Installing/Building Code
To install/build the code, VSCode and Python is required. Then, the scripts in the 'src', 'model', and 'data' folder are required to run the code. To run and test the model on an example image, cd into the 'src' directory and run 'python main.py --img_file ../data/line.png' in the terminal. 

Required libraries:
- cv2
- editdistance
- path
- tensorflow


### Usage of Code
The code can be used to replicate our deep-learning model or build upon it.

## DATASET

### Link to Dataset
[See file](https://fki.tic.heia-fr.ch/databases/iam-handwriting-database)

### Data Dictionary
| Column| Description|                   
|-------|------------|
| graylevel | graylevel to binarize the line containing the word in the dataset|
| bounding box | the bounding box around the word in x,y,w,h format | 
| grammatical tag | the grammatical tag for the word (noun, verb, adjective) | 
| transcription | the transcription for words in the dataset | 


## FIGURES

### Figures Table
| Column| Description |                   
|-------|------------|
| Figure 1 | Figure 1 displays the frequency of certain gray level values in the IAM dataset. Gray levels are used in image preprocessing to describe the grayscale values of individual pixels in an image. It reveals the pixel’s brightness or intensity. A gray level of 0 corresponds to a completely black pixel and a gray level of 255 corresponds to a white pixel. The EDA revealed that 182 was the most common gray level, followed by 170 and 160. This means that a significant number of pixels in the dataset are likely to be brighter or lighter gray in the images.|
| Figure 2 | We analyzed the sizes of the images in the folder 'a01-000u', which contains a full line of words from the greater a01 folder. The images have varying sizes, indicating that the words in each image are of different lengths, sizes, and shapes, adding to the diversity of the dataset. Additionally, although there are some images that are very small (close to 100), there are other images that are large (past 40,000 pixels), indicating that there is a large range of image sizes in this subfolder of the dataset.|
| Figure 3 | We analyzed the texture of all the images in the 'a01-000u' folder. We used the Mahotas library [4] to gain insight on the Haralick textural features we could derive across all 52 of these images in the folder. We found that the average sum variance was 25,000, which is very high, indicating that there is a great deal of diverse and varied textural patterns in this folder of the dataset.  The average sum of squares being at approximately 7,000 indicates that the images have textural patterns that have differing degrees of contrast, meaning that the gray-level pairs in the images have an increased amount of spread. |



## REFERENCES 
[1] "IAM Handwriting Database," fki, [Online]. Available: https://fki.tic.heia-fr.ch/databases/iam-handwriting-database. [Accessed: 08-Oct-2023]. 

[2] “Handwriting Recognition Guide,” v7labs, [Online]. Available: https://www.v7labs.com/blog/handwriting-recognition-guide#:~:text=Improved%20accessibility,blind%20and%20visually%20impaired%20individuals. [Accessed: 08-Oct-2023]. 

[3] "Train your image classifier model with PyTorch," Microsoft, [Online]. Available: https://learn.microsoft.com/en-us/windows/ai/windows-ml/tutorials/pytorch-train-model. [Accessed: 08-Oct-2023]. 

[4] “Mahotas: Computer Vision in Python,”mahotas.readthedocs.io, [Online]. Available:
https://mahotas.readthedocs.io/en/latest/features.html.
[Accessed: 15-Oct-2023]



### MI1 and MI2 Assignments
MI1 Assigment: [https://docs.google.com/document/d/15kF4ldljKkB7TauAzlaOjv6WxM9HJWvKzsEGZzX-_34/edit?usp=sharing](https://docs.google.com/document/d/15kF4ldljKkB7TauAzlaOjv6WxM9HJWvKzsEGZzX-_34/edit?usp=sharing)

MI2 Assignment: [https://docs.google.com/document/d/1gefyCpMglXhB2M0MZ3hF82AivXBM_BHLFKRwHv0fRO4/edit?usp=sharing](https://docs.google.com/document/d/1gefyCpMglXhB2M0MZ3hF82AivXBM_BHLFKRwHv0fRO4/edit?usp=sharing)



