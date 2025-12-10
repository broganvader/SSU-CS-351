# Threaded project

## Computing Mean
![mean computation time graph](proj4/mean.png)

The threaded program takes much less time to complete the calculation, but there are diminishing returns after about 10 cores, and virtually no gain after 32 cores. The time converges at about 1.7 seconds which happens at 32 cores, so any more than that is unnecessary. 
- You do not get linear scaling as you add mroe cores
- for the maximum speed equation:
 T = (1 - p)T + pT
    - I would say p (fraction of your program that is run in parallel) would be about 0.95, as the time the multithreaded program converges to is 5% of the total serial time. So the 5% that can't be cut out is most likely the serial part, leaving the rest to be parallelized. 

-  

## Computing Volume
![volume comp time graph](proj4/volume.png)



