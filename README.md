# Amazon_review_analysis

### Amazon 리뷰 (텍스트)데이터 크롤링
- 사용기법 : 셀레니움 bs4 혼합
  - 과정 : 별점별 find_all로 span data-hook 텍스트 100개 이상 다음 페이지로 넘기면서 추출 후 tsv로 저장
  - 고찰 : time.sleep을 랜덤하게 하지 않으면 크롤링할 때 페이지 차단됨 + 다음 페이지 수를 제한을 해야 페이지 차단이 안됨

 ### Amazon 리뷰 분석
 - 사용 기법
1) 소문자 변환
2) 토큰화
   
▪ 등장 빈도가 10회 미만인 토큰은 삭제

▪ 길이가 2자 이하인 토큰은 삭제

▪ nltk에서 제공하는 불용어(stopwords)는 모두 제거.

▪ 각 토큰에 대해 표제어(lemmatization) 처리

3) 빈도 분석


### 감성 분석
- 사용 기법 :
  - SentimentIntensityAnalyzer
  - 별점별 긍정,부정 리뷰를 집계 후 시각화
 
