# Detecção de fogo com YOLOv8

Detector de fogo treinado com YOLOv8n (Ultralytics) no Google Colab (GPU T4).

## Dataset
Fire_detector, autor "vision", Roboflow Universe, licença CC BY 4.0.
https://universe.roboflow.com/vision-zz6rk/fire_detector-g4lir
Versão 1: 4.693 imagens (3.285 treino / 938 validação / 470 teste), 2 classes.
O dataset não está neste repositório; baixe pelo link acima ou pelo notebook.

## Resultados (validação)
mAP50 = 0,729 | mAP50-95 = 0,447 | Precisão = 0,734 | Recall = 0,699

<img width="469" height="477" alt="image" src="https://github.com/user-attachments/assets/ae9c853c-fdbf-401b-a0eb-1b8d19f50bd7" />
Imagem de teste	Classe	Confiança
fire1-377	fire	0,71
WEBFire1863	fire (3 caixas)	0,41; 0,39; 0,32
89_jpg	fire (2 caixas)	0,32; 0,27
NoiseWEBFire1346	fire	0,67


## Como usar
pip install -r requirements.txt
python uso.py caminho_da_imagem.jpg

## Como treinar
Abra Fire_detector.ipynb no Colab (GPU T4), informe sua chave do Roboflow
(nunca a publique) e execute as células. Ou use treino.py.

## Arquivos
- Fire_detector.ipynb: notebook completo
- treino.py / uso.py: treinamento e inferência
- best.pt: modelo treinado
