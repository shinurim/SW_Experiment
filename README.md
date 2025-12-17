<h2>🎬DB Bridge</h2>
자연어 질의를 통한 고품질의 패널 추출

▶️ [GitHub에서 시연 영상 바로 재생하기](https://github.com/shinurim/SW_BE/issues/1#issue-3734958059)

<hr>

<h2>Preview</h2>
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
<hr>

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
git clone https://github.com/shinurim/SW_Experiment.git
cd SW_Experiment
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

<h2>🔑Key Features</h2>
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
  카테고리 분류에 있어 주관을 최대한 배제하기 위해 zero-shot 분류 진행
* 실험 결과:
  대표적으로 정의된 7가지 카테고리를 기준으로 분류를 수행<br>
  질문에 따라 복수의 카테고리가 도출되는 경우, 보기 항목에 대해 재분류를 진행하였고 그 결과 각 메인 카테고리 및 서브 카테고리 분류에 성공함
  
<h3> 🫡 Loyalty Algorithm</h3>

* 충성도 알고리즘의 필요성:
  적합한 패널이 과도하게 확보되는 경우, 데이터 품질 유지를 위해 평소 설문에 성실히 응답한 패널을 우선적으로 선별
* 충성도 알고리즘의 구현법:
  패널이 질의에 응답한 수를 기준으로 응답한 수가 많으면 충성도를 높게, 적으면 충성도를 낮게 부여

<h3> 🤖 Prompt_N_Rag Experiment</h3>

* 도메인 특화 문서 임베딩:
  기존에 작성한 도메인 특화 문서를 위의 실험에서 메인 임베딩 모델로 선정된 KURE-v1으로 임베딩
* 청킹 기준:
  문서 분할 조건을 300 token 기준으로 자르고 30 token을 오버랩
* 벡터 DB:
  임베딩 한 결과를 Chroma DB에 저장
* 프롬프트 설계:
  역활 부여 및 자연어 질의를 SQL,Opinion,Main,Sub 형태로 변환할 수 있는 규칙 제시

<h3> 🧠 Embedding Aggregation Pipeline</h3>

* 입력 데이터:
  문항별 임베딩이 저장된 Pickle 파일 로드(uid × 문항 × embedding 구조)
* 카테고리 매핑:
  문항(qid)을 기준으로 main / sub 카테고리 매핑 적용
* 임베딩 집계:
  동일 사용자(uid) 내에서 main / sub 기준 문항 임베딩 평균 계산
* 추적 정보 기록:
  각 sub 평균 벡터 생성에 사용된 문항 라벨(qids_used) 기록
* 벡터 직렬화:
  평균 임베딩을 문자열 벡터 형태로 직렬화
<hr>

<h2>License</h2>
<p>본 프로젝트는 한성대학교 기업연계 SW캡스톤디자인 수업에서 진행되었습니다.</p>
