# Generative AI - sample codes
* `gTTS.py` : to generate gTTS.mp3

---
## Text-to-Text (LLMs)

### local LLM Server & Client
* `python llm_server.py` (on your PC's GPU)
* `python post_text.py`  (on your PC's CPU)

---
### Colab's LLM Server & Client
* [pyngrok-LLM server](https://github.com/rkuo2000/GenAI/blob/main/Text-to-Text/pyngrok_LLM_Server.ipynb) (on Colab T4)<br>
![](https://github.com/rkuo2000/GenAI/blob/main/assets/pyngrok_LLM_Server_fastapi.png?raw=true)
* [post-text client](https://github.com/rkuo2000/GenAI/blob/main/Text-to-Text/post_text.py) (on your PC)<br>
![](https://github.com/rkuo2000/GenAI/blob/main/assets/pyngrok_post_text.png?raw=true)

---
## Audio-to-Text

### local ASR+LLM Server (on your PC+GPU)
1. **run server on local PC (on your PC+GPU):** `python whisper_llm_server.py`<br>
2. **Generate audio file**: `python ../gTTS.py "Hello, how are you?" en`<br>
3. **Post Audio to Server**: `python post_audio.py`<br>

---
### Colab ASR+LLM Server (on Colab T4)
1. **Open [colab](https://colab.research.google.com) to run [pyngrok_Whisper_LLM_Server.ipynb](https://github.com/rkuo2000/GenAI/blob/main/Audio-to-Text/pyngrok_Whisper_LLM_Server.ipynb)** on Colab T4
2. **Generate audio file**: `python ../gTTS.py "Hello, how are you?" en`<br>
3. **Post Audio to Server**: `python post_audio.py`<br>
![](https://github.com/rkuo2000/GenAI/blob/main/assets/post_audio.png?raw=true)

---
## Image-to-Text (VLM)

### local ASR+VLM server (on GPU RTX4060Ti-OC 16GB)
1. `python whisper_llava_server.py` (server)<br>
2. `python ../gTTS.py "這是什麼有名的台南美食?" zh` (TTS)<br>
3. `python post_imgau.py` (client)<br>
![](https://github.com/rkuo2000/GenAI/blob/main/Image-to-Text/images/Tainan_BeefSoup.jpg?raw=true)<br>
![](https://github.com/rkuo2000/GenAI/blob/main/assets/post_imgau.png?raw=true)

* Whisper+LLaVA Server (ASR+VLM)<br>
![](https://github.com/rkuo2000/GenAI/blob/main/assets/whisper_llava_server.png?raw=true)

---
## Text-to-Speech
* **Parler TTS**: `python parler.py`
* **Bark TTA**: `python bark_en.py`, `python bark_cn.py`
* **Coqui TTS**: `python coqui_en.py`, `python coqui_zh.py`
* **text-to-speech**: `python text_to_speech.py`
* **gTTS**: `python gTTS.py "你好?" zh`
* **gTranslate**: `python gTranslate.py`

---
## Text-to-Image 
* `sdxl-base.py` - run SDXL-base model to input text and generate an image
* `sdxl-lightning-lora.py` - run SDXL-Lightning with LoRA model to use text to generate an image
* `sdxl-lightning-unet.py` - run SDXL-Lightning with UNet model to use text to generate an image

---
## Image-to-3D

### TripoSR
![](https://favtutor.com/articles/wp-content/uploads/2024/03/TripoSR-Image-to-3D-Objects-Examples.gif)

### Text-to-3D
**gTranslate + SDXL-Lightning + TripoSR + AppInventor2**<br>
