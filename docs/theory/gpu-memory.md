# GPU와 메모리

## 모델을 GPU에 올린다는 것

학습이 끝난 모델의 **가중치(weight)를 포함한 모델 레이어를 GPU VRAM에 배치하고 GPU에서 연산**하도록 하는 것이다.

`LlamaCpp` 계열에서:

```python
n_gpu_layers = -1
```

은 가능한 모델 레이어를 최대한 GPU로 offload하려는 설정이다.

## RAM과 VRAM

일반 PC 예:

- 시스템 RAM 32GB → 주로 CPU가 사용
- NVIDIA GPU VRAM 8/16/24GB → GPU가 사용

모델이 VRAM에 다 들어가지 않으면 일부는 시스템 RAM/CPU 쪽에 남겨 CPU+GPU 혼합 실행을 할 수 있다.

## HBM

HBM = High Bandwidth Memory.

AI 서버용 GPU/가속기에서 많이 사용하는 고대역폭 메모리다.

HBM은 NVIDIA 전용이 아니다. NVIDIA GPU뿐 아니라 AMD GPU, Google TPU, AWS Trainium 같은 AI 가속기에서도 사용할 수 있다.

AI에서 메모리가 병목이 되는 핵심 이유 중 하나는 **GPU가 대량의 모델 weight를 계속 빠르게 읽어야 하기 때문**이다.
