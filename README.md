# 24w_audio
deepdaiv 24w audio

1. 프로젝트 소개
⭐ **사투리 인식 및 표준어 변환 시스템** ⭐입니다! 
사투리 음성으로 주어지는 발화를 최종적으로 표준어 음성으로 출력하게 하는 모델입니다.

2. 데이터 소개
**1) 한국어 방언 발화(경상도)**

저희는 [AI Hub의 한국어 방언 발화(경상도) ****데이터](https://aihub.or.kr/aihubdata/data/view.do?currMenu=&topMenu=&aihubDataSe=data&dataSetSn=119)를 사용하였습니다. 이 데이터는 경상도 지역 2,000명 이상의 10대~60대의 연령별 화자가 발화한 3,000시간 이상의 음성 데이터와 대응된 담화 텍스트 말뭉치로 구성되어 있습니다. 원본 방언 텍스트 및 방언에 대응하는 표준어 대응쌍을 포함하여 전사한 50만 건 이상의 어절 데이터셋이 있고, 데이터화되어 JSON 포맷의 데이터 파일로 구성되어 있습니다.
**2) 한국어 음성** 

AI hub의 [한국어 음성 데이터](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=realm&dataSetSn=123)를 사용하였습니다. 이는 2,000여명이 발성한 한국어 대화음성 1,000시간으로 이루어져 있습니다. 두 사람이 다양한 주제로 자유롭게 대화하는 음성이 녹음되어 있습니다. 
데이터는 발화 단위로 분할된 음성파일(16kHz/16bits, headerless (little endian) linear PCM)과 전사파일로 구성되어 있습니다.

3. 워크플로우
STT-Translation-TTS
Ko-Speech(DeepSpeech2) Ko-BART TensorflowTTS(fastspeech2)
사투리 발화 → STT → 텍스트 → TTS → 표준어 발화
