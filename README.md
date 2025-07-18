# 💳 카드연구소: 신용카드 기획을 위한 데이터 시각화


## 🧾 프로젝트 개요
**우리는 외부 모델이나 분석 리포트에 의존하지 않고, 자체적으로 카드 소비 데이터를 분석하고 시각화하여, 그 결과에 기반해 신용카드 상품을 직접 기획했습니다.**

2023년 카드 소비 데이터를 기반으로, 타겟 고객군의 소비 성향을 분석한 후 총 3종의 신용카드를 기획하였으며, 카드별로 **전월 실적 기준**, **할인/포인트 혜택**, **권역별 특화 혜택** 등을 실제 사용자 데이터를 통해 설계하였습니다.

<br>

## 👥 팀원
<table align="center">
  <tr>
    <td align="center">
      <a href="https://github.com/kddmmm">
        <img src="https://github.com/kddmmm.png" width="100px;" alt="김동민"/><br />
        <sub><b>김동민</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/2jeong2">
        <img src="https://github.com/2jeong2.png" width="100px;" alt="이정이"/><br />
        <sub><b>이정이</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/ddddabi">
        <img src="https://github.com/ddddabi.png" width="100px;" alt="정다빈"/><br />
        <sub><b>정다빈</b></sub>
      </a>
    </td>
  </tr>
</table>

<br>

## 🎬 시나리오

> **“피사카드 기획팀 직원 3명에게 팀장이 신용카드 기획 프로젝트를 줬다.”**

<img width="700" height="700" src="https://github.com/user-attachments/assets/0024c413-f6e7-42fc-8be7-9b7c983e70b3" />

기획팀은 단순한 시장 벤치마크가 아닌, **기존 소비 데이터를 기반으로 실질적인 카드 상품을 기획**하기로 결심한다.  
우리는 데이터를 통해 사용자의 실제 소비 패턴을 파악하고, 이를 기반으로 **각 타겟별 소비 성향에 맞는 혜택 구조를 설계**한다.

<br>

## ⚙️ Tech Stack

<div>
  <img src="https://img.shields.io/badge/beats-005571?&style=flat&logo=beats">
  <img src="https://img.shields.io/badge/logstash-005571?&style=flat&logo=logstash">
  <img src="https://img.shields.io/badge/-ElasticSearch-005571?style=flat&logo=elasticsearch"> 
  <img src="https://img.shields.io/badge/Kibana-005571?&style=flat&logo=Kibana">
</div>
<br>
<img width="700" height="700" src="https://github.com/user-attachments/assets/257b769d-b1bd-4983-8649-58b5934c6f5f" />



<br>

## 📂 DataSet
| 분류 | 필드명 |
|------|--------|
| 기본 정보 | `연령대`, `성별`, `회원등급`, `직업`, `거주지역` |
| 금액 정보 | `총이용금액`, `신용카드이용금액`, `체크카드이용금액` |
| 업종별 이용금액 | `요식업`, `보험/병원`, `여행/레저`, `의류`, `주유`, ... |

> ⚠️ 해당 프로젝트는 교육용 실데이터를 기반으로 하며, 데이터셋의 상세 정보는 비공개입니다.

<br>

## 🎯 기획한 카드 상품 목록

<br>

### 1️⃣ 오늘먹카드 — *대학생 / 사회초년생 대상 신용카드*

<table>
  <tr>
    <td rowspan="6">
      <img width="250" height="250" alt="ChatGPT Image 2025년 7월 17일 오후 06_37_56" src="https://github.com/user-attachments/assets/b8bc8d53-5e59-43c0-aa26-95bd416f5156" />
    </td>
    <td><strong>💳 카드명</strong>: 오늘먹카드</td>
  </tr>
  <tr>
    <td><strong>📝 슬로건</strong>: <em>오늘도, 먹고 할인받자</em></td>
  </tr>
  <tr>
    <td><strong>🎯 타겟</strong>: 대학생, 사회초년생 (20대 중심)</td>
  </tr>
  <tr>
    <td><strong>📌 전월 실적 기준</strong>: 30만 원 이상</td>
  </tr>
  <tr>
    <td><strong>📊 주요 혜택 업종</strong>: 요식업 (식당, 배달앱, 카페)</td>
  </tr>
  <tr>
    <td><strong>💳 결제 수단</strong>: 신용카드</td>
  </tr>
