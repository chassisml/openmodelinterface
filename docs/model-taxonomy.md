# A Proposed Taxonomy of ML Model Output Formats
This list of algorithm types will be used as a basis for recommending standard output formats within the OMI specification.

## Audio
### Audio classification
### Emotion segmentation
### Speaker diarization
### Transcription per region
### Transcription whole audio

## Imagery
### Image classification
Example `json` output
```json
{
   "classPredictions":[
      {
         "class":"Image Class 1",
         "score":0.8
      },
      {
         "class":"Image Class 2",
         "score":0.1
      },
      {
         "class":"Image Class 3",
         "score":0.05
      },
      {
         "class":"Image Class 4",
         "score":0.025
      },
      {
         "class":"Image Class 5",
         "score":0.0125
      }
   ]
}
```

### Bbox object detection
### Brush segmentation
### Circular object detector
### Keypoints and landmarks
### Polygon segmentation
### Multi-image classification

## Text
### Text classification
Example `json` output
```json
{
   "classPredictions":[
      {
         "class":"eng",
         "score":0.19990852235440365
      }
   ]
}
```

### Multi classification
### Named entity recognition
### Text summarization
### Word alignment
### Text translation

## Code
### HTML classification
### HTML NER tagging
### Dialogs & conversations
### Rate PDF
### Rate website
### Video classifier

## Time Series
### Time Series classification
### Segmentation extended
### Multi-step annotation

## Classical ML
### Linear regression
### Logistic regression
### Decision tree
### Support vector machines
### Naive Bayes
### K-Nearest neighber
### K-Means clustering
### Random forest
### Dimensionality reduction algorithms
### Gradient boosting

## Other
### Conditional classification
### Three level classification
### Two level classification
### Pairwise comparison
### Relations among entities
### Video timeline segmentation
### Audio regions classification
### Image bboxes classification
### Text spans classification
