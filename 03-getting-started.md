Deep learning with R: Chapter 3
================
Mauro

<https://livebook.manning.com/book/deep-learning-with-r/chapter-3/>

# Install

## Option CPU: slow but installing it is "Easy

> Stick with the CPU version to start out, then install the GPU version
> once your training becomes more computationally demanding.

– <https://tensorflow.rstudio.com/tools/local_gpu>

## Quick start: via `install_tensorflow()`

> `install_tensorflow()` … provides an easy to use wrapper for the
> various steps required to install TensorFlow.

– <https://tensorflow.rstudio.com/installation/>

## Failed locally and on rstudio.cloud

Locally with options auto and custom. On RStudio with option auto

Links:

  - <https://tensorflow.rstudio.com/installation/custom/>
  - <https://www.tensorflow.org/install/>

## Success with with Docker

<https://hub.docker.com/r/rocker/tensorflow>

    -| rocker/tidyverse
      -| rocker/tensorflow
        -| rocker/ml
      -| rocker/cuda 
        -| rocker/tensorflow-gpu
          -| rocker/ml-gpu
        -| rocker/cuda-dev

## docker start tidyveerse -i

``` bash
# docker run -e PASSWORD=123 -p 8787:8787 rocker/tidyverse
docker start tidyveerse -i
```

## Back to the book

``` r
# install.packages("tensorflow")
tensorflow::install_tensorflow()
#> 
#> Installation complete.
```

``` r
# install.packages("keras")
keras::install_keras()
#> 
#> Installation complete.
```

## House prices

``` r
library(keras)
```

## Data

``` r
dataset <- dataset_boston_housing()
```

## Data: works?

<https://stackoverflow.com/questions/48006018/reading-npz-files-from-r>

``` r
library(reticulate)
np <- import("numpy")

dataset <- np$load("data/boston_housing.npz")
c(c(train_data, train_targets), c(test_data, test_targets)) %<-% dataset
#> Error: invalid `%<-%` right-hand side, incorrect number of values
```

``` r
c(c(train_data, train_targets), c(test_data, test_targets)) %<-% dataset
```
