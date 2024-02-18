#  1. Quaternion to rotation matrix, code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574447165
  ```  
##  4. Display of results 

>  Quaternion-to-rotation matrix; [[-0.6 -0.8 0.] [0.8 -0.6 0.] [0.0.1.]] 

#  Second, Euler angular rotation matrix 

##  3. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574447165
  ```  
##  4. Display of results 

>  The Euler angle rotated 90 degrees along the X axis and 45 degrees along the Z axis is converted into a rotation matrix of [7.07106781e-01 -7.07106781e-01 0.000000e + 00] [4.32978028e-17 4.32978028e-17 -1.00000000e + 00] [7.07106781e-01 7.07106781e-01 6.12323400e-17]] 

#  Rotation vector to rotation matrix 

##  1. Rotation vector 

   For the rotation of a coordinate system, we know that any rotation can be characterized by an axis of rotation and an angle of rotation. Therefore, we can use a vector whose direction is consistent with the axis of rotation and whose length is equal to the angle of rotation. This vector is called a rotation vector (or axis angle, Axis-Angle). This representation requires only one three-dimensional vector to describe rotation. The purpose of this paper is to introduce the use of rotation vectors in open3d. The theoretical basis of rotation vectors will not be expanded in detail. Please refer to: Rotation Matrix and Rotation Vector 

##  2. Main functions 

   Open3d.geometry.get_rotation_matrix_from_axis_angle () implements the conversion of rotation vectors to rotation matrices. 

##  3. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574447165
  ```  
##  4. Display of results 

>  The rotation vector rotated 45 degrees along the Z axis is converted into a rotation matrix of; [[0.70710678 -0.70710678 0.] [0.70710678 0.70710678 0.] [0.0.1.]] 

