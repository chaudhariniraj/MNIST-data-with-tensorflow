# MNIST-data-with-tensorflow
small operations on MNIST data
#install tensorflow

!pip install tensorflow==2.0.0-beta-1
import tensorflow as tf

mnist=tf.keras.datasets.mnist
(x_train,y_train),(x_test,y_test)=mnist.load_data()

#check feature of tensor#
print('atrribute of x_train')
print('diamension=%d'%x_train.ndim)
print('shape:',x_train.shape)
print('datatype:',x_train.dtype)

print('atrribute of x_test')
print('diamension=%d'%x_test.ndim)
print('shape:',x_test.shape)
print('datatype:',x_test.dtype)

#print the data 
x1_train=x_train[10]
import matplotlib.pyplot as plt
def display_img(img):
  plt.imshow(img,cmap=plt.cm.binary)
  plt.show()
display_img(x1_train)

#print no. of data

for i in range(10):
  x_i=x_train[i]
  display_img(x_i)
  
  
  
  #data slicing
  x_train_slice=x_train[10:100]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)


x_train_slice=x_train[10:100, :,:]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)

#slicing bottom right 14*14
x_train_slice=x_train[:,14:,14:]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)



[ ]
!pip install tensorflow==2.0.0-beta-1
import tensorflow as tf


[ ]
mnist=tf.keras.datasets.mnist
(x_train,y_train),(x_test,y_test)=mnist.load_data()


[ ]
print('atrribute of x_train')
print('diamension=%d'%x_train.ndim)
print('shape:',x_train.shape)
print('datatype:',x_train.dtype)


[ ]
print('atrribute of y_train')
print('diamension=%d'%y_train.ndim)
print('shape:',y_train.shape)
print('datatype:',y_train.dtype)


[ ]
print('atrribute of x_test')
print('diamension=%d'%x_test.ndim)
print('shape:',x_test.shape)
print('datatype:',x_test.dtype)


[ ]
print('atrribute of y_test')
print('diamension=%d'%y_test.ndim)
print('shape:',y_test.shape)
print('datatype:',y_test.dtype)

[ ]
x1_train=x_train[10]
import matplotlib.pyplot as plt
def display_img(img):
  plt.imshow(img,cmap=plt.cm.binary)
  plt.show()
display_img(x1_train)



[ ]

for i in range(10):
  x_i=x_train[i]
  display_img(x_i)



[ ]
x_train_slice=x_train[10:100]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)


[ ]
x_train_slice=x_train[10:100, :,:]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)


[ ]
x_train_slice=x_train[10:100,:28,:28]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)

bottom right 14*14

[ ]
x_train_slice=x_train[:,14:,14:]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
print('data type',x_train_slice.dtype)


[ ]
x_train_slice=x_train[:,7:21,7:21]
print('diamension',x_train_slice.ndim)
print('shape',x_train_slice.shape)
3print('data type',x_train_slice.dtype)
'''
data batches
we usually break the data in the batches and we are process on that

-the first axis in the all data sensors is sample axisor sample dimension.

-the first axis of batch sensors is called batch axis or batch dimension
'''
#batch of 128 
x_train_batch=x_train[:128]
print('diamension',x_train_batch.ndim)
print('shape',x_train_batch.shape)
print('data type',x_train_batch.dtype)

#batch of 128 
x_train_batch=x_train[128:256]
print('diamension',x_train_batch.ndim)
print('shape',x_train_batch.shape)
print('data type',x_train_batch.dtype)





