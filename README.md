#### 얼굴 인식 모델(<span style="color:blue">face-detection-adas-0001</span>)에 대해서 [여기](https://docs.openvino.ai/2022.1/omz_models_model_face_detection_adas_0001.html)에서 알아봅니다.

<img src="https://docs.openvino.ai/2022.1/_images/face-detection-adas-0001.png" style="width:400px; float:left;" />
<div style="clear:both;"></div>

네트워크(모델)는 모양이 [1, 1, N, 7] 인 blob을 출력합니다. <br>
여기서 N은 감지 된 경계 상자의 수입니다. 각 탐지에 대해 설명은 다음과 같은 형식을 갖습니다.<br>
<b>[image_id, label, conf, x_min, y_min, x_max, y_max]

A very basic introduction to using face detection models with OpenVINO™ 

The [Model/face-detection-adas-0001](https://github.com/openvinotoolkit/open_model_zoo/blob/master/models/intel/face-detection-adas-0001/README.md) model from [Open Model Zoo](https://github.com/openvinotoolkit/open_model_zoo/) is used. It detects faces in images and returns a blob of data 

with shape: `1, 1, 200, 7` in the format `1, 1, N, 7`, where `N` is the number of detected
bounding boxes. The results are sorted by confidence in decreasing order. Each detection has the format
[`image_id`, `label`, `conf`, `x_min`, `y_min`, `x_max`, `y_max`], where:

- `image_id` - ID of the image in the batch
- `label` - predicted class ID (1 - face)
- `conf` - confidence for the predicted class
- (`x_min`, `y_min`) - coordinates of the top left bounding box corner
- (`x_max`, `y_max`) - coordinates of the bottom right bounding box corner
