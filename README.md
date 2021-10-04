# Lane-line-detection
Lane line detection based on improved semantic segmentation in complex road environment
## Keywords: smart city; autonomous driving; complex road environment; lane line detection; semantic segmentation
To enable the constructed VGG-SS network model to accurately detect and extract lane line semantic information under complex road conditions, this paper uses the CULane dataset to train the VGG-SS network, and by training the network model, it is able to have to strong feature extraction capability.
Dataset	Total	Training set	Validation set	Test set	Pixel	Environment	Source	Evaluation Indicators
TuSimple	6,408	3,268	358	2,782	1280 x 720	Expressway	Santiago	Accuracy
CULane	133,235	88,880	9,675	34,680	1640 x 590	Urban Expressway rural	Beijing	F1Score /IOU
The CULane dataset used in this chapter contains a total of 133,235 images. The CULane dataset covers data from nine scenes including common scenes, crowded scenes and night scenes, and the proportion of each scene is shown in the figure.
![图片](https://user-images.githubusercontent.com/69465888/135834534-3f76821a-e468-4a5d-8b2e-22ff78ae2cd6.png)
The network model was trained and tested on a computer with an NVIDIA 1080Ti graphics processor, 8GB of video memory and a Windows 10 operating system. The entire algorithm was developed and trained based on the Python3 language and TensorFlow deep learning framework platform under Windows 10 operating system.
Property	Parameter
Dataset	CULane
Input Image Size	800×290
Initial Learning Rate	0.001
Power	0.9
Batch Size	10
Weight Decay	0.0001
Iteration Number	60000
In order to solve the problem of low detection accuracy in complex road scenarios where lane lines are often worn and obscured, this section proposes an improved semantic segmentation-based lane line detection method, mainly using the SAD and SCNN modules to optimise the "encoder-decoder" network structure based on the improved VGG-16. The proposed VGG-SS model has been extensively trained on the CUlane dataset, and has been compared with current semantic segmentation networks for several sets of experiments. However, when faced with complex road conditions, the accuracy of the VGG-SS model for lane line detection also decreases, but its detection accuracy can still reach 82.6, which is significantly higher than the current semantic segmentation model with better detection effect, proving that the improved method proposed in this paper can improve the detection accuracy of the model for lane lines.
