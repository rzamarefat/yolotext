<div align="center">
  <h2>
    YOLOText: A Packaged version of YOLOv8 for synthetic and natural scene text detection  
  </h2>
</div>

### Sample Results
![PPP_3](https://github.com/rzamarefat/YOLOv8_Text_Detection/assets/79300456/84d08057-8c6b-4a14-ae91-dc2fe6005589)

### Installation
```
pip install yolotext
```

### Usage
```python
from glob import glob
import cv2
from yolotext import Yolov8TextDetection
images = [cv2.imread(p) for p in sorted(glob(r"C:\Users\ASUS\Desktop\github_projects\YOLOv8_Text_Detection\images\*.jpg"))]

detector = Yolov8TextDetection(device="cuda")
polylines = detector.detect(images)
drawn_images = detector.visualize_polylines(images, polylines)
for d in drawn_images:
        cv2.imshow("Image", d)
        cv2.waitKey(0)
    cv2.destroyAllWindows()
```

