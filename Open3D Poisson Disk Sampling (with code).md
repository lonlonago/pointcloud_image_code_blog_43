#  First, the principle of the algorithm 

##  1. Nature 

 An ideal Poisson disk sampling point set needs to satisfy three conditions: 

   The sampling method that satisfies these three conditions is called maximized Poisson disc sampling. The effect after sampling is good, which can satisfy the uniform data points, retain the details better, and have better blue noise characteristics. The algorithm has a large time complexity 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095744630
  ```  
 The function samples points from the grid, where each point is approximately the same distance from its neighbors (blue noise). 

##  3. References 

>  [1] Quan Weize, Guo Jianwei, Zhang Yikuan, Meng Weiliang, Zhang Xiaopeng, Yan Dongming. Maximizing Poisson Disk Sampling Based on Sampling Radius Optimization [J]. China Science: Information Science, 2017, 47 (04): 442-454. [2] Sample Elimination for Generating Poisson Disk Sample Sets, EUROGRAPHICS, 2015. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095744630
  ```  
#  III. Display of results 

##  1. Grid model 

 ![avatar]( b4bfd65c1ea3476d929b5e6077cedd5c.png) 

##  2. Sampling results 

 ![avatar]( 8d013f0f43db4e959fe5c7816bedf8b8.png) 

##  3. Sampling results in point clouds 

 ![avatar]( b9bd7eb1118949968418b78797fc09d4.png) 

