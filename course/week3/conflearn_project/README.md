# Week 3 Project: Confidence learning on sentiments

```
pip install -e .
```

This project will implement confidence learning to identify elements for relabeling. Please download a dataset of precomputed embeddings [here](https://drive.google.com/file/d/12UtQMwfSgm4FpXSFZvLDNLO8VGxzCPYq/view?usp=sharing). Please `conflearn_project/data` with the unzipped file.


# Results

- Model accuracy without confidence learning:  88.33% 
    - `{'acc': 0.8833125233650208, 'loss': 0.30028796195983887}`

- Model accuracy with confidence learning 92.31%
    - `{'acc': 0.9231874942779541, 'loss': 0.1792345643043518}`


## Manual annotation

```
These colors are for older women & also peels quite easily for a high-end nail polish.
```

In the above example conflearn detected the lable was potentially wrong, after flipping the prediction we get that this is positive, but I would say it is negative.

I saw other examples that were mixed, the customer said they loved the product, but complained about something. I'm not sure if it is a positivie or negative review in this case.

Another example was just giberish.