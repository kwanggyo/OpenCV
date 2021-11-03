# OpenCV
**컴퓨터 비전 분야**는 사람이 시각 정보를 입력값으로 하여 행동하기 이전에 생각하고 판단하는 부분을 컴퓨터가 대신하도록 하는 학문이다.

쉽게 말해 인공지능이라고 할 수 있고 다만, **시각적인 입력 데이터**, 즉 **영상**을 주로 다룬다는 것이 차이점이다.

OpenCV는 Computer Vision 관련 프로그래밍을 쉽게 할 수 있도록 도와주는 Open Library

영상처리, 3D 구성, 추적, 기계학습, 인식 그리고 딥러닝까지 유용한 기능이 많다.

## 환경설정

💡 참고 : https://kali-live.tistory.com/4

Pycharm을 사용할 것이다.

File - Settings → Project:<프로젝트 이름> → Python Interpreter → +버튼 → opencv-python, opencv-contrib-python 검색 → Install Package(각각 Install)

설치 후 아래의 코드로 확인한다.

```python
import cv2
print(cv2.__version__)
```

## 함수

`cv2.imread(filename, flags)` : 영상파일(BMP,JPEG,PNG,TIFF 등)을 numpy.ndarray의 배열로 읽어 반환한다. → retval

`cv2.imwrite(filename,img)` : numpy.ndaaray의 배열 img를 filename의 영상파일로 저장한다. → retval

`cv2.namedWindow(winname,flag)` : winname을 갖는 윈도우를 생성한다.

`cv2.imshow(winname, img)` : img를 winname에 표시한다.

`cv2.witKey(delay)` : delay만큼(단위 : ms) 키보드 입력을 대기한다. → retval

`cv2.destroyWindow(winname)` : winname을 가진 윈도우를 종료한다.

`cv2.destoryAllWindows()` : 모든 윈도우를 종료한다.

- filename : 파일의 경로
- flags : 함수 옵션
- retval : 리턴 값
- winname : 윈도우창 이름
- retval 출력 값이 의미 있을 때 표시

### flags 종류

- cv2.imread() : cv2.IMREAD_COLOR - 기본, cv2.IMREAD_GRAYSCALE ,cv2.IMREAD_UNCHANGED - 알파 채널 포함
- cv2.namedWindow() : cv2.WINDOW_AUTOSIZE - 기본, 크기 고정, cv2.WINDOW_NORMAL

### **cv2.waitKey()**

- 자주 사용된다.
- delay값으로 ms만큼 대기한다.
- 단, delay 값이 0이면 키보드 입력이 있을 때까지 무한 대기한다.
- retval은 키보드에서 누른 키에 대한 코드를 반환한다. 지정된 시간까지 누르지 않으면 -11을 반환한다. (ex. ESC 값은 27)

💣 에러 발생

error: (-215:Assertion failed) size.width>0 && size.height>0 in function ~

: imshow에 넘겨주는 이미지 파일에 문제가 있을 경우 발생하는 에러이다.

1. 이미지 파일에 문제
2. 이미지 파일 존재 x
3. 이미지 경로 잘못 설정

→ 이미지 파일 이름이 한글이었는데 영어로 고치니 해결되었다..!

- 이미지 파일 문제인지 해결하는 코드

  ```python
  import sys
  
  if img is None:
      print('Image load failed')
      sys.exit()
  ```