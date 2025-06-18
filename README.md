# Book Recommender
## Objective:
To build a simple book recommendation system using collaborative filtering with TensorFlow and Keras, based on implicit feedback from users' book interactions (e.g., ratings or selections).
It learns embedding vectors for both users and books and then recommends books to a user by computing similarity scores between embeddings.

## Tools and Libraries:
TensorFlow: For building and training the neural network model using Keras and performing tensor operations.  
Pandas: For reading and processing CSV files (book.csv and book-ratings.csv).  
NumPy: Imported, though not directly used—commonly helpful for numerical operations.  

## Visualizations
Visualization 1: Top-5 Recommendations for Sample Users  
Visualization 2: Cosine Similarity Between Book Embeddings

## Experiments
### Experiment 1: Impact of Parallel Data Loading in the Data Pipeline
Testing Parallel Data Loading with num_parallel_calls  
Purpose: explicitly demonstrate the impact of parallel data loading in your TensorFlow data pipeline  
Actions: Modified prepare_dataset function to use the num_parallel_calls argument. Allows TensorFlow to process multiple elements of the dataset in parallel, potentially speeding up data input and preprocessing.

### Experiment 2: Training Loss by Epoch Monitoring Training Progress Using a Custom Keras Callback
Purpose: To observe how the model’s loss value changes over multiple training epochs and whether the model is learning effectively.  
Actions: A custom Keras callback class was created to record the training loss at the end of each epoch. The callback was passed into the model’s .fit() function and then ran for 3 epochs. After training, a simple table was printed to display how the loss value changed with each pass over the dataset. This helped evaluate the model's convergence and identify whether the learning rate or number of epochs might need adjustment.
