
# Text Detector

Font identification system capable of recognizing diverse font styles. By blending CNN-based deep learning with the OCR capabilities of Tesseract, we aimed to develop a comprehensive solution for font identification in images.


## Screenshots
Scanning text such that around each word, a bounding box is made 
![image](/home/adi_techbuddy/Desktop/dc_proj/repo/DocumentTranslation/image_detector/word_5.png)

And then, using our pre-trained model, it will be able to detect the font around each word  
![image](https://github.com/adityarathor007/Story/assets/120591213/1d67b0da-4e5f-47f0-8152-e6c8a9dcbf74)
![image](https://github.com/adityarathor007/Story/assets/120591213/4b0aaf93-9857-473e-82db-884ea989ce9d)



# DOCUMENT TRANSLATION


The aim of this project is to develop a system capable of recognizing text formatting styles in pdf documents using its LaTeX formatting and while preserving those formats to convert to other language 


## TRAIN

After converting pdfs to image extracted cnn features of each word and given label from latex script for font style and font size

And trained a svm and random forest classifier for font style prediction and regression model for font size on 8k pdf generated synthetically using random words kept in latex script and then converted to pdfs


## PIPELINE

First converted pdf to image then,

Now again extraction of features and predicting font size and style and creating a new image with those specfication and with the help of google trans translated each word into different language and placed them at the same position using bounding box