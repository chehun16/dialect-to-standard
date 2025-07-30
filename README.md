# Converting dialect speech to standard speech
deepdaiv 24w audio


## Dataset

- [한국어 방언 발화(경상도)](https://aihub.or.kr/aihubdata/data/view.do?currMenu=&topMenu=&aihubDataSe=data&dataSetSn=119)
- [한국어 음성 데이터](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=realm&dataSetSn=123)

<br>

## Pipeline

STT → Translation → TTS

Ko-Speech(DeepSpeech2) Ko-BART TensorflowTTS(fastspeech2)

사투리 발화 → STT → 텍스트 → TTS → 표준어 발화
