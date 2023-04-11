# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step 2:
Translate the image.
<br>

### Step 3:
Scale the image.
<br>

### Step4:
Shear the image.
<br>

### Step 5:
Reflect of image.
<br>

### Step 6:
Rotate the image & Crop the image.
<br>

### Step 7:
Display all the Transformed images.
<br>

## Program:

### Developed By:Sanjay Kumar S S
### Register Number:212221240048
i)Image Translation
```
rows,cols,dim=img.shape
M=np.float32([[1,0,50],[0,1,90],[0,0,1]])
trans=cv2.warpPerspective(img,M,(cols,rows))
plt.axis('off')
plt.imshow(trans)
plt.show()
```
ii) Image Scaling
```
N=np.float32([[1.1,0,0],[0,2,0],[0,0,1]])
scale=cv2.warpPerspective(img,N,(cols,rows))
plt.axis('off')
plt.imshow(scale)
plt.show()
```
iii)Image shearing
```
N_x=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
N_y=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
shear_x=cv2.warpPerspective(img,N_x,(int(cols*1.5),int(rows*1.5)))
shear_y=cv2.warpPerspective(img,N_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(shear_x)
plt.show()
plt.axis('off')
plt.imshow(shear_y)
plt.show()
```
iv)Image Reflection
```
R_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
R_y=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
ref_x=cv2.warpPerspective(img,R_x,(int(cols),int(rows)))
ref_y=cv2.warpPerspective(img,R_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(ref_x)
plt.show()
plt.axis('off')
plt.imshow(ref_y)
plt.show()
```
v)Image Rotation
```
ang=np.radians(25)
N_r=np.float32([[np.cos(ang),-(np.sin(ang)),0],
                [np.sin(ang),np.cos(ang),0],
                [0,0,1]])
rot=cv2.warpPerspective(img,N_r,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rot)
plt.show()

```
vi)Image Cropping
```
cropped_img=img[300:450,300:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Original Image:
![image](https://user-images.githubusercontent.com/93427246/231227312-935bf55e-f04c-41e7-82fc-a79d5fa8a071.png)

###  ii) Image Translation:
<br>
<br>

<img src='https://user-images.githubusercontent.com/93427246/231227785-87e1332b-5c64-4fc0-9103-f0413f6b7277.png'>
<br>
<br>

### iii) Image Scaling:
<br>
<br>
<img src='https://user-images.githubusercontent.com/93427246/231228007-f634134e-4dba-4190-99b1-e649146bff37.png'>

<br>
<br>


### iv)Image shearing:
<br>

<img src='https://user-images.githubusercontent.com/93427246/231228128-03c21702-64c0-4b37-ad7a-654346e525be.png'>
<br>
<br>

<img src='https://user-images.githubusercontent.com/93427246/231228193-3879f7d2-228d-4586-806b-59581fc03454.png'>
<br>


### v)Image Reflection:
<br>

<img src='https://user-images.githubusercontent.com/93427246/231228281-28fb4df9-fe5a-4b18-8155-84f0221b260f.png'>
<br>
<br>

<img src='https://user-images.githubusercontent.com/93427246/231228394-69897baa-a2b1-42a6-8286-3419862390a2.png'>
<br>



### vi)Image Rotation:
<br>
<br>

<img src='https://user-images.githubusercontent.com/93427246/231228459-190cc832-a30b-4cd9-92c0-5b35d1490b19.png'>
<br>
<br>



### vii)Image Cropping:
<br>
<br>

<img src='https://user-images.githubusercontent.com/93427246/231228521-8d5ac70f-c81a-496f-b47b-3c117ffdd88d.png'>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
