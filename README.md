# Live image classifier project

This repository contains the image dataset and a browser demo for a Teachable Machine image classification project. The dataset has **200 photographs**, organized by contributor:

| Contributor | Folder | Images |
| --- | --- | ---: |
| Mel | [`dataset/Mel/class1/`](dataset/Mel/class1/) | 100 |
| Mia | [`dataset/Mia/class1/`](dataset/Mia/class1/) | 100 |

Mel's images came from two local folders (44 and 56 files); Mia's came from one folder (100 files). All 200 files were checked for exact duplicates, converted to JPEG for browser compatibility, and compressed for GitHub upload. The original photographs remain on the contributors' computer. Folder names identify who supplied each image; they **do not** claim that Mel and Mia are the model's class labels.

## Project background and contributions

The project explores image classification with Google's Teachable Machine and the limitations of small, human-curated datasets. Mel and Mia contributed the photographs listed above. The image subjects, capture conditions, model class definitions, training procedure, and evaluation results should be documented by the team once confirmed; no accuracy or demographic performance numbers are asserted here.

## Model and demo

The published [Teachable Machine image model](https://teachablemachine.withgoogle.com/models/1rbbm3v-y/) has three classes named **Esther**, **Picnic**, and **Chewy**. In the training interface, these classes currently show 104, 85, and 53 image samples respectively. These are model training sample counts; they are separate from the 200 contributor-organized photographs uploaded to this repository.

Open the [live demo](https://mel000618.github.io/mel-LIS500-ML/) in a modern browser and select **Start camera** to test live predictions. Camera access requires permission. The page displays class probabilities from the published model. A demonstration-video URL has not yet been supplied, so the page labels that section as pending.

For local serving, a simple static HTTP server is enough: from the repository root run `python3 -m http.server 8000` and visit `http://localhost:8000`. No build step is required. The page loads TensorFlow.js and the Teachable Machine image library from a CDN, so an internet connection is required. A published Teachable Machine image model must provide `model.json` and `metadata.json` at its URL.

## Data collection and ethics

This is a contributor-organized corpus, not a validated benchmark. The source folders provided 100 files per person, and no exact file duplicates were found. The photos may still contain near-duplicates, correlated backgrounds, or uneven lighting. Evaluate a trained model on images withheld from training and report results separately for relevant conditions rather than assuming that a high overall score represents reliable behavior. See the discussion in [`index.html`](index.html).

## Remaining project materials

- Add a 1–2 minute screen recording that shows live predictions, then link to its YouTube or Vimeo page.
- If the assignment requires three contributors and 300 photos, add the third contributor's 100 original photos. This repository currently contains only Mel's and Mia's sets.
