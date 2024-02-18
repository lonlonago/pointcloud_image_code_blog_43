#  First, the principle of the algorithm 

##  1. Registration process 

   ICP iteratively corrects the rigid body transformation (translation, rotation) of the two original point clouds to minimize the distance between all point sets. Input: Two frames of original point clouds, initial estimate of the transformation, standard for stopping the iteration; Output: transformation matrix, modified point cloud after transformation. ICP algorithm steps: (1) For the point set 

 (4) Determine whether the convergence is based on the iteration error of the previous two iterations and the number of iterations.

     T0 = T0, repeat step (1). 

##  2. References 

>  [1] BESL P J, MCKAY N D. A method for registration of 3-Dshapes [J]. IEEE Transactions on Pattern Analysis and Machine Intelligence, 1992, 14 (2): 239-256. [2] Wang Fei, Liu Rufei, Ren Hongwei, Chai Yongning. Multi-phase vehicle laser point cloud registration using road target characteristics [J]. Journal of Surveying and Mapping Science and Technology, 2020, 37 (05): 496-502. 

#  Second, the main function 

 1. This class TransformationEstimationPointToPoint provides a function for computing the residuals and Jacobian matrix of the point-to-point ICP objective function. The function registration_icp take it as a parameter and run the point-to-point ICP to get the result. 2. The function evaluate_registration compute two main metrics. Fitness computes the overlapping area (interior point correspondence/number of target points). The higher the better. inlier_rmse computes the root mean square error RMSE for all intrinsic correspondence. The lower the better. 3. Since the function transformand paint_uniform_color changes the point cloud, the visualization part calls copy.deepcoy to replicate and protect the original point cloud. 

#  III. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574429074
  ```  
#  IV. Display of results 

##  1. Initial position 

 ![avatar]( 20200828190129900.png) 

##  2. Registration results 

 ![avatar]( 2020082819022375.png) 

#  V. Reference links 

 1. Point-to-point ICP 2. Open3d learning plan - 9 (ICP registration) 3. Tutorial: Python Open3d completes ICP point cloud registration 

