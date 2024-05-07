<p align="center">

  <h2 align="center">Bookieum : AI Book Recommendation servicel</h2>
  <p align="center">
    <a href="https://scholar.google.com/citations?user=-4iADzMAAAAJ&hl=en"><strong>이재윤</strong></a>
    ·
    <a href="http://jeff95.me/"><strong>장현지</strong></a>
    ·
    <a href="https://scholar.google.com.sg/citations?user=8gm-CYYAAAAJ&hl=en"><strong>차하린</strong></a>
    ·
    <a href="https://hanshuyan.github.io/"><strong>최영렬</strong></a>
    ·
    <a href="https://scholar.google.com/citations?user=stQQf7wAAAAJ&hl=en"><strong>최자윤 </strong></a>
    ·
    <a href="https://zhangchenxu528.github.io/"><strong>함세연</strong></a>
    ·
    <br>
    <br>
        <a href="https://arxiv.org/abs/2311.16498"><img src='https://img.shields.io/badge/arXiv-MagicAnimate-red' alt='Paper PDF'></a>
        <a href='https://showlab.github.io/magicanimate'><img src='https://img.shields.io/badge/Project_Page-MagicAnimate-green' alt='Project Page'></a>
        <a href='https://huggingface.co/spaces/zcxu-eric/magicanimate'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue'></a>
    <br>
    <b> Bookieum</b>
  </p>

  <table align="center">
    <tr>
    <td>
      <img src="assets/teaser/t4.gif">
    </td>
    <td>
      <img src="assets/teaser/t2.gif">
    </td>
    </tr>
  </table>

## 📢 News
* **[2023.12.12]** Release server with https, we are about to use camera on our service! stay tuned!
* **[2023.11.23]** Release Bookieum


## 🏃‍♂️ Getting Started

회원가입 후 기본 설문조사를 해주세요!

오늘의 책 추천 받기를 눌러서 오늘의 책을 추천 받아보세요!

**Place them as follows:**
```bash
magic-animate
|----pretrained_models
  |----MagicAnimate
    |----appearance_encoder
      |----diffusion_pytorch_model.safetensors
      |----config.json
    |----densepose_controlnet
      |----diffusion_pytorch_model.safetensors
      |----config.json
    |----temporal_attention
      |----temporal_attention.ckpt
  |----sd-vae-ft-mse
    |----...
  |----stable-diffusion-v1-5
    |----...
|----...
```
