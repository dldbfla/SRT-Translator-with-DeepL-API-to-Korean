# SRT-Translator-with-DeepL-API-to-Korean
이 프로젝트는 DeepL API를 사용하여 SRT 파일 내의 자막을 번역하는 파이썬 스크립트입니다. Tkinter를 사용하여 파일 선택과 저장을 위한 GUI를 제공합니다.
## 예시 

![스크린샷 2024-07-12 173252](https://github.com/user-attachments/assets/2bee5a84-b837-49dd-8983-55faab1be414)


![스크린샷 2024-07-12 174821](https://github.com/user-attachments/assets/ac6480a2-b3b7-46a6-9e55-d4bfd654efe9)


![스크린샷 2024-07-12 175611](https://github.com/user-attachments/assets/7b8ec828-eaed-4435-8060-cf552ca8cfcc)

## 기능

- SRT 파일 내의 자막을 번역
- 번역된 SRT 파일을 지정된 폴더에 저장
- DeepL API를 사용한 번역

## 요구 사항

- Python 3.x
- `requests` 라이브러리
- `tqdm` 라이브러리
- `tkinter` 라이브러리 (대부분의 Python 배포판에 기본 포함)
- DeepL API 키(DEEPL_API_KEY = ''안에 지급받은 DeepL API 키를 넣으세요.)

## 설치

필요한 라이브러리를 설치합니다:

```bash
pip install requests tqdm
```

## 사용법
##### 스크립트를 실행하면 Tkinter를 사용하여 파일 선택 창이 나타납니다. 여기서 번역할 SRT 파일을 선택합니다.
. SRT 파일을 선택하면 다음 단계로 넘어갑니다.
. 저장 폴더 선택

##### 번역된 SRT 파일을 저장할 폴더를 선택하는 창이 나타납니다. 원하는 폴더를 선택합니다.
. 폴더를 선택하면 번역이 시작됩니다.
. 번역 진행

##### 선택한 SRT 파일을 읽어들입니다. 이 과정에서 각 자막 라인을 추출합니다.
. 추출된 자막 라인은 DeepL API를 통해 번역됩니다. 번역 과정은 tqdm 라이브러리를 통해 진행 상황이 터미널에 표시됩니다.
. 시간 정보나 빈 줄은 번역하지 않고 그대로 유지됩니다.
. 파일 저장

##### 번역된 자막을 새로운 SRT 파일로 저장합니다. 저장 파일명은 translated_원본파일이름.srt 형태로 지정됩니다.
. 번역된 파일은 사용자가 선택한 폴더에 저장됩니다.
. 완료 메시지

##### 번역이 완료되면 터미널에 완료 메시지가 출력되며, 번역된 파일의 경로가 표시됩니다.
