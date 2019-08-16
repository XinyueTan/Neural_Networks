# Neural Networks
<img src="https://user-images.githubusercontent.com/46146748/63178520-34420200-c018-11e9-8f9f-183da398376f.jpg" width="600">

## Goal of the analysis

In this project, I will be explaining the utility of artificial networks and building a neural network to predict student attentional state from webcam imags. 

In the attached data sets **attention1.csv** and **attention2.csv**, there is data that describe features assocaited with webcam images of 100 students' faces as they particpate in an online discussion. The variables are:

  * eyes - student has their eyes open (1 = yes, 0 = no)
  * face.forward - student is facing the camera (1 = yes, 0 = no)
  * chin.up - student's chin is raised above 45 degrees (1 = yes, 0 = no)
  * attention - whether the student was paying attention when asked (1 = yes, 0 = no)

I will use the webcam data to build a neural net to predict whether or not a student is attending. The accuracy of the neural net is also caculated in the end of the RMarkDown file.

## Packages Required
``` 
install.packages("neuralnet")
install.packages("dplyr")
```

## Procedures
1. Load both **attention1.csv** and **attention2.csv** data sets
2. Build a neural net that predicts attention based on webcam images by using neuralnet package
3. Increase the number of hidden layers in the neural net and build a second neural net with more layers in it
4. Use the preferred neural net to predict both the first (train data set) and the second data set (test data set)
5. Caculate the accuracy of the prediction

## Visualizations
### Neural Network with Three Hidden Layers
<img src="https://user-images.githubusercontent.com/46146748/63179238-af57e800-c019-11e9-93d1-e9d6f5c64efa.PNG"" width="600">

The command "neuralnet" sets up the model. It is composed of four basic arguments:

- A formula that describes the inputs and outputs of the neural net (attention is our output)
- The data frame that the model will use
- How many hidden layers are in our neural net
- A threshold that tells the model when to stop adjusting weights to find a better fit. If error does not change more than the threshold from one iteration to the next, the algorithm will stop (We will use 0.01, so if prediction error does not change by more than 1% from one iteration to the next the algorithm will halt)


## Background
**Neural networks** are not a new method, the first artificial neural network was devised in 1943, but advances in computational power and speed have made them a much more viable strategy for solving complex problems over the last 5-10 years. Originally devised by mathmaticians and neuroscientists to illustrate the fundamental principles of how brains might work they lost favor in the second half of the 20th century only to surge in popularity in the 20-teens as software engineers used them to resolve mathmatically intractable problems. 

Nowadays, audio recognition (e.g.: google translate), handwriting recognition (e.g.:banks to process cheques, post offices to recognize addresses) and segmentation (e.g.: classify pictures of dogs or cats) are all implications of neural network in the real life.

The application of neural networks to learning problems has been ongoing for 20 years, often to predict student behvior or to parse unstructured data such as student writing samples and provide natural sounding feedback through AI avatars.


##  Related Readings

[Nielsen, M. (2015). Neural Networks & Deep Learning. Determination Press:San Francisco, CA]
  [Chapter 1](http://neuralnetworksanddeeplearning.com/chap1.html)  
  [Charpter 2](http://neuralnetworksanddeeplearning.com/chap2.html)  

[McKlin, T., Harmon, S. W., Evans, W., & Jones, M. G. (2001). Cognitive presence in Web-based learning: A content analysis of students' online discussions.](https://files.eric.ed.gov/fulltext/ED470101.pdf)  

[Lewis-Kraus, G. (2016). The Great AI Awakening. The New York Times: New York, NY](https://www.nytimes.com/2016/12/14/magazine/the-great-ai-awakening.html)

[Roberts, E. (2000). History in Neural Networks. Stanford University: Palo Alto, CA](https://cs.stanford.edu/people/eroberts/courses/soco/projects/neural-networks/History/history1.html)


For more detail:  
[Stergiou, C. & Siganos, D. (2000). Neural Networks.](http://www.doc.ic.ac.uk/~nd/surprise_96/journal/vol4/cs11/report.html)

[Hartnett, K. (2019). Foundations Built for a General Theory of Neural Networks](https://www.quantamagazine.org/foundations-built-for-a-general-theory-of-neural-networks-20190131/)


## Related Videos

[Sanderson, G. (2017). But what *is* a Neural Network? 3Blue1Brown. ](https://www.youtube.com/watch?v=aircAruvnKk)

[Grey, C.G.P. (2017). How Machines Learn.](https://www.youtube.com/watch?v=R9OHn5ZF4Uo)

[Bling, S. (2017). MariFlow - Self-Driving Mario Kart with Recurrent Neural Network](https://www.youtube.com/watch?v=Ipi40cb_RsI)


## Author
[Katherine Tan](www.linkedin.com/in/katherine-tan-2019), M.S student in Learning Analytics at Teachers College, Columbia University
