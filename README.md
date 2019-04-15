# Prediction for pet adoption speed
kaggle competition @ https://www.kaggle.com/c/petfinder-adoption-prediction

### Python/keras/TensorFlow project summary

- Prepared three given datasets for joint analysis:
  - Data fields collected for each pet incl. age, breed, color etc.
  - Pet images and image metadata (obtained via Google Vision API)
  - Pet description's sentiment data (obtained via Google Natural Language API)
- Conducted feature engineering for data fields and sentiment data
- Used keras and TensorFlow backend for image pre-processing and analyses
- Implemented keras basic model plus VGG19 and ResNet50 via transfer learning
- Ran image analyses on local machine and AWS, merged output with other data
- Applied 11 classifier algorithms, grid search and fine-tuning for 4 algorithms

### Project results

![Grid](https://github.com/manuelfreude/kagglepetfinder/blob/master/grid_adaboost.png)

The grid search shows that the best-performing AdaBoost algorithm delivered quadratic Cohen's kappa of about 0.28, which ranked at the time of hand-in within the top 82% of the kaggle competition. In another shot, the AdaBoost achieved quadratic Cohen's kappa of about 0.55, a surprisingly high value, which oddly did not improve the competition score and ranks, so might have been a lucky shot.

Due to fragmented internet connectivity in South East Asia and a high amount of memory required, I chose to run the analyses on my local machine instead of a kaggle kernel, which led to the score being rejected once the competition was finished.

### Conclusion / further improvements

The project, especially the data preparation part, shows how different real-life sources can be leveraged for sophisticated analytics. Well-defined neural networks might lead to a high value second-last image analyses step: determining which features are important for the Adoption speed prediction by the keras model. These features could be transferred in a separate dataset instead of using only the predicted Adoption speed.

This was my first kaggle competition, its completion a big milestone, upon which I moved on to the Santander Customer Transaction prediction.

![kaggle](https://github.com/manuelfreude/kagglepetfinder/blob/master/kaggle_dashboard_petfinder.png)
