+++
title = "Making predictions from a model file"
description = "Loading the model and making predictions from R"
weight = 10
draft = false
toc = true
bref = "decryptr allows you to load a trained model from a `.hdf5` file and make predictions for new captchas"
+++

### Loading the model

If you trained a model with decryptr API or [a custom model](/docs/custom-model/) and saved the model file at some point you will need to make predictions using the trained model.

First, you will need to load the model to memmory. `decryptr` provides a `load_model` function that can be used to do so.

```
library(decryptr)
model <- load_model("model.hdf5", labs = c(letters, 0:9))
```

> It's important to note the `labs` argument of the function `load_model`. It **must** be the same that you passed to the `read_captcha` when reading the captchas for training.

If you want to load a pre-trained model you can use the name found in [this list](/docs/list-models/) with the `load_model` function.

```
model <- load_model("rfb") # example using rfb
```

### Making predictions

After loading the model, one can easily make predictions for a new captcha by running:

```
captcha <- read_captcha("path-to-captcha.png")
decrypt(captcha, model)
```

The `decrypt` function will return a scalar character containing the predicted content of the captchas.




