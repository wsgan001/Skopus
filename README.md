# Skopus
Exact discovery of the top-k sequential patterns under Leverage

# Preamble

This code was used to generate the results of the paper entitled: 
*Skopus: Mining top-k sequential patterns under Leverage*.
When using this repository, please cite:
```
@article{Petitjean2016-Skopus,
  author    = {Petitjean, Francois and Li, Tao and Tatti, Nikolaj and Webb, Geoffrey I.},
  title     = {Skopus: Mining top-k sequential patterns under Leverage},
  journal   = {Data Mining and Knowledge Discovery},
  volume    = {30},
  number    = {5},
  pages     = {1086--1111},
  year      = {2016}
}
```
Note the paper is available [here](http://francois-petitjean.com/Research/Petitjean2016-Skopus.pdf)


# Copyright
The code in `src` is provided under GLP License version 3. 

Datasets are provided for reproducibility and without any license. 

# Running
From where you have build the project, simply call
```
java -Xmx1g skopus.InterestingnessMeasureMain <dataset> <output-folder> -i2 -m1 -k100
```
The parameters are: 
```
-i<number>: the interestingness measure (1 for support, 2 for leverage [to be used by default])
-m<number>: m-value for the smoothing of support (1 is Lapace, 0 is MLE)
-k<number>: top-"how-many" patterns you want to extract
-l<number>: maximum length of the patterns
```

If you want have a large dataset and/or want to speed up the computation, you can limit the size to, say, patterns of length 5:
```
java -Xmx1g skopus.InterestingnessMeasureMain <dataset> <output> -i2 -m1 -k100 -l5
```


