개인적으로 공부하며 느낀 자주 사용되는 명령어 정리

# 01_Basic_Python

1. 기본 파이썬
- Pandas 불러오기
- Numpy 불러오기
- 경고문 생략
- 문자열 변수 생성
- 문자열 슬라이싱
- 문자열 수정
- 공백 제거
- 리스트 수정, 삭제, 추가, 정렬
- 리스트 for문
- 딕셔너리
- 딕셔너리 for문

2. DataFrame
- 데이터프레임 만들기 1 - pd.DataFrame()
- 데이터프레임 만들기 2 - pd.DataFrame(np.zeros(( a , b )))
- 데이터프레임 만들기 3
- 데이터프레임 상위 5행 출력 - df.head( 숫자로 갯수 변경 가능 )
- 데이터프레임 하위 2행 출력 - df.tail( 숫자로 갯수 변경 가능 )
- 데이터프레임 랜덤 4행 출력 - df.sample( 숫자로 갯수 변경 가능 )
- 데이터프레임 특정값 불러오기 - df.loc [ 행index , "column명" ] / df.iloc [ 행index , column_index ]
- 데이터프레임 행 값 불러오기 - df[ index넘버 : index넘버 ] / df.loc [  ] / df.iloc [  ]
- 데이터프레임 열 값 불러오기 - df[ "column명" ] / df.loc[ : , "column명" ] / df.iloc[ : , index넘버 ] / df[ "column명" ] [ index ]
- 데이터프레임 값 변경 - df.replace
- 데이터프레임 조건에 따라 불러오기 - df[ ( 조건식 ) ]
- column명 바꾸기 - df.rename ( columns = { "before1" : "after1", ... } )
- column명 한번에 모두 바꾸기 - df.columns = [ "name1" , "name2",  ... ]
- 행 개수 출력 - len ( df ) / df.shape[0] / len(df.index)
- 열 개수 출력 - df.shape[1] / len(df.columns)
- 결측값이 아닌 행 개수 출력 - df.count ( )
- 결측값 확인 - df.isnull
- 결측값이 있는 행 제거 - df.dropna( axis = 0 )
- 결측값이 있는 행 제거 - df.dropna( axis = 1 )
- 결측값을 특정값으로 대치 - df.fillna( 특정값 )
- 결측값을 앞 방향으로 채우기 - df.fillna(method = "ffill" or "pad")
- 결측값을 뒷 방향으로 채우기 - df.fillna(method = "bfill" or "backfill")
- 특정 column의 결측치 치환 - np.where() & pd.notnull()
- 특정 column에서 고유값 확인(중복값 카운트) - df[ " column명 " ].value_counts()
- 특정 column에서 고유값 확인(중복 제거) - df[ " column명 " ].unique()
- 특정 column에서 고유값 수 확인 - df[ " column명 " ].nunique()
- for문 활용

3. Series
- 시리즈 만들기 - pd.Series()
- 시리즈 값 변경 - s [ ] / s.replace( 위치, 변경값, inplace=True )
- 시리즈 여러값을 한번에 변경 - s.replace([변경 전 값], [변경 후 값]
- 시리즈 행 개수 출력 - len ( s ) / s.size / len(s.index)
- 결측값이 아닌 행 개수 출력 - s.count ( )


# 02_Basic_Python

1. 기본 파이썬
- 숫자 변수 생성
- 문자열 변수 생성
- print 기본 옵션
- 문자열 속 변수 설정
- f-string
- 문자열 띄어쓰기
- 문자열 찾기 - a.count( "  " ) / a.index( "  " )
- 문자열 분리 - a.split( " " )
- 리스트 내용 삽입 - " ".join ( a )
- 리스트 특정 문자 제거 - a.remove ( )
- 리스트 특정 문자 추출 - a.pop ( )
- 튜플
- 딕셔너리
- 집합
- 집합 연산
- id값 출력

2. 라이브러리 Numpy
- numpy 라이브러리 선언

3. 라이브러리 Pandas
- "0"값을 가지는 데이터프레임 만들기 - pd.DataFrame()
- numpy 라이브러리를 사용하여 위와 같은 형태의 데이터프레임 만들기
- 결측값 채우기 회수 제한 (fillna(method="ffill", limit=number)


# 사용환경
Google Colab
