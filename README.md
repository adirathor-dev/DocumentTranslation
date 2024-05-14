
# Text Detector

Font identification system capable of recognizing diverse font styles. By blending CNN-based deep learning with the OCR capabilities of Tesseract, we aimed to develop a comprehensive solution for font identification in images.


## Screenshots
Scanning text such that around each word, a bounding box is made 
![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/image_detector/test5.jpg_with_boxes.jpg?raw=true)

And then, using our pre-trained model, it will be able to detect the font around each word  
![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/image_detector/word_4out.png?raw=true)
![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/image_detector/word_7out.png?raw=true)



# DOCUMENT TRANSLATION


The aim of this project is to develop a system capable of recognizing text formatting styles in pdf documents using its LaTeX formatting and while preserving those formats to convert to other language 


## TRAIN

After converting pdfs to image extracted cnn features of each word and given label from latex script for font style and font size

And trained a svm and random forest classifier for font style prediction and regression model for font size on 8k pdf generated synthetically using random words kept in latex script and then converted to pdfs


## PIPELINE

First converted pdf to image then,

Now again extraction of features and predicting font size and style and creating a new image with those specfication and with the help of google trans translated each word into different language and placed them at the same position using bounding box.

The challenge was to bring uniformity in position (moving up and down) and lines with the same paragraph and was solved by chossing the y_corrdinate of the bounding box of starting word for each word in the line and for font for each line starting word label was checked  :


- actual image from pdf:


- without uniformity:


- with uniformity:



- Example 1:
    - original doc converted to image:
        ![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/eg1/eg1_page_1.png?raw=true)

    - Bounding boxes with fonts:
        ![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/eg1/eg1_witharr.jpg?raw=true)


    - Creating new image with background entact and words translated to other language in the image:
        - in hindi: 
        ![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/eg1/test_f2_hin.png?raw=true)
        - in french: 
        ![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/eg1/test_f2_fr.png?raw=true)
        - in dutch:
        ![image](https://github.com/adirathor-dev/DocumentTranslation/blob/main/eg1/test_f2_dutch.png?raw=true)

