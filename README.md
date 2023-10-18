# NoteNinja

## Introduction
This project delves into the utilization of variational autoencoders to facilitate audio genre interpolation and music generation. The primary objective is to develop an interactive tool capable of transforming the genre of the original audio file into a genre preferred by the user. This will be achieved through an interpolation process within the latent space, ultimately producing an audio output aligned with the user's genre selection.

### Deliverables
A short writeup explaining the project with screenshots 
Presentation slides
Code via GitHub repository

## Concept 
An interactive music genre conversion and generation tool using a variational autoencoder (VAE) model.

Assume you have a favorite song that you wish was in a different genre. For example, you may enjoy the melody of a pop song but wish it was written in the manner of a jazz song. You may quickly change a pop song to a jazz song using our tool. The application will then create a new song in jazz style while keeping the original tune. 

### Applications

Music producers can use this tool to develop fresh music ideas or to transform music from one genre to another. Music educators can use it to teach students about music theory and composition, while music therapists can use it to create personalized music for their patients.

## Process

The GTZAN dataset contains music tracks from 10 different genres: blues, classical, country, disco, hip-hop, jazz, metal, pop, reggae, and rock. We used this dataset to train a variational autoencoder (VAE) model to generate music in different genres. To understand the concept of VAEs, we went through Chapter 3 of the book ‘Generational Deep Learning’ 2nd edition by David Foster. Foster is using the autoencoder to compress the audio, but we used it to interpolate between the features instead (thus interpolating between the genres).


First, we preprocessed the GTZAN dataset by converting the audio files to spectrograms. The system will take as input mp3 audio files across various genres. The VAE model encodes the audio into a latent space, which represents the underlying musical elements of the audio. Once the VAE model was trained, we used it to generate music in different genres. To do this, we first sampled a point from the latent space. Then, we decoded the latent space into a spectrogram. Finally, we converted the spectrogram back to audio. The model can be used to generate new audio from different points in the latent space, which will correspond to different genres of music.

## Challenges
Our present focus is on improving our outputs to assure sharper and clearer outcomes, even though our initial findings have produced results with controllable degrees of loss that are generally acceptable. We have discovered that noisy audio can result from fuzzy spectrograms, which has prompted us to give process improvement a higher priority in order to generate audio with more accuracy and quality.

## Next Steps

As a part of our next steps, our strategy involves enhancing the functionalities of our model to include the recognition of sheet music and the generation of extended sequences of audio. Additionally, we are aiming to delve into new areas, such as the creation of music with targeted tempos or moods. These developments will enable us to provide a more comprehensive and versatile musical experience for our users, catering to a broader range of preferences and requirements.
