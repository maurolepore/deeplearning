Deep learning with R: Chapter 3
================
Mauro

<https://livebook.manning.com/book/deep-learning-with-r/chapter-3/>

# Install

## Option GPU: Hard to install but fast

How can I find out if I have a GPU?

## Option CPU: Easy to install but slow

> Stick with the CPU version to start out, then install the GPU version
> once your training becomes more computationally demanding.

– <https://tensorflow.rstudio.com/tools/local_gpu>

## Quick start: via `install_tensorflow()`

> `install_tensorflow()` … provides an easy to use wrapper for the
> various steps required to install TensorFlow.

– <https://tensorflow.rstudio.com/installation/>

## Install tensoflow

``` r
# install.packages("tensorflow")

library(tensorflow)
Error: package or namespace load failed for ‘tensorflow’ in dyn.load(file, DLLpath = DLLpath, ...):
 unable to load shared object '/home/mauro/R/x86_64-pc-linux-gnu-library/4.0/Matrix/libs/Matrix.so':
  libRlapack.so: cannot open shared object file: No such file or directory
```
