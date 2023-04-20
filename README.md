# face_recognition_exam
깃허브 사이트에 있는 얼굴 인식 모델의 단점찾기

1. 얼굴인식 원 소스 코드 주소 URL
https://github.com/ageitgey/face_recognition

2.실행 예제코드 주소 URL
https://github.com/ageitgey/face_recognition/blob/master/examples/facerec_from_webcam_faster.py


###정리내용.

1. 얼굴인식 원 소스 코드 주소 URL

2. 자신이 찾은 얼굴인식 개요

3. 장단점 분석


1. 얼굴인식 원 소스 코드 주소 URL

https://github.com/ageitgey/face_recognition
* 실행 예제코드 주소 URL
https://github.com/ageitgey/face_recognition/blob/master/examples/facerec_from_webcam_faster.py
설명: 위 코드는 face_recognition 패키지를 사용하여 웹캠에서 영상을 읽어와 실시간으로 얼굴 인식 및 인식된 얼굴에 대한 이름을 표시하는 코드로 바이든, 오바마 사진등의 이름은 표시 가능하지만 나머지는 unkown으로 표시됩니다.

* 실행과정(Compiler:Colab)
- 실행환경: import face_recognition를 위한 환경: numpy, pillow, opency, scipy, cmake, dlib 설치합니다.
- 이미지 파일 준비 기본 이미지 대신 iu. 유재석이미지를 드라이브에 저장 -> 마운트, 호스팅 연결
- 코드 복사 후 실행합니다. 
- 오류과정 : error: OpenCV(4.7.0) /io/opencv/modules/imgproc/src/resize.cpp:4062: error: (-215:Assertion failed) !ssize.empty() in function 'resize’->
- 수정 코드 URL
 : https://github.com/kim6274158/face_recognition_exam/blob/main/face_recognition_change.ipynb

* ![image](https://user-images.githubusercontent.com/127082884/233367800-be2b45d1-d2e2-4e90-895e-ad072df02c39.png)

나의 깃허브 주소
https://github.com/kim6274158/face_recognition_exam

2. 얼굴인식 개요
* 목적
다양한 어플리케이션에서 얼굴 인식 기술을 쉽게 이용할 수 있도록 하기 위함입니다. 예를 들어, 보안 시스템, CCTV 모니터링, 인증 시스템 등에서 이러한 기술이 활용될 수 있습니다. 또한, 이러한 기술을 이용하여 사진 앱에서 얼굴 태깅, 얼굴 검색 등의 기능도 구현할 수 있습니다.
* 주요 기능
- 얼굴 검출 (Face Detection): 사진이나 비디오에서 얼굴을 검출할 수 있습니다. 또한, 얼굴 검출 결과를 바탕으로 얼굴 영역을 자르거나, 얼굴이 포함된 이미지를 회전시키는 등의 다양한 작업을 수행할 수 있습니다.
- 실시간 얼굴 인식 (Face Recognition): 웹캠을 이용하여 실시간으로 얼굴을 인식하고 결과를 출력합니다. 그리고 등록된 얼굴과 일치하는지 여부를 판별할 수 있습니다. 이를 위해 얼굴 이미지의 특징을 추출하고, 이를 비교하여 일치하는지 여부를 판별합니다. 이를 이용하여 보안 시스템, 출석체크 시스템 등 다양한 응용프로그램을 구현할 수 있습니다.
- 자동화된 테스트(Automated Testing):테스트 이미지와 테스트 데이터셋을 이용하여 얼굴 인식 정확도를 자동으로 테스트합니다.
- 얼굴 등록(Face registration): 인식 대상이 되는 얼굴들을 미리 등록하여 데이터베이스에 저장합니다. 이를 통해 인식 대상이 되는 얼굴과 일치 여부를 판별할 수 있습니다.
- 얼굴 인식 기반 캡션 생성 (Caption Generation): 인물의 얼굴을 인식하여, 해당 인물에 대한 자막을 생성할 수 있습니다.
- 얼굴 랜드마크 추출 (Facial Landmark Detection): 인물의 얼굴에서 눈, 코, 입 등의 특징점을 추출할 수 있습니다. 이를 이용하여 다양한 응용프로그램을 구현할 수 있습니다.
- 얼굴 분류 (Face Clustering): 등록된 다수의 얼굴을 그룹화하여, 인물별로 분류할 수 있습니다. 이를 이용하여, 사진첩에서 특정 인물의 사진을 찾거나, 인물의 연령대, 성별 등을 분류하는 등의 작업을 수행할 수 있습니다.
- 성별 및 연령 추정 (Age and Gender Estimation): 얼굴 이미지를 이용하여 해당 인물의 성별과 연령대를 추정할 수 있습니다.
- 얼굴 합성 (Face Morphing): 두 개의 얼굴 이미지를 합성하여 새로운 얼굴 이미지를 생성할 수 있습니다.

3. 장단점 분석
* 장점
 - 높은 정확도: 딥러닝 알고리즘을 이용하여 얼굴 인식을 수행하므로, 다른 방법보다 높은 인식 정확도를 보입니다.
- 다양한 기능: 얼굴 검출, 얼굴 인식, 얼굴 분류, 얼굴 합성 등 다양한 기능을 제공하여, 다양한 응용프로그램을 구현할 수 있습니다.
 - 쉬운 사용성: Python 언어를 이용하여 개발되었으며, OpenCV 라이브러리를 사용하므로, 다른 라이브러리나 툴킷과의 호환성이 높습니다. 따라서, 다른 라이브러리나 프레임워크와 연동하여 사용하기도 용이합니다.
 - 빠른 처리 속도: C++로 작성된 OpenCV 라이브러리를 이용하여, 높은 처리 속도를 보입니다.
* 단점
 - 하드웨어 요구 사항: 이 프로젝트는 딥러닝 알고리즘을 이용하므로, 높은 성능의 CPU나 GPU가 필요합니다. 따라서, 저사양 컴퓨터에서는 처리 속도가 느릴 수 있습니다.
 - 데이터셋 의존도: 딥러닝 알고리즘을 이용하므로, 대량의 얼굴 이미지 데이터셋이 필요합니다. 이러한 데이터셋이 없거나, 작은 규모의 데이터셋을 사용할 경우 인식 정확도가 떨어질 수 있습니다.
 - 오분류 가능성: 딥러닝 알고리즘을 이용하기 때문에 얼굴 인식을 위한 학습 데이터에 따라 오분류가 발생할 수 있습니다. 이러한 경우에는 추가적인 데이터 수집과 학습이 필요합니다.
 - 개인정보 보호 문제: 이 프로젝트를 이용하여 얼굴 인식 시스템을 구현할 경우, 개인정보 보호 문제가 발생할 수 있습니다. 따라서, 이를 고려하여 적절한 보안 대책을 마련해야 합니다.
