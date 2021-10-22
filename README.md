# OpenCV
**컴퓨터 비전 분야**는 사람이 시각 정보를 입력값으로 하여 행동하기 이전에 생각하고 판단하는 부분을 컴퓨터가 대신하도록 하는 학문이다.

쉽게 말해 인공지능이라고 할 수 있고 다만, **시각적인 입력 데이터**, 즉 **영상**을 주로 다룬다는 것이 차이점이다.

OpenCV는 Computer Vision 관련 프로그래밍을 쉽게 할 수 있도록 도와주는 Open Library

영상처리, 3D 구성, 추적, 기계학습, 인식 그리고 딥러닝까지 유용한 기능이 많다.

## 환경 설정

Window7 이상

64bit

OpenCV 3.2

- https://github.com/opencv/opencv
- 현재 기준 최신 버전으로 받는다.(21.10.21)

Cuda Toolkit 8.0

- https://developer.nvidia.com/cuda-downloads
- 

CMake 3.8.0

- 대표적인 C/C++ 프로젝트 빌드(Build) 도구
- https://cmake.org/download/
- 현재 기준 최신 버전으로 받는다.(21.10.21)

TBB 2017

- Threading Building Blocks
- Intel에서 만든 다중 코어, 멀티 쓰레드 라이브러리
- 용량 데이터인 영상을 처리할 때 여러 개의 쓰레드를 사용하여 연산을 좀 더 빠르게 수행할 수 있게 해주는 역할
- TBB를 꼭 설치해야 하나? -  https://kkokkal.tistory.com/1301