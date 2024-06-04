# Multimodal Annotation for Virtual Meeting Summarization

In this repository we provide the annotations for the paper “Multimodal Annotation for Virtual Meeting Summarization”.

The [`data`](https://github.com/skotey/vidchatsum/tree/main/data) folder contains the train, test and val (*.json) files with the annotations. The video_id in the json files can be mapped to the original dataset videos. These mappings are provided in the [`video_id_mappings`](https://github.com/skotey/vidchatsum/tree/main/video_id_mappings) folder. Due to copyright issues, we are unable to provide the original video data, however you can contact the authors of the [`Candor dataset`](https://betterup-data-requests.herokuapp.com/)to download it, inline with their terms and agreement.


## Data Annotations

```plaintext

├── data
│   ├── test.json
│   ├── train.json
│   └── val.json
└── video_id_mappings
    ├── video_id_mappings_test.txt
    ├── video_id_mappings_train.txt
    └── video_id_mappings_val.txt


## Feature Extraction

**Linguistics:**
Process the ASR time-stamped words to generate the sentence segments. The sentences are divided by a gap of 200 ms. Tokenize the segments using [Roberta`](https://huggingface.co/FacebookAI/roberta-base). To create the entity labels, use [spaCy’s](https://spacy.io) entity recognition library. 

**Aural**
To extract the acoustic word embeddings for the audio feature [Hubert] (https://huggingface.co/facebook/hubert-base-ls960) is utilized. Also pitch variance data is extracted using the [TorchCrepe](https://pypi.org/project/torchcrepe/) library.

**Visual**
Video extracted can be extracted using a pre-trained [CLIP](https://huggingface.co/openai/clip-vit-base-patch32) model. This [repository](https://v-iashin.github.io/video_features/models/clip/) is recommend for use. To extract hand gesture information, [MediaPipe](https://github.com/google-ai-edge/mediapipe) can be used. 
