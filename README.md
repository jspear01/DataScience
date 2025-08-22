# DataScience

## Resource

1. Books
- Mathematics for Machine Learning [https://mml-book.github.io/](https://mml-book.github.io/)
- DeepLearning from the Basics by Koki Saitoh
- Mathmatics for Deep Learing [https://d2l.ai/chapter_appendix-mathematics-for-deep-learning/index.html](https://d2l.ai/chapter_appendix-mathematics-for-deep-learning/index.html)
2. Learning
- MIT Matrix Calculation [https://www.youtube.com/playlist?list=PLUl4u3cNGP62EaLLH92E_VCN4izBKK6OE](https://www.youtube.com/playlist?list=PLUl4u3cNGP62EaLLH92E_VCN4izBKK6OE)
- 혁팬하임 유튜브
- Mathmatics for machine learing [https://www.youtube.com/playlist?list=PLiiljHvN6z1_o1ztXTKWPrShrMrBLo5P3](https://www.youtube.com/playlist?list=PLiiljHvN6z1_o1ztXTKWPrShrMrBLo5P3), [https://www.youtube.com/playlist?list=PLiiljHvN6z193BBzS0Ln8NnqQmzimTW23](https://www.youtube.com/playlist?list=PLiiljHvN6z193BBzS0Ln8NnqQmzimTW23)
- Linear Algebra
  - [Immersive Linear Algebra](https://immersivemath.com/ila/index.html), Image Linearing
  - [Interactive Linear Algebra](https://textbooks.math.gatech.edu/ila/), More Mathmatical
  - [Linear Algegra with Python](https://github.com/weijie-chen/Linear-Algebra-With-Python), Python Coding
  3. Interview
- Deep understanding of linear models
- Have a solid understanding of probability and some important probability distribution. (ex. Bete binomial distribution)
- Multi dimentsional space - require strong understanding of variance co-variance matrix

  

## Study Plan

### 1. Data Base
#### - Basic Concept
#### - SQL

Here are 25 most common Deep Learning interview questions for ML research positions:

Fundamentals:
- What is deep learning, and how does it differ from traditional machine learning?
- What is an activation function, and why is it important? Explain three types of activation functions.
- You are using a deep neural network for prediction, but it overfits the training data. What can you do to reduce overfitting?
- What is the vanishing gradient problem in neural networks, and how can it be fixed?
- Explain the process of backpropagation.

Neural Network Architectures:
- Describe the architecture of a typical Convolutional Neural Network (CNN).
- What are Autoencoders, and what are three practical uses of them?
- What is a transformer architecture, and how is it used in NLP tasks?
- What is the role of pooling layers in CNNs?
- What are Recurrent Neural Networks (RNNs), and where are they used?

Training and Optimization:
- How does L1/L2 regularization affect a neural network?
- Why should we use Batch Normalization?
- How do you know if your model is suffering from exploding gradients?
- What is the purpose of dropout in neural networks, and how does it affect training?
- What are some hyperparameters used in training neural networks?

Advanced Topics:
- What are the main gates in LSTM networks, and what are their tasks?
- Explain how self-attention works in transformers.
- Can CNNs be used to classify 1D signals?
- What is transfer learning, and when is it recommended or not?
- How do depthwise separable convolutions improve CNNs?

Practical Implementation:
- Describe the process of pre-training and fine-tuning in transformers.
- What are the main challenges when training a deep learning model with limited data?
- How do you handle class imbalance in deep learning?
- What are the challenges of deploying deep learning models in production?
- How would you modify a pre-trained model from classification to regression?

### 2. Deep Learning

- Vanilla RNN = Neural Network that's able to work with sequential data where each node takes in an element of the sequence with the current understanding of the sequence up to that point and generate a new understanding with that context taken into account

- LSTM = RNN + ability to persist a "memory" via cell state and control updating or resetting this memory as we process sequence (to mitigate the long-term dependency problem if sequence is long)

- Seq2Seq = Putting LSTM/RNNs together in an encoder-decoder architecture. You feed the entire sequence thru encoder and use the compressed, learned understanding from encoder (final hidden state) to predict output sequence in decoder.

- Seq2Seq with attention = Seq2Seq + ability to generate a better final hidden state by computing weighted sum with every hidden layer from encoder to understand how "elements in input sequence relate to one another" and pass that info to decoder.

- Transformers = Seq2Seq with Attention BUT instead of updating hidden state via sequential processing of input sequence, Attention layer is implemented such that the input sequence can be processed in one go and parallelizable on GPU. Transformer also allows for attention amongst input, attention amongst output and attention between the two.

## ✅ Resume Check-Up

### **Overall Strategy**
- [ ] Focus on your most impressive **achievements**, not just a list of responsibilities. Use specific numbers and results to show your impact.  
- [ ] **Tailor your resume** for each job application by highlighting skills and experiences that align with the job description.  

### **Content**
- [ ] Start with your **strongest information first**. Your most relevant experience and skills should be at the top to immediately grab a recruiter's attention.  
- [ ] **Remove "fluff."** Get rid of vague or overused phrases like "hard-working" or "results-oriented." Instead, use action verbs and data to demonstrate these qualities.  
- [ ] Keep it concise. Generally, aim for **one page** unless you have extensive experience (more than 10–15 years) that is highly relevant to the role.  

### **Format and Polish**
- [ ] Make your **name, phone number, and email** clearly visible at the top.  
- [ ] **Do not include your mailing address** for privacy and security. A city and state is all that's needed.  
- [ ] **Include links** to your relevant online presence, such as your LinkedIn profile, GitHub, or personal portfolio.  
- [ ] **Hyperlink** to outside work or projects you've mentioned in your experience section.  
- [ ] **Save your resume as a PDF** with a professional file name, such as `FirstName-LastName-Resume.pdf`.  
