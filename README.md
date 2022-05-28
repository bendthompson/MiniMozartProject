
# MiniMozart 🎼✍️

An RNN deep learning powered tool for writing melodies with the help of Mozart.

## Streamlit App
Hear example melodies and write your own using the model api. 

Try it! -[MiniMozart](https://cmp-web-7wc6zc723a-ew.a.run.app/)

## Skills I used/learned

🎹 Cleaned, transformed, and augmented 52 pieces of messy music data to 20,000 9-note sequences of pitch and duration for dataset

🎵 Used Keras to train Recurrent Neural Network models with LSTM and Dropout layers, trained with Early Stopping

🎸 Quickly self taught specialised music packages and software using available documentation

🎶 Built Docker virtual machines with specified environments and installed software dependencies

🎻 Built a complex frontend website with Streamlit, using statefulness and API connections to run smoothly

🎺 Hosted the model API and Streamlit in a Docker virtual machine on Google Cloud Platform with custom settings


## Data creation

Data created from MIDI files acquired from:
- the [Classical Music MIDI dataset](https://www.kaggle.com/soumikrakshit/classical-music-midi) from Kaggle
- the Music 21 library's MIDI corpus

Preparing the data for the model:
- melody extracted from the MIDI files
- saved values for pitch and duration for each note in the melody
- melody transposed to C major / A Minor
- removed uncommon rhythms and tuplets
- created 8-note-long sequences for X and the 9th note for y

## Model building
We created a multi-output deep learning model using Tensor Flow.  We used an LSTM for the first layer, before splitting into pitch and duration paths.  Each path had an LSTM layer, a dense layer, and a softmax output layer with dropout layers in between each.

## API
The API has two main functions:
- initialize: return an opening 8 note sequence at random from one of Mozart's piano sonatas.
- predict: using our model's predictions, suggest three notes (pitch / duration combinations) that are likely to come next in the sequence (according to Mozart)



## Authors

- [@sevans47](https://github.com/sevans47)
- [@bendthompson](https://github.com/bendthompson)
- [@Mizuki8783](https://github.com/Mizuki8783)
