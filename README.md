# Data collection and ethics

This repository contains the image dataset and a browser demo for a Teachable Machine image classification project. The dataset has **200 photographs**, organized by contributor:

| Contributor | Folder | Images |
| --- | --- | ---: |
| Mel | [`dataset/Mel/class1/`](dataset/Mel/class1/) | 100 |
| Mia | [`dataset/Mia/class1/`](dataset/Mia/class1/) | 100 |

Mel also contributed [**46 additional No cat photos**](dataset/no-cat/Mel/) for the second iteration.

## 1. Project background and contributions

This project explores how image classification could help a multi-cat household serve each cat the right food. Esther eats weight-management food, Chewy eats hairball-control food, and Picnic eats kitten food. In our proposed system, a camera on an automatic feeder would identify the cat at the bowl and dispense that cat's assigned food, helping prevent the cats from eating one another's meals.

Mel and Mia each contributed 100 photographs, as shown above. The folders identify the contributors; the model's classes identify Esther, Picnic, and Chewy. Another household could adapt the idea by collecting photos of its own pets, retraining and testing the model, and setting a food assignment for each pet.

## 2. Model and demo

We use a three-class [Teachable Machine image model](https://teachablemachine.withgoogle.com/models/1rbbm3v-y/) that predicts whether a camera image shows Esther, Picnic, or Chewy. The [public demo webpage](https://mel000618.github.io/mel-LIS500-ML/) shows the three cats, their assigned foods, live predictions, and a [demonstration video](https://mel000618.github.io/mel-LIS500-ML/#video-title). Select **Start camera** and allow camera access to try the classifier. The displayed scores show the model's predictions, not certainty.

The webpage does not connect to or control an automatic feeder. A real feeder would also need a safe way to handle uncertain predictions, multiple cats in view, and failures of the camera or model.

## 3. Data collection and ethics

The original 200 cat photos are organized by contributor, while the model training samples are organized by cat. Those are different groupings and should not be treated as the same counts. The photos may include similar backgrounds, repeated poses, uneven lighting, and other patterns that make a model appear more accurate than it would be on new images.

Before using this idea to dispense food, we would need to test it on photos withheld from training and under varied lighting, camera angles, and feeding conditions. A wrong prediction could give a cat food intended for another cat, so the current classifier should not make feeding decisions by itself. The people who collected and labeled the images chose what the model could see; those choices shape its limits. Any new household would need its own representative photos and careful testing. Pet photos should be shared with the owners' permission, especially when they reveal details of a private home.
