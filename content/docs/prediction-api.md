+++
title = "Using the web API for prediction from R"
description = "Zero config captcha decrypting"
weight = 10
draft = false
toc = true
bref = "decryptr offers a free and simple web API that you can use to break captchas that are on our list of pre-trained models."
+++

### Making predictions

The web interface needs 2 parameters passed throught a POST request to an endpoint in `decryptr.now.sh`.
The complete list of endpoints can be found [here]().

The first parameter, `img`, is a base64 encoded image. The second is the api key which you can obtain [here]().

In R, you can make the request by calling:

```
arq <- "path-to-img"
img <- arq %>%
  readr::read_file_raw() %>%
  base64enc::base64encode()

res <- httr::POST(
  "https://decryptr.now.sh/rfb",
  body = list(
    img = img,
    key = "your-api-key"
  ),
  encode = "json"
)
```