</table>


#### 📈 분석 시나리오
- 대학생과 사회초년생이 주로 어떤 결제 수단을 사용하는지 파악합니다.
  - **방법**: 신용카드이용금액과 체크카드이용금액을 연령대 및 직업군(예: 대학생, 사회초년생) 기준으로 비교하여,해당 타겟층이 신용카드 중심인지 체크카드 중심인지 확인합니다.
  - **데이터 분석 결과**:
    해당 연령대(20대)의 경우 신용카드 사용 비율이 체크카드에 비해 낮은 경향을 보였습니다.  이에 따라 신용카드 사용 유도 및 활성화를 위한 카드 상품 기획이 필요하다고 판단하였고, 신용카드 중심 혜택 설계를 진행하였습니다.  

- 전월 실적 기준의 적정성을 검토합니다.
  - **방법**: 총이용금액의 평균과 분포를 확인하여, 30만 원이라는 기준이 무리 없는 수준인지 판단합니다. 이때 실적 조건이 과도하지 않도록, 데이터 기반으로 실적 기준을 수립합니다.
  - **데이터 분석 결과**: 대학생은 평균적으로 낮은 이용금액을 보였고, 사회초년생은 그보다 다소 높은 수준이었습니다. 이 두 집단의 중간값 성격을 갖는 30만 원을 전월 실적 기준으로 설정하였습니다. 이는 실적 기준이 과도하지 않으면서도 카드사의 수익성과 사용자 편의를 모두 고려한 금액입니다.

- 해당 타겟층이 실제로 어디에 돈을 많이 쓰는지를 확인합니다.
  - **방법**: 요식업, 의류, 카페, 여행/레저 등 업종별 이용금액을 비교하여, 요식업이 가장 높은 소비 비중을 차지하는지를 확인합니다.
  - **데이터 분석 결과**: 유통 업종(예: 쿠팡, 이마트 등)이 가장 높은 이용 비중을 차지했습니다. 그러나 유통 카테고리는 범위가 매우 넓고 구체적인 혜택 설계가 어려운 점이 있어, 이용금액 2위를 차지한 ‘요식업’ 카테고리를 혜택 대상으로 선정했습니다. 요식업은 대학생과 사회초년생이 일상적으로 많이 이용하는 업종이며, 타겟팅도 명확하게 가능한 만큼 할인/적립 혜택 설계에 가장 적합한 업종으로 판단되었습니다.


#### 👁️시각화
1. 대학생과 사회초년생은 신용카드와 체크카드 중 어떤 카드를 많이 쓸까?
    <details>
    <summary>📊 대학생과 사회초년생의 카드 유형별 시각화</summary>
      <img width="1865" height="357" alt="image" src="https://github.com/user-attachments/assets/12f920fe-35b9-4515-8139-2779d2405b58" />

    </details>
    
2. 대학생과 사회초년생들의 평균 이용금액 기준 적정 전월실적은 얼마일까?
    <details>
      <summary>📊 이용금액 평균 시각화</summary>
      <img width="1585" height="351" alt="image" src="https://github.com/user-attachments/assets/e8f08c8f-7e22-4f0d-b018-681105763853" />

    </details>

3. 대학생과 사회초년생들은 어떤 업종에서 가장 많이 결제할까?
    <details>
      <summary>📊 업종별 이용 비중</summary>
      <img width="913" height="665" alt="image" src="https://github.com/user-attachments/assets/780f65a2-4a75-4e43-971c-acb40b872c8a" />

    </details>

#### 💳 카드 혜택

| 항목 | 혜택 내용 |
| --- | --- |
| 🍜 요식업 업종 할인 | 일반 음식점, 패스트푸드, 프랜차이즈 카페 등 요식업종 10% 청구할인 (월 최대 10,000원) |
| 🛵 배달앱 추가 혜택 | 배달의민족, 요기요 결제 시 5% 추가 할인 (월 최대 30,000원) |
| ☕ 카페 포인트 적립 | 전월 실적 50만 원 이상 시 커피전문점 2% 포인트 적립 |

<br>

---

