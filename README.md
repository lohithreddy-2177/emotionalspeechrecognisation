# emotionalspeechrecognisation
contents:
- dataset
- data preprocessing
- feature extraction
- exploratory data analysis
- model pipeline
- model evaluation


1) Data set:
     1)RAVDESS Speech Audio Dataset Overview:
     1st data set contains the speech files, which is created by 24-profestional actors, total of 1440 samples.
     Each actor had a folder name as Actor_XX, XX- the no.
     Each folder had the 60 different recordings -
      | Emotion    | Intensity | Statements | Repetitions | Total per Emotion  |
      | ---------- | --------- | ---------- | ----------- | ------------------ |
      | Neutral    | 1         | 2          | 2           | 4                  |
      | Others (7) | 2         | 2          | 2           | 8 × 7 = 56         |
      | **Total**  |           |            |             | 60 files/actor     |
      File Naming Format: Each audio file is encoded in a certain way, giving the entire info about the recording
      Pattern:
      03-01-EMO-INT-STMT-REP-ACTOR.wav
     Breakdown
     | Field | Example | Meaning                                    |
     | ----- | ------- | ------------------------------------------ |
     |  03   |   03    | Modality = Audio-only                      |
     |  01   |   01    | Vocal Channel = Speech                     |
     |  05   |   05    | Emotion = Angry                            |
     |  01   |   01    | Intensity = Normal                         |
     |  02   |   02    | Statement = “Dogs are sitting by the door” |
     |  01   |   01    | Repetition = First take                    |
     |  12   |   12    | Actor ID (even = female, odd = male)       |
     Emotion map:
     | Code | Emotion   |
     | ---- | --------- |
     | 01   | Neutral   |
     | 02   | Calm      |
     | 03   | Happy     |
     | 04   | Sad       |
     | 05   | Angry     |
     | 06   | Fearful   |
     | 07   | Disgust   |
     | 08   | Surprised |

     Only Neutral has one intensity (01); all others have both intensities (01 = normal, 02 = strong).
     Each statement appears with each emotion and intensity, recorded twice (repetition = 01 or 02)
     Statement code:
     | Code | Text                            |
     | ---- | ------------------------------- |
     |  01  | "Kids are talking by the door." |
     |  02  | "Dogs are sitting by the door." |
     2)RAVDESS Song Audio Dataset Overview (latest):
     The second part consists of song audio files, performed by 23 professional actors,contains a total of 1012 samples.
     Each actor has a dedicated folder named Actor_XX where XX is the actor number.
     Each folder contains 44 audio recordings, based on the combinations of emotion, intensity, statements, and repetitions.
     Breakdown of Recordings per Actor:
     | Emotion                   | Intensity Levels         | Statements | Repetitions | Total per Emotion       |
     | ------------------------- | ------------------------ | ---------- | ----------- | ----------------------- |
     | Angry                     | 2 (Normal, Strong)       | 2          | 2           | 8                       |
     | Fearful                   | 2                        | 2          | 2           | 8                       |
     | Disgust                   | 2                        | 2          | 2           | 8                       |
     | Surprised                 | 2                        | 2          | 2           | 8                       |
     | Total                     |                          |            |             | 4 emotions × 8 = **32** |
     | Neutral                   | Not present in song data | –          | –           | –                       |
     | Total files per actor     |                          |            |             | 44                      |
     File Naming Format:
     Just like the speech data, each audio file follows a structured naming convention that encodes metadata directly in the 
     filename:
     03-01-EMO-INT-STMT-REP-ACTOR.wav
     | Field | Example | Description                                   |
     | ----- | ------- | --------------------------------------------- |
     | 03    | 03      | Modality = Audio-only (song)                  |
     | 01    | 01      | Vocal Channel = Song                          |
     | 05    | 05      | Emotion = Angry                               |
     | 01    | 01      | Intensity = Normal (01 = normal, 02 = strong) |
     | 02    | 02      | Statement = "Dogs are sitting by the door"    |
     | 01    | 01      | Repetition = First take                       |
     | 12    | 12      | Actor ID (even = female, odd = male)          |
     Emotion Code Map:
     | Code | Emotion |
     | ---- | ------- |
     | 01   | Neutral |
     | 02   | Calm    |
     | 03   | Happy   |
     | 04   | Sad     |
     | 05   | Angry   |
     | 06   | Fearful |
     unlike the speech data set song contains only 6 emotions.
     Statement Code Map:
     | Code | Statement                       |
     | ---- | ------------------------------- |
     | 01   | "Kids are talking by the door." |
     | 02   | "Dogs are sitting by the door." |
2)Data preprocessing/ feature extraction:









     
     

     

     

      
