# NLP_FINAL_PROJECT

### Dataset Information

##### The training and testing data cann be downloaded from the below provided links:
##### Training Data: https://drive.google.com/file/d/1WiQQ5Tq4MHClNrXPB9jFuK667IHKcbTO/view?usp=sharing
##### Testing Data: https://drive.google.com/file/d/1afcla6nhNkPD1y7mCgolFvSG8W8DvYef/view?usp=sharing
##### The training data consists of 400k rows of data and testing data consists of 3.5M rows. 
### Preprocessing techniques used
##### Removed unwanted coulmns of the train and test data set.Balanced the training dataset by is_duplicate feature(considered the same number of is_duplicate=0 and is_duplicate=1 rows). Defined a POS function to categorize the text to a particular parts of speech. Defined a clen text method to convert text into lower case, convert HTML tags into blank space, to remove @-mentions and hashtags and remove unwanted words. Performed lemmatization and filered the text by removing stop words and also by dropping the NULL values. Implemented Tokenization and padded the input sequences to balance out the input that is fed to the model. 

### Models Used 

#### 1) LSTM model
##### Used GLOVE Embeddings with 200 dimensions. Initially defined two models, a question1 model and a question2 model each containing a embedding layer ,3 LSTM layers and 2 fully connected dense layers. Merged the above two models and added few more dense layers with relu and sigmoid activation functions for merged model. Built the model with the help of keras and used adam optimizer.

#### 2) BiLSTM model
##### Used GLOVE Embeddings with 200 dimensions. Defined two input layers, one for question1 and other for question2. Created an embedding layer which takes in both the inputs. The output of this embedding layer is then fed into a BiLSTM layer. Finally two fully connected layers are added with relu and sigmoid activation functions. Similar to LSTM, adam optimizer was used.

#### 3) MaLSTM model
##### Used Word2Vec word embedding for this model. Created embedding matrix and assigned each word to its word2vec embedding. Defined the MaLSTM Similarity function. Defined left and right input layers and fed them into the embedding layer. Since this is a siamese network, both sides share the same LSTM. Calculated the distance as defined by the MaLSTM model and then built the model using adadelta optimizer.

### Running the source code
##### Download the ipynb files from models folder in the main page and download the data from the google drive links provided in the data folder . Keep the data and model files in the same directory and run each cell in the ipynb files in the jupiter notebook.

### Input and Output
##### Input data contains string columns(question1 and question2) with questions and Output data contains  a feature  with 0 and 1 classes

### Results
##### Calculated training accuracy,validation accuracy,training loss, validation loss for the three models.
##### We could't calculate the test accuracy because there is no feature with class variable in the test data set.
##### Indetail explaination about results can be seen in the results file


