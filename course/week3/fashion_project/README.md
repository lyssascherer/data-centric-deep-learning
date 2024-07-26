# Week 3 Project: Active learning on fashion classifier

```
pip install -e .
```

This project will investigate various strategies to identify elements for relabeling.

# Results

- Accuracy on the fixed FashionMNIST test set using model.ckpt
    -  85.26%
    - `{'acc': 0.8526358008384705, 'loss': 0.4197469651699066}`
    
- Accuracy on set of production data using model.ckpt
    - 30.21%
    - `{'acc': 0.3021000027656555, 'loss': 7.151782989501953}`
    - the low accuracy can be caused by a data shift in production. By checking the images in the production dataset we see that it has rotated images of fashion items, while the offline dataset had only images of straight fashion items (examples in `image_analysis.ipynb`).

- Accuracy on set of production data using random.ckpt
    - 31.13%
    - `{'acc': 0.31139999628067017, 'loss': 1.9035247564315796}`

- Accuracy on set of production data using uncertainty.ckpt
    - 39.49%
    - `{'acc': 0.39499998092651367, 'loss': 2.771846294403076}`

- Accuracy on set of production data using margin.ckpt
    - 35.79%
    - `{'acc': 0.3579999804496765, 'loss': 1.9569098949432373}`

- Accuracy on set of production data using entropy.ckpt
    - 38.15%
    - `{'acc': 0.3815999925136566, 'loss': 3.192443370819092}`

- Accuracy on the fixed FashionMNIST test set using augment.ckpt
    -  52.53%
    - `{'acc': 0.5253594517707825, 'loss': 1.310063123703003}`

- Accuracy on set of production data using augment.ckpt
    - 49.07%
    - `{'acc': 0.4907999634742737, 'loss': 1.3892154693603516}`


# Summary of accuracy in production data:

- MODEL (DEFAULT).    : 30.21%
- MODEL (RANDOM)      : 31.13%
- MODEL (UNCERTAINTY) : 39.49%
- MODEL (MARGIN)      : 35.79%
- MODEL (ENTROPY)     : 38.15%
- MODEL (AUGMENT)     : 49.07%