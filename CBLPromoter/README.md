# CBLPromoter

###### Links: 
 - **Reference article:** https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6460014/
 - **Eukaryotic Promoter Database:** https://epd.epfl.ch//index.php

###### Overview:
 - **CBLPromoter** is DNA promoter sequence classifier that distinguishes promoters from non-promoters based off of a CNN-BiLSTM architecture.

###### Motivation: 
 - Due to the important role of the promoters in gene transcription, accurate prediction of promoter sites becomes a required step in gene expression, patterns interpretation, and building and understanding the functionality of genetic regulatory networks.

###### Dataset:
 - **Specifications:** All sequences have a length of 300 bp and were extracted from -249~+50 bp (+1 refers to TSS position)
 - **Negative Dataset:** A challenging negative dataset was generated to produce better model generalization. Explanation and process of generating is described in the article and is replicated in my code.

###### Results/Errors:
 - Current model is only configured to classify non-TATA box promoter sequences.
 - Model is still overfitting quite a bit and producing a very high validation loss. More data, a learning rate scheduler, and finer hyperparamter tuning would certainly help to regularize the model better. Additionally, Keras Tuner was used to find the current model hyperparameters.
 - Recall is very low, Accuracy and Precision looking adequate
 - Validation loss decreases then increases which is a sign of overfitting and needs to be addressed in future model versions 

###### Comparison:
| Promoter       | Method          | Precision | Recall |
| :---           |    :---         | :---      |   :--- |
|                | CNNProm         | 0.58      | 0.83   |
|                | DeePromoter     | 0.92      | 0.95   |
| Human non-TATA | **CBLPromoter** | **0.77**  |**0.61**|
|                | CNNProm         | 0.54      | 0.86   |
|                | DeePromoter     | 0.91      | 0.90   |
| Mouse non-TATA | **CBLPromoter** | **0.79**  |**0.61**|
