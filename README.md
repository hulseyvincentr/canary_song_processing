Discussion w. George on how to create song filter for .wav files:
1. Extract the song by removing empty space by using George's song_extractor from :https://github.com/georgevenven/ZebraFinch_VAE_Rotation_1/blob/main/song_extractor.ipynb (this takes all noise ever, and removes the silence). This removes all amplitude below a threshold (in a clever way - using convolution). 
	1. Option: combine all the stuff into one mega .npy file (numpy array file)
2. On the extracted songs, create the rhythmicity by using rhythmicity.ipynb on all of the extracted songs  (needs to be modified to work on spectrogram .png/image files). This takes a spectrogram of the power envelope, and gives a bunch of images of the spectrogram of the power envelope. 
	1. To do: combine into one mega file (.npy file)
	2. This gives us the rhythmicity: syllables of different time lengths of syllables = frequency, so syllable a = sin(f1*x), syllable b = sin(f2*x)
3. UMAP the rhythmicity. The songs will be in one cluster, and you make a "bounding box" that removes all data from outside of the box. Use https://github.com/georgevenven/ZebraFinch_VAE_Rotation_1/blob/main/vae.ipynb 

George and I have created a new GitHub repo here, which we will use to coordinate this: https://github.com/hulseyvincentr/canary_song_processing 