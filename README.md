# Live image classifier project

This repository contains the image dataset and a browser demo for a Teachable Machine image classification project. The dataset has **200 photographs**, organized by contributor:

| Contributor | Folder | Images |
| --- | --- | ---: |
| Mel | [`dataset/Mel/class1/`](dataset/Mel/class1/) | 100 |
| Mia | [`dataset/Mia/class1/`](dataset/Mia/class1/) | 100 |


## Project background and contributions

The project explores image classification with Google's Teachable Machine and the limitations of small, human-curated datasets. Mel and Mia contributed the photographs listed above. Both of us are responsible for the image subjects, model class definitions, training procedure, and evaluation results.

## Model and demo

The published [Teachable Machine image model](https://teachablemachine.withgoogle.com/models/1rbbm3v-y/) has three classes named **Esther**, **Picnic**, and **Chewy**. In the training interface, these classes currently show 104, 85, and 53 image samples respectively. These are model training sample counts; they are separate from the 200 contributor-organized photographs uploaded to this repository.

Open the [live demo](https://mel000618.github.io/mel-LIS500-ML/) in a modern browser and select **Start camera** to test live predictions. Camera access requires permission. The page displays class probabilities from the published model. 



## Data collection and ethics

This is a contributor-organized corpus. The source folders provided 100 files per person, and no exact file duplicates were found. The photos may still contain near-duplicates, correlated backgrounds, or uneven lighting. Evaluate a trained model on images withheld from training and report results separately for relevant conditions rather than assuming that a high overall score represents reliable behavior. See the discussion in [`index.html`](index.html).


