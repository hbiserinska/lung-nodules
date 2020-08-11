## YOLO v3 and v4 for Automatic Lung Nodules Detection from CT Scans
In this work, I propose an application of an object detection algorithm - You Only Look
Ones (YOLO) for lung nodules detection from Computed Tomography (CT) scans. YOLO
is a convolutional neuron network, pre-trained on ImageNet, and usually used for real-time
object detection. This application’s purpose is to provide a second opinion to radiologists when
analyzing CT scans. What distinguishes this work from existing research is its focus on the very
small nodules that are hard to detect. These nodules help to identify lung cancer in its early
stage when the cancer is most treatable. I experimented with 2 different architectures of YOLO
(version 3 and version 4) and 3 image enhancement pre-processing pipelines. The training was
performed with CT chest scans from a new dataset - Lung Nodule Database (LNDb) which was
introduced few months prior, and hence not widely used yet for development of lung nodule
detection algorithms. I showed that a model pre-trained on natural images can have promising
results when applied in the medical domain. The nodule detection with this single neural network
and the right contrast enhancement technique resulted in low false positives with reasonably high
sensitivity.

#### Access to the dataset can be requested from the following link: https://lndb.grand-challenge.org/

#### Project summary:
- ***flow_chart.png*** gives a visual overview of the project and the image enhencement techniques used.
- ***preprocessing.ipynb*** is handling with:
  - the initial **pre-processing** of the 3D CT scan images
  - extraction of the **image of interest** (containing the nodule's centroid)
  - application of the 3 pre-processing **image enhancement pipelines** and saving the resultant images as .jpg (input for the model)
  - preparing yolo compatible **label files** with the nodules coordinates
- ***yolo.ipynb*** explains the steps and runs the YOLO-v3 and YOLO-v4 repository by [AlexeyAB](https://github.com/AlexeyAB/darknet).
- ***folder yolo_files*** contains the yolo compatible files:
  - **obj.data** - file paths
  - **obj.names** - the name of the object we want to detect
  - **train.txt** - image name part of the train dataset
  - **text.txt** - image name part of the test dataset
  - **obj.zip** - label files with coordinates of the nodules
