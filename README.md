# Architectural Heritage Elements Classification

Classification Model using Pytorch pretrained Residual ConvNet 18 Layers Model.


## Results

Loss by CrossEntropyLoss function.  Data normalized in 3 color channels.

Model | Train Loss | Traing Acc | Val Loss | Val Acc | Test Acc | Train Time | 
--- | --- | --- | --- |--- |--- |---
ResNet18 + FC | 0.0391 | 0.9911 | 0.3086 | 0.9207 | 0.9017 | 128m 11s |

### Training images
![Training images](/ScreenShots/InputSample.PNG)

### Single Test Images
![Single Test Images](/ScreenShots/OutputSample.PNG)


## Usage/Examples

Put images into dataset/SingleTest/ and run SingleTest.ipynb last section to get predictions. 

Image must be .jpg format.

Few online image examples are in SingleTest.
