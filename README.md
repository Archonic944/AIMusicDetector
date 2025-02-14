A machine learning model that determines if a song was generated with AI.

Chops the song into 1-second segments then feeds each segment to a TensorFlow/Keras sequential model with 5 convolutional blocks.
Final certainty for a song is determined by dividing segments evaluated as "AI" by the total number of segments in the song.

Instructions: Set the LOAD_MODEL flag to True to load the 21Jan2025.h5 file. Add cells at the end calling evaluate_independent_file() to evaluate your own music files. Run all cells.

## Validation statistics

The training set contained songs from Suno and Udio, whereas the validation set contained songs from numerous other AI generation services, such as LoudMe, Musichero, and Stable Audio.

The following is a scatterplot that shows "confidence ratings" for each song. A "confidence rating" is the percentage of segments in that song that were classified as AI-generated.

The cutoff for a song to be classified as AI is 60%. Given this cutoff, the model had an **83%** specificity and a **90%** sensitivity.

![image](https://github.com/user-attachments/assets/9b96d7c5-a5b4-4974-8ce9-35b6e49b309f)
