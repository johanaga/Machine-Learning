# WikiGen

###### Overview:
 - **WikiGen** is a wikipedia page text generator/paraphraser. Text is generated based off of a given wikipedia page title, a word count, and the number of unique generated texts to be created.

###### Dataset:
 - Dataset is obtained from wikipedia via its python library: https://pypi.org/project/wikipedia/

###### Results/Errors:
 - Project is far from perfect. Generated text sometimes lacks coherency. Additionally, not all generated words are real words.
 -  Quality of generated text is proportional to size of given input data. For example, a book about Elvis Presley with 1M+ characters will generate vastly better results compared to his wikipedia page with 100,000 characters.

###### Improvement:
 - Add regularization / fine tune hyperparameters
 - Monitor and display time when generating text
 - Instead of solely relying on wikipedia text, I can implement web scraping of a given topic of interest to accumulate substantially more training data to further increase model and generator efficacy.
