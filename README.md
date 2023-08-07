# A-new-thinning-algorithm-for-binary-images
Implement of following paper:  
"L. Ben Boudaoud, A. Sider and A. Tari, "[A new thinning algorithm for binary images]" 2015 3rd International Conference on Control, Engineering & Information 
Technology (CEIT), 2015, pp. 1-6, doi: 10.1109/CEIT.2015.7233099.  
Compare with ZS algorithom：  
T. Y. Zhang and C. Y. Suen. 1984. [A fast parallel algorithm for thinning digital patterns]. Commun. ACM 27, 3 (March 1984), 236–239. 

## ZS Algorithm
- Algorithm description:
  - For the first iteration , if the edge of point P1 satisfies the following conditions, it will be deleted P1：  
(1) 2 ≤ 𝐵(𝑃1) ≤ 6  
(2) 𝐴(𝑃1) = 1  
(3) 𝑃2×𝑃4×𝑃6= 0  
(4) 𝑃4×𝑃6×𝑃8= 0  
𝐴(𝑃1) When traversing the 8 neighbors of 𝑃1，the number of values changing from 0 to 1 (white to black)；
  - For the second iteration, if point P1 satisfies the following conditions, will deleted P1：  
(1) 2 ≤ 𝐵𝐵(𝑃𝑃1) ≤ 6  
(2) 𝐴𝐴(𝑃𝑃1) = 1  
(3) 𝑃𝑃2×𝑃𝑃4×𝑃𝑃8= 0  
(4) 𝑃𝑃2×𝑃𝑃6×𝑃𝑃8= 0  
## The New Thinning Algorithm
- Algorithm description：
(1) Use the same 8-connected neighborhood as the ZS algorithm.   
(2) 𝑃1 is the pixel to be deleted.  
(3) 𝐵(𝑃1) = ∑ 𝑃𝑖𝑖9𝑖𝑖=2 is the number of 1 (black grid) in 𝑃1、𝑃2、𝑃3 … 𝑃8.   
(4) 𝐶(𝑃𝑃1) =¬𝑃2∧ (𝑃3∨𝑃4) + ¬𝑃4∧ (𝑃5∨𝑃6) + ¬𝑃6∧ (𝑃7∨𝑃8) + ¬𝑃8∧ (𝑃9∨𝑃2) is the "1" in the 8-connected neighborhood of the number of connected 8-components.  
## Result
[A new thinning algorithm for binary images]:https://ieeexplore.ieee.org/document/7233099/references#references
[A fast parallel algorithm for thinning digital patterns]:https://doi.org/10.1145/357994.358023
