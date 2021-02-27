# DACON_KCB_Financial-Style-Visualization

해당 공간은 [DACON KCB 금융스타일 시각화 대회](https://dacon.io/competitions/official/82407/overview/)에 참여한 코드를 저장하기 위한 공간입니다.

해당 코드에 대한 저작권은 시로앤마로(김이정, 안지민, [이인섭](https://github.com/insub789), [이형선](https://github.com/traceofpassion), [주은혁](https://github.com/EunHyeok-Ju))에게 있습니다.

주관 : [데이콘](https://dacon.io) / 주최 : KCB

# 1. 대회 설명

KCB는 다양한 금융사로부터 여신거래 기록, 채무 정보, 연체정보 등  다양한 고객 금융 정보를 받아 전국민 85.4%인 4,400만 경제활동 인구의 경제 활동 데이터를 보유하고 있음

이러한 데이터를 활용하여 다음과 같은 목적으로 대회 주최

1. KCB 전국민 금융 데이터의 새로운 인사이트 발굴
2. 활용도 높은 결과물로 금융친화적 콘텐츠 발전에 기여


## 1.1. 데이터 설명

### 1.1.1 제공 데이터
* credit_card_data.csv : 전국민 카드 및 대출 이용통계 데이터
* jeju_financial_life_data.csv : 지역 거주지(제주도) 금융라이프 데이터

### 1.1.3 외부 데이터
* jeju_zipcode_db.txt : [우편번호 공공사이트](https://www.epost.go.kr/search/zipcode/areacdAddressDown.jsp)에서 우편번호 다운로드
* extr_2016.txt / extr_2017.txt : [마이크로데이터 통합서비스(MDIS)](http://mdis.kostat.go.kr/)에서 16,17년도의 지역별고용조사 데이터 활용

### 1.1.2 산출 데이터

* mdis_data.csv : 마이크로데이터 통합서비스 외부 데이터 전처리 후 산출물
* credict_data.csv : credict_card_datd에 대한 전처리 후 산출물
* sample_data.csv : Tabeau에 활용하기 위해 제작한 샘플 데이터

## 1.2. 데이터 처리 과정

데이터 수집 - 데이터 전처리 - Feature Engineering - Visualization - Verification

## 1.3. 주제 선정 배경

자신의 소비성향과 신용상태에 영향을 줄 수 있는 요인에 대해서 판단할 수 있는 기회가 부족하다고 판단

저희는 개인들이 자신의 신용점수를 포함하여 여러 항목들을 비교해볼 수 있는 기회를 제공하고 , 

이에 따른 자신의 금융유형을 파악하여 미래에 대한 계획을 세울 수 있도록 하고자 했습니다.


# 2. 데이터 분석

## 2.1. Feature Engineering

사람들에 대한 새로운 금융유형을 제작하기 위해 다음과 같은 변수 생성
* 소득대비 카드 사용량 
* 비은행 대출 비율

## 3. 시각화

## 3.1. 금융유형

사람들의 금융 소비 유형에 따라 다음과 같이 유형의 이름을 매칭

<img src="https://user-images.githubusercontent.com/64209837/109381489-097b7e00-791e-11eb-9f8f-f85ec0931b6a.jpg" width="50%" height="50%">
<img src="https://user-images.githubusercontent.com/64209837/109381492-0aacab00-791e-11eb-9bfb-54bc48cc82e3.jpg" width="50%" height="50%">
<img src="https://user-images.githubusercontent.com/64209837/109381493-0aacab00-791e-11eb-877c-143d3dd39c40.jpg" width="50%" height="50%">
<img src="https://user-images.githubusercontent.com/64209837/109381494-0b454180-791e-11eb-9a41-9f647f25c43a.jpg" width="50%" height="50%">

개인의 소비형태에 따라 금융유형을 제시

## 3.2. 전국민 데이터 Tableau

[Tableau](https://en.wikipedia.org/wiki/Tableau_Software)는 시각화 도구로서 동적인 시각화를 표현할 수 있고, 간편하게 활용할 수 있다.

이를 활용하기 위해서 샘플 데이터를 제작하여서 데이터에 따라 개인과 집단과의 비교가 두드러지게 표현함.

![태블로 화면](https://user-images.githubusercontent.com/64209837/109381297-ee5c3e80-791c-11eb-9eca-11f0ec715a34.png)

[credit data Tableau Link](https://public.tableau.com/profile/.19960903#!/vizhome/KCB____15626060032900/sheet0)

## 3.3. Jeju

전국민 금융 데이터를 활용해서 얻은 인사이트를 활용하여 제주 데이터에 대입

제주 데이터는 개인의 데이터가 아닌 지역별 데이터로서, 지역별로 금융 유형을 나누어 표현

![제주 tableau 화면](https://user-images.githubusercontent.com/64209837/109381807-d20dd100-791f-11eb-8254-3a543f566e5b.png)

[jeju data Tableau Link](https://public.tableau.com/profile/.19960903#!/vizhome/-2030/1)

## 3. 후기

금융 데이터를 다루어 새로운 금융 유형을 만들었다는 점이 흥미로웠음.

R이 아닌 새로운 Tableau라는 강력한 시각화 툴을 공부하게 된 계기가 되었음.

각 유형별로 상품을 추천해주거나, 피드백에 대한 부분이 아쉬웠음.

## 3.2. 결과

![최종 결과](https://user-images.githubusercontent.com/64209837/109381880-45afde00-7920-11eb-89ab-f76fe6042cc5.png)

최종 3등으로 수상

## 폴더 구조

```sh

├─Github
│  │  README.md
│  ├─code
│  │      01.credit_card 전처리.Rmd
│  │      02.제주도 전처리.Rmd
│  └─data
│         credit_data.csv
│         extr_2016.txt
│         extr_2017.txt
|         jeju_summ.csv
|         jeju_with_zipcode.csv
|         jeju_zipcode_db.txt
|         mdis_data.csv
|         num_opencard.csv
|         sample_data.csv
│  └─img
│         funds.png
|         hand-shake.png
|         감귤.png
|         눈앞캄캄.jpg
|         알뜰살뜰.jpg
|         위태위태.jpg
|         제목.png
|         흥청망청.jpg
│  └─output
│         01.데이콘 보고서.pdf
|         2.KCB_금융데이터_시각화_시로앤마로.twbx
|         3.제주도 시각화.twbx
|

```