### 2️⃣ 이제 쉼 카드 — *은퇴자 대상 트래블 신용카드*

<table>
  <tr>
    <td rowspan="6">
      <img width="250" height="250" src="https://github.com/user-attachments/assets/3ebcca41-6b3b-470d-a114-4d60f307d5d9" />
    </td>
    <td><strong>💳 카드명</strong>: 이제 쉼 카드</td>
  </tr>
  <tr>
    <td><strong>📝 슬로건</strong>: <em>이제는 쉬자!</em></td>
  </tr>
  <tr>
    <td><strong>🎯 타겟</strong>: 은퇴자</td>
  </tr>
  <tr>
    <td><strong>📌 전월 실적 기준</strong>: 30만 원 이상</td>
  </tr>
  <tr>
    <td><strong>📊 주요 혜택 업종</strong>: 여행(비행기/숙박/여행자보험)</td>
  </tr>
  <tr>
    <td><strong>💳 결제 수단</strong>: 신용카드</td>
  </tr>
</table>

#### 📈분석 시나리오

- 이용고객 중 은퇴자 비율과, 은퇴자 주 연령대를 파악합니다.

  - **방법** : 총 회원 수와 직업군이 은퇴자인 사람을 기준으로 비교하여, 타켓층 비율이 적은지 확인합니다.
  - **데이터 분석 결과** : 해당 연령대(70세 이상)의 경우 카드 회원 중 은퇴자 직업군이 현저히 낮은 것을 알 수 있었습니다.  
    이에 따라 카드  사용이 적은 직업군인 '은퇴자'를 타켓으로, 직장에서의 삶으로 부터 벗어난 '쉼'을 장려하는 카드를 기획하게 되었습니다.

- 은퇴한 연령대가 여행/레져/문화분야에 소비하는 비율을 파악합니다.

  - **방법**: 모든 연령대 중 은퇴자인 직업군을 기준으로 여행/레져/문화 분야에 소비하는 금액을 비교합니다.
  - **데이터 분석 결과**: 은퇴자의 여행 소비 비율 중 80%이상이 0값을 나타냅니다. 따라서 은퇴자들을 위한 트래블 카드를 출시하여 고객유치를 도모하고자 합니다.

- 은퇴자들의 총 카드 이용요금을 파악합니다.

  - **방법**: 은퇴자 직업군을 기준으로 카드 총 이용요금 평균을 도출합니다.
  - **데이터 분석 결과**: 은퇴자를 위한 트래블 카드를 출시하고자 하였을 때 혜택을 주기위한 기준이 필요했습니다.  
    더 많은 카드사용을 장려하는 기획이기 때문에 은퇴자들의 카드 총 이용요금 평균인 22만원보다 높은 30만원을 전월실적 기준으로 설정하였습니다.
  

#### 👁️시각화

1. 카드 회원 중 은퇴자의 비율은 얼마나 될까? 
    <details>
    <summary>📊총 회원 중 은퇴자 비율 </summary>
      <img width="1002" height="487" alt="회원 중 은퇴자 비율" src="https://github.com/user-attachments/assets/b662d32d-ad20-4dc1-aced-d6f78e6617fc" />
    </details>


2.  은퇴자의 주 연령대는 어떻게 될까?
    <details>
    <summary>📊연령별 은퇴자 비율 </summary>
      <img width="1000" height="491" alt="은퇴자 주 연령대" src="https://github.com/user-attachments/assets/fd620a61-0ea5-4dd9-871a-edf6cd57ba29" />

    </details>

3.  은퇴자인 회원들의 카드 총 이용금액 평균은 얼마일까?
    <details>
    <summary>📊은퇴자 총 이용금액 </summary>
    ><img width="1003" height="485" alt="은퇴자 총 카드 이용요금 평균" src="https://github.com/user-attachments/assets/e23dfaa9-1a33-4285-9418-77ba0712967e" />

    </details>

4.  은퇴자 중 여행/레져/문화 분야에 소비하는 소비금액은 얼마일까?
    <details>
    <summary>📊은퇴자 중 여행/레져/문화 분야 소비금액 </summary>
    <img width="1034" height="575" alt="은퇴자 여행 소비 비율" src="https://github.com/user-attachments/assets/b3e56337-810e-48ad-8925-eaacffcc8c8d" />
    </details>

