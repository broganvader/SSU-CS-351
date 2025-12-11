# Cuda Project

## iota
- CPU iota final test - 36s
- GPU iota final test - 50s
The results are not what I expected. The CPU was faster than the GPU.
I assume this is because the operation is almost instant, and the overhead of sending out operations to the GPU is a lot of work when compared to directly addressing the memory on the CPU.

## Julia
- CPU set creation - 1.94s
- GPU set creation - 0.12s

This 



![julia set](julia.png)
