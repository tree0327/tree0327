<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Inter&weight=700&size=42&duration=2800&pause=900&color=0066CC&center=true&vCenter=true&width=760&height=66&lines=%EA%B9%80%EB%8B%A4%EB%B9%88+%C2%B7+Dabin+Kim;Problem-solving+with+Structure" alt="김다빈 · Dabin Kim" />

### 문제를 구조로 해결하는 AI 엔지니어

<sub>입력 → 검색 → 추론 → 검증 → 응답까지, AI 파이프라인 전체를 한 흐름으로 설계합니다.</sub>

<br/>

[**대표 프로젝트 →**](#-대표-프로젝트)&nbsp;·&nbsp;
[**기술 스택 →**](#-기술-스택)&nbsp;·&nbsp;
[**경력 →**](#-경력--학력)&nbsp;·&nbsp;
[**연락하기 →**](#-연락하기)

<br/>

![followers](https://img.shields.io/github/followers/tree0327?label=followers&style=flat-square&color=1d1d1f&labelColor=ffffff&logo=github&logoColor=0066CC)
![repos](https://img.shields.io/badge/public%20repos-21-1d1d1f?style=flat-square&logo=git&logoColor=0066CC&labelColor=ffffff)
![camp](https://img.shields.io/badge/SK%20Networks%20Family%20AI%20Camp-23%EA%B8%B0-0066CC?style=flat-square&labelColor=ffffff)

</div>

<br/>

---

## 👋 About Me

가구 시공 **3년 9개월**, 웹 프론트엔드 **1년 8개월**의 실서비스 경험을 바탕으로
AI 엔지니어로 영역을 확장해온 풀스택 AI 개발자입니다.

모델을 단순히 호출하는 데 그치지 않고,
**RAG 검색 신뢰도 · LLM 서빙 · LangGraph 오케스트레이션 · 시스템 인프라**까지
파이프라인 전체를 직접 설계·튜닝하는 데 강점이 있습니다.

```text
프론트엔드 (1.8년)   →   AI 엔지니어링 (현재)
실서비스 SCSS·React       LangGraph · RAG · vLLM
사용자 경험 감각          파이프라인 설계 역량
```

<br/>

---

## 📦 대표 프로젝트

> AI 4 · Frontend 3, 총 7개 중 **가장 봐주셨으면 하는 프로젝트**들입니다.

<br/>

### 1. 🏗️ CADence — CAD sLLM Multi-Agent Platform
<sub>**2026.04 – 2026.05 · 부팀장 / Agent Engineer**</sub>

AutoCAD `.dwg` 도면의 **물리적 이상 탐지**와 KEC·NFSC 법규 검토 사항을
LLM Multi-Agent로 사전 검증하고, **Human-in-the-Loop 기반 자동 도면 수정**까지
한 흐름으로 연결한 B2B AutoCAD Plugin 플랫폼.

| 영역 | 내용 |
|---|---|
| **Fine-Tuning** | Qwen3.5-27B를 RunPod에서 **QLoRA 양자화 + 파인튜닝** · 16차원 Adaptor를 FFN 상단에 위치 |
| **Hybrid RAG** | 조항번호·수치 키워드 정확 매칭을 위해 **tsvector + pg_trgm + RRF + Qwen3-Reranker** |
| **Plugin** | AutoCAD C# Plugin 직접 설계 · **AutoCAD ↔ Agent 양방향 통신** |
| **Harness** | LangGraph Tool Calling 기반 Orchestrator Multi-Agent로 도면 검토 흐름 제어 |

<sub>`LangGraph` · `Qwen3.5-27B` · `QLoRA` · `pgvector` · `RRF` · `AutoCAD C#` · `RunPod` · `AWS`</sub>

<br/>

### 2. 🎙️ AIwork — LangGraph 기반 AI 모의면접 Assistant
<sub>**2026.02 – 2026.03 · AI Engineer / BE (인성면접 게시판)**</sub>

LangGraph LLM Orchestrator로 면접 흐름을 그래프 단위로 제어하는
**Multi-Agent 모의면접 SaaS**. STT · LLM · 비전을 결합한 멀티모달 파이프라인.

| 영역 | 내용 |
|---|---|
| **LLM-as-a-Judge** | 면접관 Persona 4종 · 정확성·깊이·구조·명확성 4축 채점 |
| **LangGraph Agent** | 답변 점수에 따라 **꼬리질문 동적 생성** (최대 2회 제한) |
| **태도 평가** | MediaPipe Landmark로 얼굴 각도·표정·시선 수치화 → 서비스 로직에서 해석 |
| **BE** | 인성면접 게시판 FastAPI 라우트 · RLS 멀티테넌시 · 도메인 모델링 단독 책임 |

<sub>`LangGraph` · `OpenAI` · `Faster-Whisper` · `MediaPipe` · `FastAPI` · `RLS`</sub>

<br/>

### 3. ✍️ 합격 — 9-Judge Full-Async AI 자소서 생성 플랫폼
<sub>**2026.04 – 2026.05 · AI Engineer / SaaS Architect**</sub>

채용공고 · 이력서 · 회사정보 · 합격 자소서를 하나의 **Full-Async 파이프라인**으로 연결한 AI SaaS.
**9명의 LLM 평가관이 실시간 SSE 스트리밍**으로 피드백을 제공.

| 영역 | 내용 |
|---|---|
| **RAG** | 합격 자소서 데이터를 **Parent-Child 청킹**으로 인덱싱 · 채용공고 임베딩 유사도 검색 |
| **LLM-as-a-Judge** | 9 평가관 병렬 실행 + SSE 스트리밍 · **다차원 보정 테이블** 기반 통과 확률 산출 |
| **Async** | Full-Async 아키텍처로 동시 다수 요청 + 평가관별 stream 응답성 확보 |
| **SaaS** | 결제 + RLS 멀티테넌시 + 플랜별 쿼터 + 관리자 대시보드까지 프로덕션 수준 풀스택 |

<sub>`FastAPI` · `Next.js` · `SSE` · `Parent-Child RAG` · `Vercel` · `Render`</sub>

<br/>

### 4. 🔮 점집.com — 멀티모달 AI 운세 분석 풀스택 서비스
<sub>**2026.04 – 2026.05 · Data Analyst / Full-stack**</sub>

관상 · 사주 · 타로 · 별자리 4개 입력 타입을 분기 처리한 뒤
**LLM 해석으로 통합한 멀티모달 AI 풀스택 웹 서비스**.

| 영역 | 내용 |
|---|---|
| **Multimodal** | 입력 타입별 최적 모델 매핑 → LLM 해석 단계로 통합 |
| **관상 분석** | MediaPipe + XGBoost로 안면 특징 추출·분류 → GPT-4o-mini 해석 생성 |
| **RAG** | 사주 · 별자리 데이터를 RAG 컨텍스트로 주입해 신뢰도 있는 해석 응답 |
| **Full-stack** | Next.js + FastAPI · Vercel · Railway 분리 배포 |

<sub>`CNN` · `MediaPipe` · `XGBoost` · `RAG` · `GPT-4o-mini` · `Next.js`</sub>

<br/>

<details>
<summary><b>🌐 Frontend Projects (3) — 일상이지 재직 1년 8개월</b></summary>

<br/>

| 프로젝트 | 기간 | 역할 | 핵심 |
|---|---|---|---|
| **URSCOPE 기업 홈페이지 제작/리뉴얼** | 2025.02–2025.10 | **PM / FE** | SCSS Mixin·Variables 컴포넌트화 · 9대 시스템 분석 탭 |
| **한양사이버대학교 홈페이지 리뉴얼** | 2024.11–2025.01 | FE | Metro UI 카드형 모듈 · 사용자 맞춤 메인페이지 커스터마이징 |
| **미래엔 디지털 교육 콘텐츠** | 2024.04–2024.12 | Web Publisher | 학년·과목별 템플릿 기반 대량 콘텐츠 구조화 |

</details>

<br/>

---

## 🧰 기술 스택

#### DL / ML
![Python](https://img.shields.io/badge/Python-1d1d1f?style=flat-square&logo=python&logoColor=0066CC&labelColor=ffffff)
![PyTorch](https://img.shields.io/badge/PyTorch-1d1d1f?style=flat-square&logo=pytorch&logoColor=0066CC&labelColor=ffffff)
![TensorFlow](https://img.shields.io/badge/TensorFlow-1d1d1f?style=flat-square&logo=tensorflow&logoColor=0066CC&labelColor=ffffff)
![Pandas](https://img.shields.io/badge/Pandas-1d1d1f?style=flat-square&logo=pandas&logoColor=0066CC&labelColor=ffffff)
![NumPy](https://img.shields.io/badge/NumPy-1d1d1f?style=flat-square&logo=numpy&logoColor=0066CC&labelColor=ffffff)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1d1d1f?style=flat-square&logo=scikit-learn&logoColor=0066CC&labelColor=ffffff)
![XGBoost](https://img.shields.io/badge/XGBoost-1d1d1f?style=flat-square&logoColor=0066CC&labelColor=ffffff)

#### Models
![Transformer](https://img.shields.io/badge/Transformer-1d1d1f?style=flat-square&labelColor=ffffff)
![CNN](https://img.shields.io/badge/CNN-1d1d1f?style=flat-square&labelColor=ffffff)
![ViT](https://img.shields.io/badge/ViT-1d1d1f?style=flat-square&labelColor=ffffff)
![YOLO](https://img.shields.io/badge/YOLO-1d1d1f?style=flat-square&labelColor=ffffff)
![U-Net](https://img.shields.io/badge/U--Net-1d1d1f?style=flat-square&labelColor=ffffff)
![ResNet](https://img.shields.io/badge/ResNet-1d1d1f?style=flat-square&labelColor=ffffff)
![BERT](https://img.shields.io/badge/BERT-1d1d1f?style=flat-square&labelColor=ffffff)
![GPT](https://img.shields.io/badge/GPT-1d1d1f?style=flat-square&labelColor=ffffff)
![Diffusion](https://img.shields.io/badge/Diffusion-1d1d1f?style=flat-square&labelColor=ffffff)

#### Agent / LLM
![LangChain](https://img.shields.io/badge/LangChain-1d1d1f?style=flat-square&logo=langchain&logoColor=0066CC&labelColor=ffffff)
![LangGraph](https://img.shields.io/badge/LangGraph-1d1d1f?style=flat-square&labelColor=ffffff)
![LangFuse](https://img.shields.io/badge/LangFuse-1d1d1f?style=flat-square&labelColor=ffffff)
![LangSmith](https://img.shields.io/badge/LangSmith-1d1d1f?style=flat-square&labelColor=ffffff)
![RAG](https://img.shields.io/badge/RAG-1d1d1f?style=flat-square&labelColor=ffffff)
![ReAct](https://img.shields.io/badge/ReAct-1d1d1f?style=flat-square&labelColor=ffffff)
![OpenAI](https://img.shields.io/badge/OpenAI-1d1d1f?style=flat-square&logo=openai&logoColor=0066CC&labelColor=ffffff)
![HuggingFace](https://img.shields.io/badge/HuggingFace-1d1d1f?style=flat-square&logo=huggingface&logoColor=0066CC&labelColor=ffffff)

#### Backend / Frontend
![FastAPI](https://img.shields.io/badge/FastAPI-1d1d1f?style=flat-square&logo=fastapi&logoColor=0066CC&labelColor=ffffff)
![Next.js](https://img.shields.io/badge/Next.js-1d1d1f?style=flat-square&logo=nextdotjs&logoColor=0066CC&labelColor=ffffff)
![React](https://img.shields.io/badge/React-1d1d1f?style=flat-square&logo=react&logoColor=0066CC&labelColor=ffffff)
![TypeScript](https://img.shields.io/badge/TypeScript-1d1d1f?style=flat-square&logo=typescript&logoColor=0066CC&labelColor=ffffff)
![SCSS](https://img.shields.io/badge/SCSS-1d1d1f?style=flat-square&logo=sass&logoColor=0066CC&labelColor=ffffff)

#### Infra / Data
![AWS](https://img.shields.io/badge/AWS-1d1d1f?style=flat-square&logo=amazonaws&logoColor=0066CC&labelColor=ffffff)
![GCP](https://img.shields.io/badge/GCP-1d1d1f?style=flat-square&logo=googlecloud&logoColor=0066CC&labelColor=ffffff)
![Docker](https://img.shields.io/badge/Docker-1d1d1f?style=flat-square&logo=docker&logoColor=0066CC&labelColor=ffffff)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1d1d1f?style=flat-square&logo=postgresql&logoColor=0066CC&labelColor=ffffff)
![Supabase](https://img.shields.io/badge/Supabase-1d1d1f?style=flat-square&logo=supabase&logoColor=0066CC&labelColor=ffffff)
![MySQL](https://img.shields.io/badge/MySQL-1d1d1f?style=flat-square&logo=mysql&logoColor=0066CC&labelColor=ffffff)
![Git](https://img.shields.io/badge/Git-1d1d1f?style=flat-square&logo=git&logoColor=0066CC&labelColor=ffffff)

<br/>

---

## 💼 경력 & 학력

```text
2025.11 – 2026.05   SK 네트웍스 Family AI 캠프 23기 (6개월)
                    AI 개발 · 모델 튜닝 · Agent · AIOps

2024.03 – 2025.10   일상이지 · 프론트엔드 개발자 (1년 8개월)
                    웹사이트 개발 · 인터랙션 · 리뉴얼 · 협업

2023.09 – 2024.03   UI/UX 프론트엔드 개발자 과정 (6개월)

2019.10 – 2023.07   지원기업 시공팀 사원 (3년 9개월)
                    배송·설치 · 품질 관리 · 고객 응대
```

<br/>

---

## 📈 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=tree0327&show_icons=true&hide_border=true&bg_color=ffffff&title_color=0066CC&icon_color=0066CC&text_color=1d1d1f" height="160" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=tree0327&layout=compact&hide_border=true&bg_color=ffffff&title_color=0066CC&text_color=1d1d1f" height="160" />

</div>

<br/>

<details>
<summary><b>📚 학습 아카이브 — SK Family AI 캠프 23기 수업 노트북 (펼치기)</b></summary>

<br/>

| 저장소 | 내용 |
|---|---|
| [LLM](https://github.com/tree0327/LLM) · [NLP](https://github.com/tree0327/NLP) | LLM · 자연어 처리 |
| [Deep-Learning](https://github.com/tree0327/Deep-Learning) · [Machine-Learning](https://github.com/tree0327/Machine-Learning) | 딥러닝 · 머신러닝 기초 |
| [MultiModal](https://github.com/tree0327/MultiModal) | 멀티모달 (CLIP · BLIP · Whisper) |
| [Analize_Data](https://github.com/tree0327/Analize_Data) · [web_crawling](https://github.com/tree0327/web_crawling) | 데이터 분석 · 웹 크롤링 |
| [web-server](https://github.com/tree0327/web-server) · [web-client](https://github.com/tree0327/web-client) | 풀스택 웹 |
| [python_mysql](https://github.com/tree0327/python_mysql) · [cloud](https://github.com/tree0327/cloud) | DB · 클라우드 실습 |
| [hyundai_faq](https://github.com/tree0327/hyundai_faq) | 현대 FAQ 크롤링 데이터셋 |
| [ai_benchmarks](https://github.com/tree0327/ai_benchmarks) | AI 엔지니어링 벤치마크 |

</details>

<br/>

---

## 📮 연락하기

<div align="center">

[![Email](https://img.shields.io/badge/superkdb0918@gmail.com-1d1d1f?style=for-the-badge&logo=gmail&logoColor=0066CC&labelColor=ffffff)](mailto:superkdb0918@gmail.com)
[![GitHub](https://img.shields.io/badge/tree0327-1d1d1f?style=for-the-badge&logo=github&logoColor=0066CC&labelColor=ffffff)](https://github.com/tree0327)

<sub>📞 010.3946.3634 · 📍 서울시 마포구 양화로 100-12</sub>

</div>