#### 🎁 카드 기본 혜택

| 항목 | 혜택 내용 |
| --- | --- |
| ✈️ 항공권 할인 | 국내/국외 항공권 5~10% 할인 (연 4회) |
| 🏨 숙박 제휴 | 주요 호텔, 리조트 10% 할인 또는 조식 무료 제공 |
| 🚕 공항 이동 | 공항 리무진 또는 택시비 1만원 할인 (왕복/연 2회) |
| 🩺 여행자 보험 | 자동 가입 (의료비, 수화물 지연 포함) |

#### 🌿 은퇴자 특화 혜택

- **웰니스 여행지 가이드북 무료 제공** (연 1회)
- **국내 힐링 프로그램 (요가, 명상, 찜질 스파 등)** 할인

#### 💵 월 사용금액 기반 페이백 혜택 (월 1회 자동 지급)

- 전월 실적 30만원 이상 시 5000원 페이백
- 전월 실적 50만원 이상 시 10000원 페이백
- 전월 실적 100만원 이상 시 25,000원 자유 여행 적립금 or 카드 청구 할인

<br>

---

### 3️⃣ 지역별 맞춤형 카드

#### 📈 분석 시나리오
- 각 지역별 카드 사용 내역을 분석하여, 어떤 업종에서 카드 사용 비율이 높은지를 파악합니다.
- 지역별 카드 사용 데이터를 바탕으로 가장 많이 결제된 업종을 분석하여, 혜택을 맞춤화할 수 있는 업종을 선정합니다.
- 각 지역의 주요 업종에 맞춰 카드 혜택을 설계합니다.

#### 👁️시각화
1. 지역별로 전월실적을 다르게 해야할까?
   <details>
     <summary>📊지역별 카드 사용 금액 비율 </summary>
      <table>
      <tr>
        <td align="center">
          <img width="553" height="485" alt="Image" src="https://github.com/user-attachments/assets/76afa6c2-8781-4b05-8aa3-909680bdebb6" />
        </td>
        <td align="center">
          <img width="535" height="233" alt="Image" src="https://github.com/user-attachments/assets/04b5068d-1bc7-4f2c-8bfd-fc1524c4a4a6" /
        </td>
      </tr>
    </table>
     -> 각 지역별 카드 사용 내용을 분석했을 때, 큰 차이가 없음을 알 수 있었습니다.
     
     -> 전체 평균 사용 금액보다 상회한 40만원으로 설정했습니다.
    </details>
    
    
   

3. 지역별로 분야마다 사용금액에 차이가 있을까?
   <details>
     <summary>📊각 거주지별 분야 평균 사용 금액 </summary>
      <table>
      <tr>
        <td align="center">
          <img width="800" height="491" alt="Image" src="https://github.com/user-attachments/assets/e38f7ef4-9b36-4700-8e21-d24cc223d8c7" />
        </td>
        <td align="center">
          <img width="817" height="485" alt="Image" src="https://github.com/user-attachments/assets/6ee19549-0695-40bb-b987-85d11954111f" />
        </td>
      </tr>
    </table>
     
     -> 전체적으로 봤을 때, 분야별로 사용금액에 차이가 있음을 알 수 있었습니다.
    </details>
    
    

4. 각 분야별로 봤을 때, 유의미한 결과가 있을까?
   <details>
     <summary>📊각 분야 및 거주지별 평균 사용 금액 차이 </summary>
     <table>
      <tr>
        <td align="center">
          <img width="815" height="482" alt="Image" src="https://github.com/user-attachments/assets/58a7fb5a-ad86-44e0-8b4a-a36e254b7422" />
        </td>
        <td align="center">
          <img width="806" height="488" alt="Image" src="https://github.com/user-attachments/assets/5cc94572-d4fd-4e72-85a2-4919a944130f" />
        </td>
      </tr>
    </table>
     
     -> 몇 가지 분야에서 지역별로 사용하는 금액의 차이가 있음을 알 수 있었습니다.
   
     -> 각 지역별로 2가지의 특정 업종에서 혜택을 줄 수 있도록 설정했습니다.
    </details>
    
    

#### 🎁 카드 기본 혜택

