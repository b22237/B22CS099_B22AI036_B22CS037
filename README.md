
```text
# Visual Speech Recognition (LRS3)

This repo is for visual speech recognition on LRS3 and other datasets. It’s based on the Auto-AVSR work.

## Setup
1. Clone this:
```bash
git clone [https://github.com/b22237/B22CS099_B22AI036_B22CS037.git](https://github.com/b22237/B22CS099_B22AI036_B22CS037.git)
cd B22CS099_B22AI036_B22CS037
```

2. Make env:
```bash
conda create -n vsr python=3.8
conda activate vsr
pip install -r requirements.txt
conda install -c conda-forge ffmpeg
```

3. Get models:
Download the pre-trained weights from the original links and put them in `./benchmarks/${dataset}/models`.

## How to use

**Test the model:**
```bash
python eval.py config_filename=[config] labels_filename=[labels] data_dir=[data] landmarks_dir=[landmarks]
```

**Run on your own file:**
```bash
python infer.py config_filename=[config] data_filename=[video_or_audio_file]
```

**Crop mouth area:**
```bash
python crop_mouth.py data_filename=[input] dst_filename=[output]
```
