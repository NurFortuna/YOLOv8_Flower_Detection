## YOLOv8 Object Detection on a Custom Dataset ##
### Flower Detection ###

[Data](https://universe.roboflow.com/my-datasets-0aq8j/flower-46h98/dataset/2)

YOLOv8 is the latest installment in the highly influential family of models that use the YOLO (You Only Look Once) architecture. YOLOv8 was developed by Ultralytics, a team known for its work on YOLOv3 and YOLOv5.

Following the trend set by  YOLOv6 and YOLOv7, we have at our disposal object detection, but also instance segmentation, and image classification. The model itself is created in PyTorch and runs on both the CPU and GPU. As with YOLOv5, we also have a number of various exports such as TF.js or CoreML.[1]


### The New YOLOv8 API ###

The developers of YOLOv8 decided to break away from the standard YOLO project design : separate train.py, detect.py, val.py, and export.py scripts. In the short term it will probably cause some confusion while in the long term, it is a fantastic decision!

This pattern has been around since YOLOv3, and every YOLO iteration has replicated it. It was relatively simple to understand but notoriously challenging to deploy especially in real-time processing and tracking scenarios.

The new approach is much more flexible because it allows YOLOv8 to be used independently through the terminal, as well as being part of a complex computer vision application.[1]

One way to download a dataset from Roboflow Universe is to use our pip package. You can generate the appropriate code snippet directly in our UI.

```
from roboflow import Roboflow

rf = Roboflow(api_key='YOUR_API_KEY')
project = rf.workspace('WORKSPACE').project('PROJECT')
dataset = project.version(1).download('yolov8')

```

[1](https://blog.roboflow.com/how-to-train-yolov8-on-a-custom-dataset/)
