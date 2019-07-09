# PADet

## Main Results

|          | Backbone   | Training    | Testing  | Input     | FPS  | mAP  | mAP@0.5 | mAP@0.75 | mAP@S | mAP@M | mAP@L |
| -------- | ---------- | ----------- | -------- | -------------- | ---- | ---- | ------- | -------- | ----- | ----- | ----- |
| Ours_384 | VGG-16     | trainval35k | test-dev | 384×384 | 62.5 | 35.2 | 55.9    | 38.1     | 17.7  | 38.2  | 48.3  |
| Ours_512 | VGG-16     | trainval35k | test-dev | 512×512 | 38.5 | 37.6 | 58.7    | 41.0     | 21.0  | 40.4  | 49.5  |
| Ours_384 | ResNet-101 | trainval35k | test-dev | 384×384 | 40.0 | 36.9 | 57.0    | 40.2     | 16.4  | 40.4  | 53.3  |
| Ours_512 | ResNet-101 | trainval35k | test-dev | 512×512 | 28.6 | 40.0 | 60.8    | 43.8     | 21.3  | 43.9  | 53.9  |
#### Notes

- Results of our models on *minival* set are 34.8, 37.6, 36.7, 39.6 respectively.
- The above results are obtained by single-scale training and testing without adopting scale-jitter training and inference augmentation (e.g., multi-scale, flip, voting)
- The runtime are measured on our local machine with single NVIDIA GTX 1080 Ti, i7-6850k CPU, pyTorch 0.4.1, CUDA 9.0 and cuDNN v7.0. Different configures may induce various runtime.
- We have updated the runtime of Ours_384 with ResNet-101 since the data of last commit 42ab085(https://github.com/zxhr2793/PADet/commit/42ab085fd1c2b067d5adcc3f3e04688dc70fbdc9) was obtained when the gpu was busy. 

## Comparison to other state-of-arts

<img src='images\results.png' width='800'>

## Speed/Accuracy trade-off

<img src='images\speed.png' width='800'>

#### Notes

- **V** means the backbone of VGG-16 and **R** is ResNet-101.

## Todo
- [ ] Release the evaluation codes and models
- [ ] Release the training codes
