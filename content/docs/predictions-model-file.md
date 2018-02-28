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
model <- load_model("model.hdf5")
```

### Making predictions

After loading the model, one can easily make predictions for a new captcha by running:

```
captcha <- read_captcha("path-to-captcha.png")
decrypt(captcha, model)
```

The `decrypt` function will return a scalar character containing the predicted content of the captchas.




