# Week 2 Project: Test driven deep learning

```
pip install -e .
```

This project will be using production deep learning tools to reliably evaluate deep learning models.

## Warmup

If you haven't yet, please do the [tutorial exercises](https://docs.metaflow.org/getting-started/tutorials) for MetaFlow. 


## Notes Regression
- Regression test dataset: we get all wrongly predicted images by checkpoint of a linear regressilo model (linear.ckpt), and from those we get the top 100 with the worst(highest) loss to be our regression test dataset. 
- Regression test: use the mlp model (mlp.ckpt) to predict the images in the regression test dataset. The accuracy was around 0.939 with 0.166 loss, which means the mlp model correctly predicted the lables 93% of the time of cases where the linear model got wrong. ** if I run the linear model I get 89%, but higher loss(0.332)-- is this result expected?

## Notes Directionality
- Directionality test dataset: we rotate and add noise to the images from the integration dataset. The idea is that the model should not break in case we for example change the camera(noise) or if we take a picture in a different angle.
- Regression test: the acc of the linear model for this dataset is 0.89, and 0.649 for the mlp model. This shows that the mlp is less robust to changes (rotation and noise) on the input.