#### Question1 : What does a neuron compute?
1.A neuron computes an activation function followed by a linear function (z = Wx + b)\
2.A neuron computes a function g that scales the input x linearly (Wx + b)\
3.A neuron computes a linear function (z = Wx + b) followed by an activation function\
4.A neuron computes the mean of all features before applying the output to an activation function\
ans:
#### Question2 : Which of these is the "Logistic Loss"?
1.L(i)(y^(i),y(i))=∣y(i)−y^(i)∣\
2.L(i)(y^(i),y(i))=−(y(i)log(y^(i))+(1−y(i))log(1−y^(i)))\
3.L(i)(y^(i),y(i))=∣y(i)−y^(i)∣2\
4.L(i)(y^(i),y(i))=max(0,y(i)−y^(i))\
ans:
#### Question3 : Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector?
1.x = img.reshape((3,32*32))\
2.x = img.reshape((1,32*32,*3))\
3.x = img.reshape((32*32*3,1))\
4.x = img.reshape((32*32,3))\
ans : 
#### Question4 : Consider the two following random arrays "a" and "b":
a.shape = (2, 3)\
b.shape = (2, 1)\
a = np.random.randn(2, 3)\
b = np.random.randn(2, 3)\
c = a + b
#### What will be the shape of "c"?
1. c.shape = (2, 3)
2. c.shape = (2, 1)
3. c.shape = (3, 2)
4. The computation cannot happen because the sizes don't match. It's going to be "Error"!
ans :
#### Question5 : Consider the two following random arrays "a" and "b":
##### a.shape = (4, 3)
##### b.shape = (3,2)
a = np.random.randn(4, 3)\
b = np.random.randn(3, 2)\
c = a*b
#### What will be the shape of "c"?
1. The computation cannot happen because the sizes don't match. It's going to be "Error"!
2. c.shape = (4, 3)
3. c.shape = (4,2)
4. c.shape = (3, 3)
ans : 
#### Question6: Suppose you have n_xn input features per example. Recall that X = [x^{(1)} x^{(2)} ... x^{(m)}]X=[x (1) x (2)...x (m)]. What is the dimension of X?
1.(m,nx) </br>
2.(m,1)</br>
3.(1,m)
4.(nx, m)
ans : 
#### Question7 : Recall that "np.dot(a,b)" performs a matrix multiplication on a and b, whereas "a*b" performs an element-wise multiplication.
#### Consider the two following random arrays "a" and "b":

a = np.random.randn(12288, 150)</br>
b = np.random.randn(150, 45)</br>
c = np.dot(a,b)</br>
What is the shape of c?
1. c.shape = (12288, 45)
2. c.shape = (150,150)
3. The computation cannot happen because the sizes don't match. It's going to be "Error"!
4. c.shape = (12288, 150)
ans : 
#### Question8 : Consider the following code snippet:
a.shape = (3,4)
b.shape = (4,1)
for i in range(3):\
  for j in range(4):\
    c[i][j] = a[i][j] + b[j]
#### How do you vectorize this?
1. c = a.T + b.T
2. c = a.T + b
3. c = a + b
4. c = a + b.T </br>
ans : 
#### Question9 : Consider the following code:
a = np.random.randn(3, 3) </br>
b = np.random.randn(3, 1) </br>
c = a*b</br>
#### What will be c? (If you’re not sure, feel free to run this in python to find out).
1. This will invoke broadcasting, so b is copied three times to become (3,3), and *∗ is an element-wise product so c.shape will be (3, 3)
2. This will invoke broadcasting, so b is copied three times to become (3, 3), and *∗ invokes a matrix multiplication operation of two 3x3 matrices so c.shape will be (3, 3)
3. This will multiply a 3x3 matrix a with a 3x1 vector, thus resulting in a 3x1 vector. That is, c.shape = (3,1).
4. It will lead to an error since you cannot use “*” to operate on these two matrices. You need to instead use np.dot(a,b)
ans : 
#### Question10 : Question 10 Consider the following computation graph.
<img src="https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CLczrXpHEeeA3RJRlG3Uqg_3c66355aff0ae7db9e27206f188267f0_Screen-Shot-2017-08-05-at-6.30.51-PM.png?expiry=1567641600000&hmac=X1f0SjC0lDNxnCRu_bqwnD4u2m27Q9Hzyx2HDDC7vqo">

#### What is the output J?
1. J = (c - 1)*(b + a)
2. J = (a - 1) * (b + c)
3. J = a*b + b*c + a*c
4. J = (b - 1) * (c + a)
