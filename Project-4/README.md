# Cuda Project

## iota

### Cpu 
|10| 0.00| 0.00| 0.00|
|100| 0.00| 0.00| 0.00|
|1000| 0.00| 0.00| 0.00|
|10000| 0.00| 0.00| 0.00|
|100000| 0.00| 0.00| 0.00|
|1000000| 0.00| 0.00| 0.00|
|5000000| 0.02| 0.00| 0.02|
|100000000| 0.52| 0.07| 0.45|
|500000000| 2.64| 0.40| 2.23|
|1000000000| 5.33| 0.87| 4.45|
|5000000000|35.69| 5.43|30.26|

### Gpu
|10| 0.13| 0.01| 0.10|
|100| 0.10| 0.00| 0.09|
|1000| 0.11| 0.00| 0.09|
|10000| 0.11| 0.00| 0.10|
|100000| 0.10| 0.00| 0.09|
|1000000| 0.10| 0.00| 0.09|
|5000000| 0.13| 0.02| 0.11|
|100000000| 0.71| 0.17| 0.53|
|500000000| 2.96| 0.63| 2.32|
|1000000000| 6.54| 1.92| 4.61|
|5000000000|45.80| 9.55|36.24|

- CPU iota final test - 36s
- GPU iota final test - 50s
The results are not what I expected. The CPU was faster than the GPU.
I assume this is because the operation is almost instant, and the overhead of sending out operations to the GPU is a lot of work when compared to directly addressing the memory on the CPU. Maybe that's what's being shown in the sys column, where the GPU final time takes 6s longer.

## Julia/mandlebrot set
- CPU set creation - 1.94s
- GPU set creation - 0.12s

This makes sense, as image generation/manipulation is very parallel, and the computation can be spread out easily. It's also what CUDA is made for.

Here is the generated mandlebrot set


![julia set](julia.png)
