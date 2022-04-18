### Below are the saved .h5 models
#### https://drive.google.com/file/d/1VGeeN-8_wmp-dkWLfvBh3zjlo2pL52np/view?usp=sharing
#### https://drive.google.com/file/d/1B51GDyaaehfVjQWQ8A6phr17M6WrqqnA/view?usp=sharing


#### Calculated training accuracy,validation accuracy,training loss, validation loss for the three models. We also predicted the output data using model.predict.
#### We could't calculate the test accuracy because there is no feature with class variable in the test data set.

### LSTM Model
#### We used 258k rows for training and 50k rows for validation. We trained the LSTM model for 20 epochs with a batch size of 2000. 
#### Accuracy for each epoch can be seen in the below diagram.
![Alt text](/screenshots/1.png?raw=true)
#### Below is the graph representing Training accuracy, Validation accuracy, Training loss and Validation loss.
![Alt text](/screenshots/2.png?raw=true)

### BiLSTM Model
#### We used 258k rows for training and 50k rows for validation. We trained the LSTM model for 10 epochs with a batch size of 2000. 
#### Accuracy for each epoch can be seen in the below diagram.
![Alt text](/screenshots/3.png?raw=true)
#### Below is the graph representing Training accuracy, Validation accuracy, Training loss and Validation loss.
![Alt text](/screenshots/4.png?raw=true)

### MaLSTM Model
#### We used 258k rows for training and 50k rows for validation. 
#### We started training the model for 10 epochs. We initially obtained a training accuracy of 75% on the 9th epoch and we faced a kernel dead error. We tried training the model several times again and we got stuck with the same error again and again. Its been extremely difficult to train this model as each epoch is training over 3 hours. When we restart the kernel, the model starts again with an accuracy of 65%. Below we attached a scrrenshot where we trained the model for 2 epochs.
![Alt text](/screenshots/5.png?raw=true)

### Among the three models we trained, we observed that the LSTM model with GLOVE Embedding outperforms both BiLSTM and MaLSTM models with a training accuracy around 93% as compared to other models which acheived a training accuracy of 75% and 61%.
