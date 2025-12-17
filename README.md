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
<pre><code># LLM API KEY
ANTHROPIC_API_KEY=your_claude_api_key
OPENAI_API_KEY=your_openai_api_key
</code></pre>
<hr>

<h2>📌Key Features</h2>
 <h3>📊 Embedding Performance Analysis</h3>

* 모델 비교 실험:
  범용 모델인 Dragon Embedding과 한국어 특화 모델 KURE-v1의 성능 비교 수행
* 한국어 문맥 인식:
  KURE-v1이 Dragon 대비 한국어 쿼리 처리에서 더 높은 정확도를 보임
* 검색 품질 평가:
  동일한 질의에 대해 KURE-v1이 사용자 의도에 더 부합하는 문서를 상위에 노출
* 최종 모델 선정:
  실험 결과를 바탕으로 프로젝트의 메인 임베딩 모델로 KURE-v1 채택

<h3>📋 Category Classification Analysis</h3> 

* 카테고리 분류:
  카테고리 분류를 공적인 기준으로 하기 위해 zero-shot 분류 진행
* 실험 결과:
  대표적으로 분류되는 7가지 종류의 명시된 카테고리에 따라서 분류가 되었으며 질문에 따라서 카테고리가 여러가지 나올 수 있는 경우 보기에 대해서 재 분류를 실행했고, 결과적으로 각 메인 카테고리와 서브카테고리를 분류하는데 성공함
  
<h3> 🫡 Loyalty Algorithm</h3>

* 충성도 알고리즘의 필요성:
  사용자의 질의에 해당하는 패널이 필요 이상으로 많을 경우 평소 설문에 충실히 응답을 했던 패널을 추천해하 함
* 충성도 알고리즘의 구현법:
  패널이 지금까지 질의에 응답한 수를 기준으로 응답한 수가 많으면 충성도가 높게, 응답한 수가 적으면 충성도가 낮게 나오도록 조정함

<h3> 🤖 Prompt_N_Rag Experiment</h3>

* chunk_size:
  문서 분할 조건을 300 token 기준으로 자르고 30 token을 오버랩 하였음
* Documnet Embdding:
  기존에 작성한 도메인 문서를 위의 실험에서 메임 임베딩 모델로 선정된 KURE-v1으로 임베딩 함
* Load Saved VectorDB:
  임베딩 한 결과를 Chroma DB에 저장함 
* Prompt:
  역활 부여 및 SQL (meta query) 규칙
  직군(Work/Job) 데이터 규칙
  오피니언 (opinion) 및 해시태그 규칙
  최종 출력 규칙
  출력예시 (FewShot) 제시
