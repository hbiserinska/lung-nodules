# nodules
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
