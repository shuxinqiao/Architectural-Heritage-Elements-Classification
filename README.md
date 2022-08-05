# Architectural Heritage Elements Classification

Image Classification Model using Pytorch pretrained Residual ConvNet 18 and 50 Layers Model for Transfer Learning.

## Data Summary

- .jpg format
- 64 px x 64 px (Height x Width)


| Class | Train Number | Test Number |
| --- | --- | --- |
| altar | 828 | 140 |
| apse | 505 | 50 |
| bell tower | 1057 | 170 |
| column | 1914 | 210 |
| dome (inner) | 589 | 69 |
| dome (outer) | 1175 | 142 |
| flying buttress | 405 | 70 |
| gargoyle | 1562 | 240 |
| stained glass | 998 | 150 |
| vault | 1097 | 163 |
| **Total** | 10130 | 1404 |



## Results

Loss by CrossEntropyLoss function.  Data normalized in 3 color channels.

Model | Train Loss | Train Acc | Val Loss | Val Acc | Test Acc | Train Time | 
--- | --- | --- | --- |--- |--- |---
ResNet18 (fine tuning) | 0.0391 | 0.9911 | 0.3086 | 0.9207 | 0.9017 | 128m 11s |
ResNet50 (fine tuning) | 0.0486 | 0.9872 | 0.0214 | 0.9951 | 0.9323 | 86m 16s |
ResNet50 (fixed feature) | 0.6233 | 0.7885 | 0.4795 | 0.8387 | 0.7756 | 56m 20s |


Fine Tuning and Fixed Feature Extractor ResNet 50 used `mosaicml/composer` for efficient training.


### Training images
![Training images](/ScreenShots/InputSample.PNG)

### Single Test Images
![Single Test Images](/ScreenShots/OutputSample.PNG)



## Usage/Examples

Put images into dataset/SingleTest/ and run SingleTest.ipynb last section to get predictions. 

Image must be .jpg format.

Few online image examples are in SingleTest.



## Library Versions

- python: `3.10.5`
- torch: `1.12.0`
- torchvision: `0.13.0`
- numpy: `1.23.1`
- matplotlib: `3.5.2`
- mosaicml: `0.8.0`
