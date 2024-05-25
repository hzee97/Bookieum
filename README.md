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

## 📃 선정 배경
독서량이 점점 떨어지는 현대인들을 위해 독서에 대한 흥미를 유발하고 지속적인 독서를 위한 환경조성 필요성 대두.

![10](https://github.com/hzee97/Bookieum/assets/136284855/f583f112-deaa-4cf8-9bda-9488c54c22e7)

## 💎 서비스 소개
“북이음” 은 사용자의 현재 감정을 토대로 책을 추천하고 그에 따른 책의 핵심문구 혹은 Catchphrase를
사용자 맞춤형으로 표시하여 사용자로 하여금 책에 흥미를 느낄 수 있도록 도와주는 서비스입니다.

책과 사용자를 유기적으로 이어질 수 있도록 설계하였습니다. 
핵심모델은 사용자의 언어, 표정인식 등을 통해 감정데이터를 3 sector로 분류하여 맵핑하고 이를 기반으로 날씨, 개인화모델의 가중치를 더하여 컨텐츠를 추천하는 모델입니다.
이 후 책에 대한 지속적인 흥미 유발을 위한 부수적인 기능을 갖추어 Pain point 해결에 집중하였습니다.

## 🛠 기술 스택

언어 : <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white"/>
<img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white"/>
<img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat&logo=javascript&logoColor=white">

Front-End : <img src="https://img.shields.io/badge/React-005571?style=flat&logo=React&logoColor=white"/>

Back-End : <img src="https://img.shields.io/badge/Django-092E20?style=flat&logo=Django&logoColor=white"/>

AI : <img src="https://img.shields.io/badge/Tensorflow-FF6F00?style=flat&logo=Tensorflow&logoColor=white"/>

DataBase : <img src="https://img.shields.io/badge/Mysql-4479A1?style=flat&logo=mysql&logoColor=white"> 

Server : <img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=flat&logo=amazon aws&logoColor=white"> 

Version Control : <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white">

Communication : 
<img src="https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=figma&logoColor=white">
<img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=notion&logoColor=white">

## 🎨 ERD

![11](https://github.com/hzee97/Bookieum/assets/136284855/a5d6feb3-f669-4a43-b415-15eabfb3f428)

## ✨ 핵심 기능

# 1. 오늘의 책 추천

A. Input
1. 문답을 베이스로 사용자가 원하는 방식(텍스트, 음성)으로 그날의 감정 데이터 수집(Clova API사용)
>A. “오늘, 당신의 하루는 어땠나요?”라는 질문에 답변하는 동안의 얼굴 감정분석
>
>B.“오늘, 당신의 하루는 어땠나요?”라는 질문에 대한 답변을 텍스트분석

2. 환경 데이터를 키워드 형태로 수집하여 Target 값의 표본 중 환경데이터에 대응하는 책들에 대하여 가중치를 부여

3. 개인화 데이터(회원가입시 설문조사 + 사용자 이용데이터)

B. Output
1. Input Data 기반의 책 3권 추천(3권)

① 하이브리드 추천 모델 이용
>i. 감정점수*가중치 + 컨텐츠유사도*가중치 + 예측 선호도 *가중치 = 최종점수
>
>최종 점수에 따른 도서 추천
>
>→ 컨텐츠 유사도 : 책의 줄거리, 저자 등 코사인 유사도를 계산하여 사용자가 좋아한 책과 유사한 책을 추천
>
>→ 예측 선호도 : 개인화 모델 기반 비슷한 성향점수를 갖고 있는 유사 사용자들이 선호하는 책을 추천

② 사용자에게 흥미 유발을 할 수 있는 맞춤형 하이라이트 문구와 간단한 줄거리 표시

③ 추천 도서 중 사용자의 선택을 통해 개인화 모델 데이터 추가 수집(재귀로직)

![12](https://github.com/hzee97/Bookieum/assets/136284855/5bb02b31-249f-4792-aa5f-19bf25349196)
