# Common-issues-and-their-solutions
Common problems that I run into and how to solve them


If tensorflow doesn’t work on Jupiter notebook (kernel appears to have died…)


import os
os.environ['KMP_DUPLICATE_LIB_OK']='True'


To cd to thumbdrive:
cd /Volumes && ls
Then cd to thumb drive name
jupyter notebook to launch 


Load and convert images in tensor flow:
from tensorflow.keras.preprocessing.image import load_img
from tensorflow.keras.preprocessing.image import img_to_array
from tensorflow.keras.applications.vgg16 import preprocess_input
from tensorflow.keras.applications.vgg16 import decode_predictions

image = load_img('/Users/tengyaolong/Desktop/download-2.jpg')
image = img_to_array(image)  #output Numpy-array

image = image.reshape((1, image.shape[0], image.shape[1], image.shape[2]))

image = preprocess_input(image)
yhat = base_model.predict(image)

label = decode_predictions(yhat)
print(label)

If glove_model doesn’t work need to add vocal length and dimension of vector in first line of text file

When running java program via CLI with package
E.g.
(base) tengyaolong@Tengs-MacBook-Pro Coffee % cd /Users/tengyaolong/Desktop/IntelliJava/out/production/IntelliJava
(base) tengyaolong@Tengs-MacBook-Pro IntelliJava % java com.company.Main
