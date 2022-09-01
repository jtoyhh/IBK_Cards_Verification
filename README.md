# <font size = "20">기업카드 건전성지표 발굴‧검증</font>
### ==================================================================

### 과제 목표

* 기업카드회원의 부실/정상을 예측하는 AI모형설계
* 학습데이터셋으로 모형 학습 후 테스트데이터로 결과 예측

#### 데이터셋 구성

* 학습데이터(Train.csv) : 기업회원 2,000개 (연체 1,000개,  정상 1,000개) --- label 있음
* 테스트데이터(Test.csv) : 기업회원 400개 (연체 200개, 정상 200개) --- label 없음

#### ----------------------------------------------------------------------------------------------------------------
#### 변수 설명
* <b>행구분번호 : 전산고객번호</b>
* <font color='yellow'><b>이진형(0, 1) 변수 (binary type)  -- 결측치 확인 및 수치변환 필요</b></font>
* <font color='red'><b>수치형 변수 (Continuous type) -- 값의 범위 파악 및 스케일링 필요</b></font>
* <font color='green'><b>시계열형 변수 (Time Series type) -- 수치형과 동일 + 시계열 파생지표 신규</b></font>
* <font color='purple'><b>범주형 변수 (Categorical type) -- 수치변환 or One-Hot Encoding 필요</b></font>

#### ----------------------------------------------------------------------------------------------------------------
* <b>FK00  : 전산고객번호</b>
* <font color='yellow'><b>BIN01 : 관리대상업종 여부</b></font>
* <font color='yellow'><b>BIN02 : 기업불량정보_최근6개월내 당타행 연체일수 5일이상 여부</b></font>
* <font color='yellow'><b>BIN03 : 대표자불량정보_대표자 최근6개월내 당타행 5일이상 계속연체 이력존재 여부</b></font>
* <font color='yellow'><b>BIN04 : 기업불량정보_최근6개월내 불량사고코드 등재이력 여부</b></font>
* <font color='yellow'><b>BIN05 : 재무정보_매출액 30%이상 감소여부</b></font>
* <font color='red'><b>CON01 : 이용행태정보_최근6개월내 상품권 구입금액</b></font>
* <font color='red'><b>CON02 : 이용행태정보_최근6개월내 유흥주점 이용금액</b></font>
* <font color='red'><b>CON03 : 전월 카드이용한도</b></font>    
* <font color='red'><b>CON04 : 전월 할부이용금액</b></font>    
* <font color='red'><b>CON05 : 전월 대표자 현금서비스 이용금액</b></font>
* <font color='red'><b>CON06 : 전월 대표자 장기카드대출 이용금액</b></font>
* <font color='red'><b>CON07 : 전월 카드한도 소진율</b></font>
* <font color='red'><b>CON08 : 리스크등급별 불량율</b></font>
* <font color='red'><b>CON09 : 전월말기준 1개월 요구불예금 평잔</b></font>  
* <font color='red'><b>CON10 : 전월말기준 1개월 총수신(외화예금, 신탁, MMDA 포함) 평잔</b></font> 
* <font color='green'><b>TIM01 : 기업카드 계정잔액_M-2</b></font>
* <font color='green'><b>TIM02 : 기업카드 계정잔액_M-1</b></font>
* <font color='green'><b>TIM03 : 기업카드 계정잔액_M-0</b></font>
* <font color='green'><b>TIM04 : 기업카드 총이용금액_M-2</b></font>
* <font color='green'><b>TIM05 : 기업카드 총이용금액_M-1</b></font>
* <font color='green'><b>TIM06 : 기업카드 총이용금액_M-0</b></font>
* <font color='purple'><b>CAT01 : 전월말 조기경보 등급</b></font>
* <font color='purple'><b>CAT02 : 기업결합 조기경보등급_모니터링용</b></font>
* <font color='purple'><b>CAT03 : 전월 신용등급</b></font>
* <font color='purple'><b>CAT04 : 리스크모니터링 등급 </b></font>

#### 
-----------------------------------------------------------------------------------------------------------------------------------------
