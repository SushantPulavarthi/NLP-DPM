## Proposed Approach

The main approach will be to try and fine tune the pre-existing DeBERTA model on the PCL dataset. This is because this model will be better at understanding the underlying features and patterns in the texts, and will be able to better determine whether a text is PCL or not.

From the EDA, we can see that the dataset is heavily biased towards articles that do not contain PCL. Therefore to tackle this, we will need to either better sample the PCL cases or augment the dataset to increase the number of PCL cases. I will be implementing weighted random sampling, as this is a good way to increase the representation of PCL cases in the training data. And I do not downsample as it could lead to a loss of information. Additionally we can look at some other techniques such as randomly removing or swapping words; or even better implementing things like back-translation or paraphrasing to further increase the number of PCL cases.

Finally I can also do some manual hyperparameter tuning to find more optimal hyperparameters for things such as learning rate, batch size, etc.

Overall, hopefully we will see that the model will be better equipped to identify the underlying subtlties and better distinguish between PCL and non-PCL texts, therefore increasing the F1 scores.