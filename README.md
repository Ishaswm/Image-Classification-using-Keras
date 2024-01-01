# Image-Classification

## Description
A set of flower photos provided by TensorFlow as an example. TensorFlow often includes example datasets for educational and demonstration purposes.
Downloaded through link: https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz 

## Dataset
Dataset contains of 3,670 total images. The images are divided into five classes: Sunflower, Tulips, Roses, Dandelions, Daisy with approximately 700 images for each.

The image_batch represents a tensor with a size of (32, 180, 180, 3). It contains 32 images, each measuring 180x180 pixels with three color channels (Red, Green, Blue).

## Model
The Keras Sequential model is composed of three sets of convolution blocks (tf.keras.layers.Conv2D) , each followed by a max pooling layer (tf.keras.layers.MaxPooling2D) . Additionally, there is a fully-connected layer (tf.keras.layers.Dense) with 128 units at the top, which is activated using the ReLU activation function ('relu'). It's important to note that this model hasn't been fine-tuned for achieving the highest accuracy. 

### Compile the model
For this model, we choose the tf.keras.optimizers.Adam optimizer and tf.keras.losses.SparseCategoricalCrossentropy loss function. 

We aaply **data augmentation** using the following Keras preprocessing layers: tf.keras.layers.RandomFlip, tf.keras.layers.RandomRotation, and tf.keras.layers.RandomZoom.

## Result


<img width="647" alt="Screenshot 2024-01-02 001338" src="https://github.com/Ishaswm/Image-Classification/assets/122556303/13a82d52-ec31-4c02-bb34-824515caa85f">

## Notes
Using packages
Keras (tensorflow.python.keras) for building models

OpenCV (cv2) for processing images

sikit-learn (sklearn) for train_test_split 
