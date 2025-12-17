<h2>🎬DB Bridge</h2>
자연어 질의를 통한 고품질의 패널 추출

▶️ [GitHub에서 시연 영상 바로 재생하기](https://github.com/shinurim/SW_BE/issues/1#issue-3734958059)

<hr>

<h2>👀Preview</h2>
<p align="center">
  <img src="./assets/판넬.png" width="900" />
</p>
<hr>

<h2>👥 Members</h2>

<table align="center" cellpadding="14">
  <tr>
    <td align="center">
      <img src="./members/yurim.png"
           width="140" height="140"
           style="border:2px solid #ddd;border-radius:12px;object-fit:cover;" />
      <div style="margin-top:8px;font-weight:600;">
        <a href="https://github.com/shinurim">신유림</a>
      </div>
    </td>
    <td align="center">
      <img src="./members/mint02123.png"
           width="140" height="140"
           style="border:2px solid #ddd;border-radius:12px;object-fit:cover;" />
      <div style="margin-top:8px;font-weight:600;">
        <a href="https://github.com/mint02123">민재영</a>
      </div>
    </td>
    <td align="center">
      <img src="./members/jonghwa-8620.png"
           width="140" height="140"
           style="border:2px solid #ddd;border-radius:12px;object-fit:cover;" />
      <div style="margin-top:8px;font-weight:600;">
        <a href="https://github.com/jonghwa-8620">박종화</a>
      </div>
    </td>
    <td align="center">
      <img src="./members/suheon98.png"
           width="140" height="140"
           style="border:2px solid #ddd;border-radius:12px;object-fit:cover;" />
      <div style="margin-top:8px;font-weight:600;">
        <a href="https://github.com/suheon98">조수헌</a>
      </div>
    </td>
    <td align="center">
      <img src="./members/rokiosm.png"
           width="140" height="140"
           style="border:2px solid #ddd;border-radius:12px;object-fit:cover;" />
      <div style="margin-top:8px;font-weight:600;">
        <a href="https://github.com/rokiosm">문경록</a>
      </div>
    </td>
  </tr>
</table>

<h2> 🛠 Tech Stack </h2> 

* Python - 서버 런타임

* Django - 백엔드 웹 프레임워크
 
* React + Vite - 프론트엔드
 
* OpenAI GPT-4o - LLM (메인 추론 모델)
 
* Anthropic Claude Opus 4.1 - LLM (고성능 추론 모델)

* KURE-v1 - 한국어 특화 벡터 임베딩
  
* PostgreSQL + pgvector - 벡터 데이터베이스

* Docker - 컨테이너 및 배포 환경
<hr>

<h2> 🔗 Getting Started </h2>  

### Installation

```bash
# 저장소 클론 (Clone Repository)
git clone https://github.com/hansung-sw-capstone-2025-2/2025_8_B_Experiment.git
cd 2025_8_B_Experiment

# 가상환경 생성 및 활성화
python -m venv venv

# 의존성 설치
pip install -r requirements.txt

### Environment Variables
# AI & LLM API Keys
OPENAI_API_KEY=sk-proj-xxxx...
ANTHROPIC_API_KEY=sk-ant-api03-xxxx...

# Database (PostgreSQL + pgvector)
DB_ENGINE=django.db.backends.postgresql
DB_NAME=your_db_name
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
<hr>

<h2> Key Features </h2>