| 항목 | 혜택 내용 |
| --- | --- |
| 💳 해당 지역 사용 | 해당 카드를 해당 지역에서 사용시 업종별 2~8% 청구 할인 |
| 🚕 타 지역 사용 | 해당 카드를 타 지역에서 사용시 업종별 1~5% 청구 할인 |

#### 지역별 혜택 카드

<details>
  <summary>🗺️영남권 </summary>
    <table>
      <tr>
        <td rowspan="5">
          <img width=250" height="380" alt="Image" src="https://github.com/user-attachments/assets/29195a9c-62d9-48ca-8c9f-efc073d6c47d" />
        </td>
        <td><strong>💳 카드명</strong>: 마 니 카드맞나?</td>
      </tr>
      <tr>
        <td><strong>🎯 타겟</strong>: 경북, 경남, 부산, 울산, 대구</td>
      </tr>
      <tr>
        <td><strong>📌 전월 실적 기준</strong>: 40만 원 이상</td>
      </tr>
      <tr>
        <td><strong>📊 주요 혜택 업종</strong>: 유통, 자동차, 보험/병원</td>
      </tr>
      <tr>
        <td><strong>💳 결제 수단</strong>: 신용카드</td>
      </tr>
    </table>
</details>

<details>
  <summary>🗺️호남권 </summary>
    <table>
      <tr>
        <td rowspan="5">
          <img width=250" height="380" alt="Image" src="https://github.com/user-attachments/assets/d05c9ab6-773b-4c20-b5d9-6302bd046cbe" />
        </td>
        <td><strong>💳 카드명</strong>: 아따 이 카드 갖고 뭐더냐</td>
      </tr>
      <tr>
        <td><strong>🎯 타겟</strong>: 광주, 전북, 전남</td>
      </tr>
      <tr>
        <td><strong>📌 전월 실적 기준</strong>: 40만 원 이상</td>
      </tr>
      <tr>
        <td><strong>📊 주요 혜택 업종</strong>: 유통, 여행, 건축</td>
      </tr>
      <tr>
        <td><strong>💳 결제 수단</strong>: 신용카드</td>
      </tr>
    </table>
</details>

<details>
  <summary>🗺️수도권 </summary>
    <table>
      <tr>
        <td rowspan="5">
          <img width=250" height="380" alt="Image" src="https://github.com/user-attachments/assets/ff747da1-59f8-4f27-9801-f9671b26f4ed" />
        </td>
        <td><strong>💳 카드명</strong>: 이거 카드 맞그든요</td>
      </tr>
      <tr>
        <td><strong>🎯 타겟</strong>: 서울, 경기, 인천, 강원</td>
      </tr>
      <tr>
        <td><strong>📌 전월 실적 기준</strong>: 40만 원 이상</td>
      </tr>
      <tr>
        <td><strong>📊 주요 혜택 업종</strong>: 유통, 서적/학원, 요식업</td>
      </tr>
      <tr>
        <td><strong>💳 결제 수단</strong>: 신용카드</td>
      </tr>
    </table>
</details>

<details>
  <summary>🗺️충청권 </summary>
    <table>
      <tr>
        <td rowspan="5">
          <img width="250" height="380" alt="Image" src="https://github.com/user-attachments/assets/24e31747-8ab7-4683-b37b-3d31c35c8250" />
        </td>
        <td><strong>💳 카드명</strong>: 이거 카드 맞아유~</td>
      </tr>
      <tr>
        <td><strong>🎯 타겟</strong>: 충북, 충남, 대전, 세종</td>
      </tr>
      <tr>
        <td><strong>📌 전월 실적 기준</strong>: 40만 원 이상</td>
      </tr>
      <tr>
        <td><strong>📊 주요 혜택 업종</strong>: 유통, 서적/학원, 의류/잡화</td>
      </tr>
      <tr>
        <td><strong>💳 결제 수단</strong>: 신용카드</td>
      </tr>
    </table>
</details>

