# Multimodal Annotation for Virtual Meeting Summarization

In this repository we provide the annotations for the paper “Multimodal Annotation for Virtual Meeting Summarization”.

The data folder contains the train, test and val (*.json) files with the annotations. The video_id in the json files can be mapped to the original dataset videos. These mappings are provided in the video_id_mappings folder. Due to copyright issues, we are unable to provide the original video data, however you can contact the authors to download it, inline with their terms and agreement.

├── data
│   ├── test.json
│   ├── train.json
│   └── val.json
└── video_id_mappings
    ├── video_id_mappings_test.txt
    ├── video_id_mappings_train.txt
    └── video_id_mappings_val.txt


 ├── data
     └── BLiSS
         ├── annotation
         ├── feature
     └── CNN
         ├── annotation
         ├── feature
     └── Daily_Mail
         ├── annotation
         ├── feature
     └── SumMe
         ├── caption
         ├── feature
         ├── splits.yml
     └── TVSum
         ├── caption
         ├── feature
         ├── splits.yml
