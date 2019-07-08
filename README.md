##‘Feature embeddings’
This is an example of ‘feature embeddings’ from a medical data set displayed in the TensorFlow projector. The idea of ‘feature embeddings’ is to extend the application of word embeddings to any kind of features. To do so features are discretized into bins if not categorical and then all of them are one-hot encoded. In the next step, for every record a ‘text’ is generated based on the one hot encodings and the respective column header.
For instance the new text representation of the features of a particular record will look like this:
“sex_1, extension_of_lesion_1, experience_2, morbidity_state_2, bmi_2, current_smoker_2…..”

And another one like this:
“sex_2, extension_of_lesion_3, experience_2, morbidity_state_4, bmi_3, current_smoker_1…..”

Now, machine learning models based on word embeddings usually only used in text analytics can be applied in a data set with continuous and/or categorical features of any origin.
The use of word embeddings gives every feature not just a weight but a defined vector in space. This allows the display of neighboring features based on the embedding vectors and PCA which can then be displayed in the TensorFlow projector as shown here:

http://projector.tensorflow.org/?config=https://raw.githubusercontent.com/xenonsgt/Disc/master/template_projector_config.json

Machine learning classifiers or regression models can therefore also be created. In the current example, a neural network based on feature embeddings, a one dimensional convolutional layer and two bidirectional LSTM layers performed slightly lower than a standard random forest regressor on the same data set . The idea of ‘feature embeddings’ will need to be explored further to find out if it can be a valuable extension of the concept of word embeddings.


