# GISLR
 Google - Isolated Sign Language Recognition - Kaggle Competition

Competion link - [GISLR](https://www.kaggle.com/competitions/asl-signs)

+ Observation from discussions :
  - different number of frames for each sign (can be anything like 12 or 45 or 89)
  + as instruction while generating data was to use single hand , so either left hand or right hand is NA for most sequence
  - instead of around 543 mediapipe landmarks most of the 480 face landmarks are useless and use only some important face landmarks such as lips , boundary of face , [mediapipe site](https://google.github.io/mediapipe/solutions/face_mesh.html)
  
- Models that I will try :
  + DNN Baseline - firstly will try Fully Connected NN with input of frame length ~ 20 , and taking only major landmarks and duplicating LH/RH points from the other hand if itself is NA
  - Transformer Baseline - Will try transformer next as it can take vaiable number of frames and also will be positive for our sequential data
  + Can try variations where each type(face , pose , hand) data is first represented to some latent z via respective encoders and then fed to RNNs.
  
  
  
