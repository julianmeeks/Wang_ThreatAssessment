# A layered, hybrid machine learning analytic workflow for mouse risk assessment behavior
Repository for data and code for Jinxin Wang et al. (Meeks Laboratory) 2022

## Project overview
Accurate and efficient quantification of animal behavior has multiple benefits in the quest to understanding the workings of the brain. An emerging approach within the rapidly developing machine learning (ML) field is to combine multiple ML-based algorithms to support automated quantification of animal behavior from video recordings. These so-called hybrid models have emerged because of limitations associated with supervised (e.g., random forest, RF) and unsupervised (e.g., hidden Markov model, HMM) ML classifiers. For example, RF models lack an explicit accounting for temporal relationships across video frames, and HMM latent states are often difficult to interpret. We set out to develop a hybrid model that integrates aspects of RF and HMM models, and did so in the context of a study of threat assessment to predatory odors (e.g., reptile feces or fecal extracts, trimethylthiazoline). We utilized DeepLabCut to estimate the positions of mouse body parts. Positional features were calculated using DeepLabCut outputs and were used to train RF and HMM models with equal number of states, separately. The per-frame predictions from RF and HMM models were then passed to a second HMM model layer (“reHMM”). The outputs of the reHMM layer showed improved interpretability over the initial HMM output, and improved the capacity to analyze temporal aspects of behavior. Finally, we combined predictions from RF and HMM models with selected positional features to train a third-layer HMM model (“reHMM+”). This reHMM+ three-layer hybrid model unveiled distinctive temporal and high human-interoperable behavioral patterns that mice displayed in the presence of predator odors. For workflow application, we uncovered detailed and dynamic mouse behavioral patterns in the presence of fearful odor TMT and enhanced mouse risk assessment behavior induced by snake feces odor. We conclude that this layered, hybrid machine learning workflow represents a balanced approach for improving the depth and reliability of ML classifiers in chemosensory and other behavioral contexts. 


## Ethogram
<img src="https://user-images.githubusercontent.com/44708430/173367509-6f340263-e1aa-4755-b531-bed88ca3d673.jpg" width="800" height="340">


## Architecture of analytic workflow
<img src="https://user-images.githubusercontent.com/44708430/173366117-8ef10f3c-3111-4575-858c-61edd0d85475.png" width="1000" height="240">