<details>
  <summary>🗺️제주도 </summary>
    <table>
      <tr>
        <td rowspan="5">
          <img width="250" height="380" alt="Image" src="https://github.com/user-attachments/assets/62e6a370-2026-4d61-9700-4a8ccda35b29" />
        </td>
        <td><strong>💳 카드명</strong>: 카드 맞수까?</td>
      </tr>
      <tr>
        <td><strong>🎯 타겟</strong>: 제주</td>
      </tr>
      <tr>
        <td><strong>📌 전월 실적 기준</strong>: 40만 원 이상</td>
      </tr>
      <tr>
        <td><strong>📊 주요 혜택 업종</strong>: 여행(비행기/숙박/여행자보험)</td>
      </tr>
      <tr>
        <td><strong>💳 결제 수단</strong>: 신용카드</td>
      </tr>
    </table>
</details>

<br>

## 트러블 슈팅

### 🎯 파이프라인 구축 시도

#### ⚙️시도 1: 컬럼 필터링 및 전처리

<img width="478" height="102" alt="Image" src="https://github.com/user-attachments/assets/423b6a5c-c0f6-49a4-8628-6e80885fae13" />

원본 CSV 파일에는 약 55개 이상의 필드가 존재합니다. 분석 및 시각화 목적에 부합하지 않는 약 40개 컬럼을 filter 단계에서 제거하도록 구성하였습니다. 그러나 필터링 이후, Logstash 파이프라인 처리 데이터 용량이 오히려 약 75% 증가하는 현상이 발생하였습니다.

**📌 원인 분석**

필드를 제거했음에도 불구하고, Logstash가 자동으로 생성하는 host, agent, @timestamp 등의 메타 필드가 포함되면서,
 필드 구조가 오히려 더 복잡해지고 JSON 구조가 커지게 되어 데이터 용량이 증가한 것으로 판단됩니다.
 
#### ⚙️시도 2: CSV 파일의 message 필드 분할 시도

<img width="914" height="399" alt="Image" src="https://github.com/user-attachments/assets/b6c26106-255a-4816-8e86-d4d33ac69d8a" />

Logstash는 기본적으로 CSV 한 줄 전체를 message 필드로 저장합니다. 이에 따라, 해당 필드를 , 기준으로 분할(split) 하여 개별 필드로 나누는 방식으로 시도하였습니다. 이 방식으로 message 필드가 분할되는 것은 확인하였으나, Elasticsearch 인덱싱 시 각 필드가 정상적으로 매핑되지 않는 문제점이 발견되었습니다.

#### ⚙️시도 3: message 필드 정상 생성 확인

<img width="404" height="157" alt="Image" src="https://github.com/user-attachments/assets/ea1da8b5-7102-451f-bab7-10896d403672" />

split과 add_field를 통해 필드가 생성된 것처럼 보였지만, 실제 구조는 내부적으로 문자열 배열(String Array) 형태로 처리되고 있었습니다. 

또한 message 필드로 인해 용량이 커지는 현상이 발생하였습니다.
 
#### 🔧 해결 방향

<img width="865" height="248" alt="Image" src="https://github.com/user-attachments/assets/53a50208-ec1e-4349-a54c-5c0249f2418d" />

CSV 데이터는 , 구분자 순서가 조금만 달라도 전체 필드 매핑이 망가질 수 있습니다. 따라서 자동 파싱보다는 명확하게 각 필드를 수동으로 지정하는 방식이 보다 안정적입니다


## 🤔 회고

### 김동민
ELK 구축의 실패가 매우 아쉬웠다. 새로운 방식의 도입이 필요하다고 판단했지만, 충분한 사전 조사를 하지 않은 채 진행했던 점이 큰 실수였다. 기존에 익숙한 방식에서 벗어나 새로운 기술을 적용하기 전에는 반드시 미리 충분히 조사하고, 가능한 리스크를 파악하는 습관을 가져야겠다는 중요한 교훈을 얻었다.

### 이정이
kibana를 통한 데이터 분석을 통해 데이터를 더 다각도로 바라보고, 향후 파이프 라인을 구축하기 위해 logstash와 filebeat를 활용해 봐야겠다고 느꼈다.

### 정다빈
실제 데이터를 기반으로 소비 패턴을 분석하고, 그 결과를 바탕으로 신용카드를 기획하는 과정을 통해 데이터 분석이 실무에 어떻게 활용되는지 체감할 수 있어 의미 있는 경험이었다. 또한, 데이터 기반 의사결정의 중요성과 재미를 동시에 느낄 수 있었다.
