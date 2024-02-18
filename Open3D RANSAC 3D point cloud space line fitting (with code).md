#  First, the principle of the algorithm 

##  1. Introduction to the algorithm 

   The RANSAC algorithm, proposed by Fischler and Bolles in 1981, is a method for iteratively and robustly estimating model parameters from data sets. The basic ideas of the algorithm are: continuously randomly select sample sets from the data set to seek model parameters that support more interior points; use the model remainder to test the obtained model parameters; through a certain number of iterations, when the consistency probability of the sampled sample set and the comprehensive understanding is the largest, the sampled sample set is regarded as the comprehensive understanding sample set, and the correctness of the parameter solution is supported by the sample remainder test. The data set contains correct data (inner point inliers) and abnormal data (outer point outliers). The essence of the calculation process of the algorithm is to assume and test: assume that the randomly sampled data are all interior points, use the randomly sampled data to calculate the model parameters; test the estimated model parameters through other points. The RANSAC algorithm requires to ensure that under a certain confidence probability, the minimum number of samples N of its basic subset and the probability of obtaining at least one benign sampling subset satisfy the relationship of equation (1). In the formula: the probability of interior points in the data set, that is, the minimum amount of data required to calculate the model parameters. 

##  2. Straight line fitting 

   The parameter setting of the RANSAC algorithm applied to the fitting of spatial straight lines is as follows: 1) Objective function. The process of maximizing the number of inner points under the model parameters in different iterative processes. The objective function of the RANSAC algorithm applied to the fitting of spatial straight lines is to obtain the parameter model containing the most inner points according to the distance threshold of the known spatial straight line. 2) Sampling subset size. In the iterative calculation process, the model parameters need to be calculated using a subset, and each sampling subset should be the minimum sampling set with the size of the data volume. Spatial straight line fitting requires at least 2 spatial points, so when the RANSAC algorithm is applied to three-dimensional spatial straight line fitting, take. 3) Iteration termination condition. The number of iteration termination of RANSAC can be obtained by theoretical calculation. Under the condition of confidence level, there is at least one sample in the loop process, so that the points of the sampled subset are all interior points, thus ensuring that at least one sample can obtain the maximum value of the objective function in the iteration process. Therefore, from equation (1), the loop termination condition should satisfy the conditional expression (2).  

 ![avatar]( 31a31c45912749bf928d10edbc9ec22a.png) 

   In the formula: the confidence level is generally set to within the range of [95%, 99%]; in general, as the probability of interior points in the data set, it belongs to the unknown parameter. Therefore, the proportion of interior points under the worst condition can be taken, and then the proportion of the current maximum interior points can be continuously updated as the number of iterations increases. The confidence level is generally set to 99%. In summary, the process of using the RANSAC algorithm to solve the geometric parameters of space straight lines is shown in the figure below.  

##  3. References 

>  Bao Jianqiang, Zhang Xianzhou, Li Yuan, Xiao Yuanmiao, Chen Xiao, Luo Chao. Application analysis of various spatial straight line fitting methods [J]. Science of Surveying and Mapping, 2020, 45 (05): 132-139 + 151. 

#  Code implementation 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490550
  ```  
 Find the optimal equation for a three-dimensional straight line. A straight line in three-dimensional space is defined as, but the sum is a vector, not a scalar.  

##  2. Simulation data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490550
  ```  
##  3. Measured data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490550
  ```  
#  III. Display of results 

##  1. Simulation data 

 ![avatar]( 7845698f65b24b9eb02b6b3991da1de3.png) 

 1, generative model 2, sampling test data  

 3. Fitting results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490550
  ```  
 ![avatar]( f633500e0b374da29b53b8c7530d0bdb.png) 

##  2. Measured data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490550
  ```  
 ![avatar]( e2439ffbb7da4325a0b4ccc221c24f8b.png) 

