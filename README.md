# Real-time-fire-detection-using-AI



<img src="https://user-images.githubusercontent.com/58718316/171399443-3b2a3aa3-f516-4402-81cd-d4afd4511960.jpg" width="800" height="500">

# Creating the customized CNN architecture
We are going to use TensorFlow API Keras for building our model. Let’s first create our ImageDataGenerator for labeling our data. [1] and [2] datasets are used here for training. Finally, we will have 980 images for training and 239 images for validation. We are going to use data augmentation as well.

<img src=https://user-images.githubusercontent.com/58718316/171979003-a32d5ca1-a7ef-49f8-816a-4eef628d7dba.PNG>



In the above code, 3 data augmentation techniques are applied — horizontal flipping, rotation, and height shifting.

Now, we will create our CNN model. The model contains three Conv2D-MaxPooling2D layers pairs followed by 3 Dense layers. To overcome the problem of overfitting we will also add dropout layers. The last layer is the softmax layer which will give us the probability distribution for both the classes — Fire and Nonfire. One can also use ‘sigmoid’ activation function at the last layer by changing the number of classes to 1.


<img src=https://user-images.githubusercontent.com/58718316/171979018-7a404185-c51f-4595-b51f-8530dab5cf87.PNG>


We will use Adam as an optimizer with a learning rate of 0.0001. After training for 50 epochs, we get the training accuracy of 96.83 and validation accuracy of 94.98. The training and validation loss is 0.09 and 0.13 respectively.


<img src=https://user-images.githubusercontent.com/58718316/171979038-e8dd45ce-fc37-4a6b-ac6c-4410109e5698.PNG>


<img src="https://user-images.githubusercontent.com/58718316/172055748-c95d5693-39ff-48b2-83de-d92a05e03eac.jpg">








