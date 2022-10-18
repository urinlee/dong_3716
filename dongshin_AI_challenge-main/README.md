# 3716이우린


```
이 프로그램은 어떤 바보(나)가 손목이 부러졌을 때 한창 마우스를 못쓰던 시절 컴퓨터를 못해 아쉬웠 던 기억때문에 제작되었다
```

> PYTHON

- mediapipe
- cv2
- pyautogui

### 캠세팅
    capture = cv2.VideoCapture(0)    #0번 캠 인식
    capture.set(cv2.CAP_PROP_FRAME_WIDTH, 1920)    #가로넓이
    capture.set(cv2.CAP_PROP_FRAME_HEIGHT, 1080)    #세로넓이


### 기본 설정
    with mp_face_mesh.FaceMesh(
    max_num_faces=1,    #얼굴 제한? 이라 해야되나?
    refine_landmarks=True,    #눈주위 랜드마크 정밀도
    min_detection_confidence=0.5,    #영어 못해서 뭔진 모르겠지만 신뢰도하 해서 최댓값으로 함
    min_tracking_confidence=0.5) as face_mesh:    #이친구도.....
    while capture.isOpened():
###### ㅇㄴ api 있길래 봤는데 이해가 안됨;;
<br>
<br>

![API](https://cdn.discordapp.com/attachments/891223977995931678/1031965438709616690/unknown.png "뇌절임")

![mediapipe](https://mediapipe.dev/images/face_mesh_ar_effects.gif "미디어파이프")

