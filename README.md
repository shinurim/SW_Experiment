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

<hr>

<h2> 🚀 Getting Started </h2>  

<h3> Installation </h3>
<pre><code># 저장소 클론 (Clone Repository)
git clone https://github.com/hansung-sw-capstone-2025-2/2025_8_B_Experiment.git
cd 2025_8_B_Experiment
</code></pre>
<pre><code># 가상환경 생성 및 활성화
python -m venv venv
</code></pre>
<pre><code># 의존성 설치
pip install -r requirements.txt
</code></pre>

<h3> Environment Variables</h3>
<pre><code># AI & LLM API Keys
OPENAI_API_KEY=Your_OpenAI_key
ANTHROPIC_API_KEY=Your_ClaudeAI_key
# Database (PostgreSQL + pgvector)
DB_ENGINE=django.db.backends.postgresql
DB_NAME=your_db_name
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
</code></pre>
<hr>

<h2>Key Features</h2>

### 📊 Embedding Performance Analysis

* 모델 비교 실험:
  범용 모델인 Dragon Embedding과 한국어 특화 모델 KURE-v1의 성능 비교 수행
* 한국어 문맥 인식:
  KURE-v1이 Dragon 대비 한국어 쿼리 처리에서 더 높은 정확도를 보임
* 검색 품질 평가:
  동일한 질의에 대해 KURE-v1이 사용자 의도에 더 부합하는 문서를 상위에 노출
* 최종 모델 선정:
  실험 결과를 바탕으로 프로젝트의 메인 임베딩 모델로 KURE-v1 채택
* 카테고리 분류:
  카테고리 분류를 공적인 기준으로 하기 위해 zero-shot 분류 진행
* 실험 결과:
  대표적으로 분류되는 7가지 종류의 명시된 카테고리에 따라서 분류가 되었으며 질문에 따라서 카테고리가 여러가지 나올 수 있는 경우 보기에 대해서 재 분류를 실행했고, 결과적으로 각 메인 카테고리와 서브카테고리를 분류하는데 성공함
  
<hr>
