# TV-Script Generator

We design an LSTM based model and train it on the [Seinfeld dataset](https://www.kaggle.com/thec03u5/seinfeld-chronicles#scripts.csv) consisting of scripts of episodes from 9 seasons. We then use this model to generate our own TV-script. 

This project was part of Udacity's [Deep Learning nano-degree](https://www.udacity.com/course/deep-learning-nanodegree--nd101?utm_source=gsem_brand&utm_medium=ads_n&utm_campaign=8301633066_c&utm_term=85414324316_sa&utm_keyword=udacity%20deep%20learning_e&gclid=Cj0KCQjwjoH0BRD6ARIsAEWO9Dv3uK8C0VfpztIXAEL-p26nHZiFi03pF3mWVkZ-ZkJGbxGs0-I8d2AaApakEALw_wcB). 

Our model consisted of an initial embedding layer (emdedding dim = 500), followed by 3 LSTM layers (hidden_dim = 700) followed by 2 hidden linear layers (with 525 and 350 units respectively) and a final output layer which predicted to next word corresponding to a given sequence of words. Each linear layer was preceded by a BatchNoramlization layer. 

We trained this for 200 epochs. The project requirement was to achieve a loss lower than 3.5. We achieved this within the first 5 epochs of training, attaining a final loss of 1.92 after 200 epochs. This is significantly better than the goal established for project assessment. 


### Generated Script
Following is a sample of the script generated by our model:

jerry: which is like, y'know jumping from the inside, but the water was cold virtually... and if i hear it, i would eat it if you would have had said no one's ever seen that kind of effect around the top of a piece of *fruit* to save name.

kramer:(to mickey) hey, you watchin' oprah?

jerry: yeah, i know, but i know.

margaret: i mean someone knows what to do. i don't need to talk about it in your house if i had to.(george reluctantly laughs.)

carl: elaine, i can't believe the last time she came.

jerry: oh.

uncle leo: helloooo, will you ever start with me?

kramer: yeah, yeah...

olive: but you thought it was it? why'd you tell that guy?

kramer: he said i was gonna get a christmas card.

jerry: i don't have a washcloth though.

.
.
.


The full script generated by our model can be obtained from [this](generated_script_1.txt) file. Though the script doesn't make a lot of sense, but we can see that it has the structure of a script with alternating set of dialogues. Also, each diaglogue in itself also seems to have a good grammatical structure.  