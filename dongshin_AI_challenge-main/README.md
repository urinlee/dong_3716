# 3716이우린


```
이 프로그램은 어떤 바보(나)가 손목이 부러졌을 때 한창 마우스를 못쓰던 시절 컴퓨터를 못해 아쉬웠 던 기억때문에 제작되었다
```

> PYTHON

- mediapipe
- cv2
- pyautogui

### 모듈 다운
    pip install mediapipe
    pip install open-cv
    pip install pyautogui
    
cmd에 안해주면 작동 안됨

setup.py 만들기 귀찮은건 절대 



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

<br>
<br>
##### ㅇㄴ api 있길래 봤는데 이해가 안됨;;
<br>
<br>

![API](https://cdn.discordapp.com/attachments/891223977995931678/1031965438709616690/unknown.png "뇌절임")


<br>
<br>
##### 근데 영어 못해도 할수 있음
<br>
<br>
<br>
<br>

아 맞다 중요한거!!
이게 보는방향은 지원을 안해줘서 캠을 보면서

이것저것 해보면서 방향을 찾음
  
  
  
답은 꽤나 가까히 있었음

코의 안쪽부분(?)과 코의 끝부분이 얼굴의 방향을 나타낼수 있는걸 찾아냄

나 자신을 칭찬하다가 분명 랜드마크 마다 id가 있다고 들었는데

그걸 안알려줘서 노가다로 찾음



![노가다 흔적2](https://cdn.discordapp.com/attachments/891223977995931678/1031968206316896257/unknown.png "허허")
여기 나오는 좌표랑 하나하나 다 비교해봄
그래서 비슷한 좌표 아이디 따서
그걸로 서로 거리 차이 구해서 왼쪽 오른쪽 가는거 구해봄

## 이건 억울해서라도 풀어야됨

  어케 해서 힘들게 옆에 보는건 인식 했는데
  
  문제는 위 아래임
  
  위아래 볼때는 아무리봐도 연관된게 없는거 같단 말이지
  
  그래서 이거 고민하는데만 3일걸림
  
  사실 이마랑 턱 중간 찾아서 하면 되긴 하는데 귀찮쓰...
  
  그래서 생각해낸게 볼따구임
  
  볼따구 y좌표랑 차이 보니까 꽤나 정확한거 같은거야
  
  그래서 했더니
  
  볼따구가 약간 아래있어서 계속 내려가대..?
  
  그래서 에라모르겠다 하고 10 올려서 했더니 됨
  
  암튼 그렇게 만들어진게 이거임
### 끝







![mediapipe](https://mediapipe.dev/images/face_mesh_ar_effects.gif "미디어파이프")
https://mediapipe.dev/
