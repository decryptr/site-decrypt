+++
title = "Benchmark"
description = "Testing speeds of decryptr!"
weight = 11
draft = false
toc = true
bref = "decryptr is very fast to make predictions once the model is loaded."
+++

### Benchmark

Once loaded to memory, keras models run very quickly Also, we don't run any pre-processing on the image, so decryption is blazing fast.

```
microbenchmark::microbenchmark(decrypt = decrypt(captcha, model))
## Unit: milliseconds
##     expr      min       lq     mean   median       uq     max neval
##  decrypt 8.333295 9.256788 10.96834 9.713691 10.47587 106.873   100
```