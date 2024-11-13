## ___***ToonCrafter: Generative Cartoon Interpolation***___
<!-- ![](./assets/logo_long.png#gh-light-mode-only){: width="50%"} -->
<!-- ![](./assets/logo_long_dark.png#gh-dark-mode-only=100x20) -->
<div align="center">



</div>
 
## 🔆 Introduction

⚠️ Please check our [disclaimer](#disc) first.

🤗 ToonCrafter can interpolate two cartoon images by leveraging the pre-trained image-to-video diffusion priors. Please check our project page and paper for more information. <br>







### 1.1 Showcases (512x320)
<table class="center">
    <tr style="font-weight: bolder;text-align:center;">
        <td>Input starting frame</td>
        <td>Input ending frame</td>
        <td>Generated video</td>
    </tr>
  <tr>
  <td>
    <img src=assets/72109_125.mp4_00-00.png width="250">
  </td>
  <td>
    <img src=assets/72109_125.mp4_00-01.png width="250">
  </td>
  <td>
    <img src=assets/00.gif width="250">
  </td>
  </tr>


   <tr>
  <td>
    <img src=assets/Japan_v2_2_062266_s2_frame1.png width="250">
  </td>
  <td>
    <img src=assets/Japan_v2_2_062266_s2_frame3.png width="250">
  </td>
  <td>
    <img src=assets/03.gif width="250">
  </td>
  </tr>
  <tr>
  <td>
    <img src=assets/Japan_v2_1_070321_s3_frame1.png width="250">
  </td>
  <td>
    <img src=assets/Japan_v2_1_070321_s3_frame3.png width="250">
  </td>
  <td>
    <img src=assets/02.gif width="250">
  </td>
  </tr> 
  <tr>
  <td>
    <img src=assets/74302_1349_frame1.png width="250">
  </td>
  <td>
    <img src=assets/74302_1349_frame3.png width="250">
  </td>
  <td>
    <img src=assets/01.gif width="250">
  </td>
  </tr>
</table>

### 1.2 Sparse sketch guidance
<table class="center">
    <tr style="font-weight: bolder;text-align:center;">
        <td>Input starting frame</td>
        <td>Input ending frame</td>
        <td>Input sketch guidance</td>
        <td>Generated video</td>
    </tr>
  <tr>
  <td>
    <img src=assets/72105_388.mp4_00-00.png width="200">
  </td>
  <td>
    <img src=assets/72105_388.mp4_00-01.png width="200">
  </td>
  <td>
    <img src=assets/06.gif width="200">
  </td>
   <td>
    <img src=assets/07.gif width="200">
  </td>
  </tr>

  <tr>
  <td>
    <img src=assets/72110_255.mp4_00-00.png width="200">
  </td>
  <td>
    <img src=assets/72110_255.mp4_00-01.png width="200">
  </td>
  <td>
    <img src=assets/12.gif width="200">
  </td>
   <td>
    <img src=assets/13.gif width="200">
  </td>
  </tr>


</table>


### 2. Applications
#### 2.1 Cartoon Sketch Interpolation (see project page for more details)
<table class="center">
    <tr style="font-weight: bolder;text-align:center;">
        <td>Input starting frame</td>
        <td>Input ending frame</td>
        <td>Generated video</td>
    </tr>

  <tr>
  <td>
    <img src=assets/frame0001_10.png width="250">
  </td>
  <td>
    <img src=assets/frame0016_10.png width="250">
  </td>
  <td>
    <img src=assets/10.gif width="250">
  </td>
  </tr>


   <tr>
  <td>
    <img src=assets/frame0001_11.png width="250">
  </td>
  <td>
    <img src=assets/frame0016_11.png width="250">
  </td>
  <td>
    <img src=assets/11.gif width="250">
  </td>
  </tr>

</table>


#### 2.2 Reference-based Sketch Colorization
<table class="center">
    <tr style="font-weight: bolder;text-align:center;">
        <td>Input sketch</td>
        <td>Input reference</td>
        <td>Colorization results</td>
    </tr>
    
  <tr>
  <td>
    <img src=assets/04.gif width="250">
  </td>
  <td>
    <img src=assets/frame0001_05.png width="250">
  </td>
  <td>
    <img src=assets/05.gif width="250">
  </td>
  </tr>


   <tr>
  <td>
    <img src=assets/08.gif width="250">
  </td>
  <td>
    <img src=assets/frame0001_09.png width="250">
  </td>
  <td>
    <img src=assets/09.gif width="250">
  </td>
  </tr>

</table>







## 📝 Changelog
- [ ] Add sketch control and colorization function.
- __[2024.05.29]__: 🔥🔥 Release code and model weights.
- __[2024.05.28]__: Launch the project page and update the arXiv preprint.
<br>


## 🧰 Models

|Model|Resolution|GPU Mem. & Inference Time (A100, ddim 50steps)|Checkpoint|
|:---------|:---------|:--------|:--------|
|ToonCrafter_512|320x512| TBD (`perframe_ae=True`)|[Hugging Face](https://huggingface.co/Doubiiu/ToonCrafter/blob/main/model.ckpt)|


Currently, our ToonCrafter can support generating videos of up to 16 frames with a resolution of 512x320. The inference time can be reduced by using fewer DDIM steps.


### Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/IHEfty/ToonCrafter-for-windows.git
   cd ToonCrafter-for-windows
   ```

2. Run the installation script:
   - For English: `install.ps1` (Powershell)
   - For Chinese: `install-cn.ps1` (Powershell)

3. **Download Models Automatically**: Models will be downloaded during installation, so there is no need for manual downloads.

## 💫 Running Inference

### 1. Command Line Execution

Download the pre-trained ToonCrafter_512 model and place `model.ckpt` in `checkpoints/tooncrafter_512_interp_v1/model.ckpt`. Then, execute:
```bash
sh scripts/run.sh
```
Or
```bash
cd scripts
run.bat
```

### 2. Local Gradio Demo

To launch a local Gradio GUI demo:
   ```bash
   powershell -File run_gui.ps1
   ```

## 📢 Disclaimer

This framework initiates generative cartoon interpolation, though results may vary due to the stochastic nature of video generation models. This open-source research tool is not intended for commercial applications and may not fulfill all expectations.

### Responsible Use

We aim to positively impact AI-driven video generation. This tool is provided for responsible, lawful use only. Users must adhere to local laws, and the developers do not assume liability for misuse. 
****
