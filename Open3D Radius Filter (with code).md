#  First, the principle of the algorithm 

##  1. Overview of the principle 

 ![avatar]( 6f0f76e32d4344bc83f62f77fe8e8903.png) 

   The filtering idea of the radius filter is very straightforward, that is, in the point cloud data, set each point to have at least enough close neighbors within a certain radius, and it will be deleted if it is not satisfied. For example, if you specify a radius d, and then specify that there are at least 1 neighbor within the radius, then only the yellow points in the image below will be deleted from the point cloud. If you specify at least 2 neighbors within the radius, then both the yellow and green points will be deleted from the point cloud.  

##  2. Implementation process 

##  3. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574421044
  ```  
##  4. Algorithm source code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574421044
  ```  
##  5. References 

>  [1] Chen Hongyi, Hu Xiaobin, Li Chongrui. Application of ground 3D laser scanning technology in deformation monitoring [J]. Bulletin of Surveying and Mapping, 2014 (12): 74-77. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574421044
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 20210227103224773.png) 

##  2. The filtered point cloud 

 ![avatar]( 20210227103231316.png) 

