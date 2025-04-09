# 🎧 AudioSeparator - AI-based Offline Vocal & Instrument Splitter

Have you ever wanted to isolate just the vocals or remove them from a song completely — without paying for expensive subscriptions or uploading to shady websites?

Well, now you can. Offline. Free. With full control. 💻🔥

---

## 🧠 What I Learned

This morning, I had zero idea how AI can separate vocals, bass, drums, and other elements from an audio file. I searched online for “vocal remover” and found tons of websites — but most required a **subscription** or had annoying limits.

I was super curious and determined to do it offline from my own computer. After digging through articles and chatting with AI (shoutout to my AI buddy 😉), I finally understood **how it works under the hood**.

Now, I can split audio into clean vocals and instrumentals — all from my system. No internet dependency. And today, I’m sharing that whole process + working project with y’all 💜

---

## 📁 Project Structure

.
├── demo.gif
├── LICENSE
├── output
│   └── yourAudio
│       ├── accompaniment.wav
│       └── vocals.wav
├── pretrained_models
│   └── 2stems
│       ├── checkpoint
│       ├── model.data-00000-of-00001
│       ├── model.index
│       └── model.meta
├── preview.png
├── README.md
├── requirements.txt
└── yourAudio.mp3



---

## 🛠 Tech Stack

| Category              | Used                             |
|-----------------------|----------------------------------|
| 💻 Programming Lang   | Python                           |
| 📦 Libraries          | Spleeter, TensorFlow, FFmpeg, LibROSA |
| 📁 Model Used         | Pre-trained Spleeter 2-Stems     |
| 🧠 Architecture       | U-Net (Deep Neural Network)      |

---

## 🔍 What is “2 Stems”?

`2 stems` = **Vocals + Accompaniment**

Other options (not used here but available):
- `4 stems`: Vocals, Drums, Bass, Other
- `5 stems`: Vocals, Drums, Bass, Piano, Other

---

## 🚀 How It Works (Simple Version)

1. You give it a song (`yourAudio.mp3`)
2. It converts the audio into waveform (numerical data)
3. A trained AI model (U-Net) processes it
4. It separates different components (like vocals)
5. You get clean `.wav` files for each stem

---

## ⚙️ Installation & Usage

### 1️⃣ Clone the Repo

```bash
git clone https://github.com/rahulophile/AudioSeparator.git
cd AudioSeparator
```

2️⃣ Setup Python Environment
```bash
pip install -r requirements.txt
```
Make sure Python ≥ 3.8 is installed and working.

3️⃣ Place your audio
Replace yourAudio.mp3 with your own .mp3 file in the root folder.

4️⃣ Run Spleeter to Split Audio
```bash
spleeter separate -i yourAudio.mp3 -p spleeter:2stems -o output
```
5️⃣ Done ✅
Separated files will be in:

```bash
/output/yourAudio/
├── vocals.wav
└── accompaniment.wav
```
🖼 Preview


🎬 Demo


📂 Pre-trained Model Notes
If you don't want to download models every time, you can use the pretrained_models/2stems folder. Just make sure Spleeter knows where to find it.

📜 License
MIT License - Use freely, credit appreciated.

🌟 Github
Give the repo a ⭐ if it helped you: https://github.com/rahulophile/AudioSeparator

Let me know what you think or if you need help — I'm still exploring this AI audio world and loving it! 😎

---