# Docker base image for TensorFlow Serving

## Run TF-Serving
```bash
docker pull codecentric/tensorflow-serving-baseimage

docker run -p 8501:8501 \
  -p 8500:8500 \
  --mount type=bind,source=$(pwd)/models/fruits/,target=/models/fruits \
  -e MODEL_NAME=fruits -t tensorflow/serving:1.10.1
```
