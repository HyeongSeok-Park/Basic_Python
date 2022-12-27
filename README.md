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

### 데이터 출력
- 데이터프레임 상위 출력 - df.head ( 숫자로 갯수 변경 가능 )
- 데이터프레임 하위 출력 - df.tail ( 숫자로 갯수 변경 가능 )
- 데이터프레임 랜덤 출력 - df.sample ( 숫자로 갯수 변경 가능 )
- 데이터프레임 열 출력 1 (컬럼명) - df [ [ " 컬럼명 " ] ]
- 데이터프레임 열 출력 2 (선택 열 제외) - df [ df.columns.difference ( [ " 컬럼명 " ] ) ]
- 데이터프레임 열 출력 3 - df [ "column명" ] / df.loc [ : , "column명" ] / df.iloc [ : , index넘버 ] / df[ "column명" ] [ index ]
- 데이터프레임 행 출력 - df [ index넘버 : index넘버 ] / df.loc [  ] / df.iloc [  ]
- 데이터프레임 특정값 출력 - df.loc [ 행index , "column명" ] / df.iloc [ 행index , column_index ]
- 데이터프레임 조건 설정 후 출력 1 - df [ ( 조건식 ) ]
- 데이터프레임 조건 설정 후 출력 2 - df [ df [ "column명" ] == "value" ]
- 데이터프레임 정렬 - df.sort_values ( "column명" , ascending=True )
- 데이터프레임 고유값 카운트 - df [ " column명 " ].nunique()
- 데이터프레임 고유값 출력 1 (중복값 제외) - df [ " column명 " ].unique()
- 데이터프레임 고유값 출력 2 (중복값 카운트) - df [ " column명 " ].value_counts()

- 데이터 수정
- - 데이터프레임 값 변경 - df.replace
- 데이터프레임 컬럼명 수정 1 (개별 선택) - df.rename ( columns = { "before1" : "after1", ... } )
- 데이터프레임 컬럼명 수정 2 (모든 컬럼명) - df.columns = [ "name1" , "name2",  ... ]
- 데이터프레임 행값 컬럼명으로 지정 - df.rename ( columns = df.iloc [ 0 ] )
- 데이터프레임 모든 열 출력 - pd.set_option('display.max_columns', None) ; 60 =========
- 데이터프레임 모든 행 출력 - pd.set_option('display.max_rows', None) ; 10 =========
- 데이터프레임 행값 타입 변경 - df.astype ( { ' 컬럼명 ' : ' type ' } ) ======
- 데이터프레임 인덱스 초기화 - df.reset_index(drop=True) ==============

(데이터 검색)
- 행 개수 출력 - len ( df ) / df.shape [ 0 ] / len ( df.index )
- 열 개수 출력 - df.shape [ 1 ] / len ( df.columns )
- 데이터프레임 컬럼명 출력 - df.columns
- 결측값이 아닌 행 개수 출력 - df.count()
- 데이터프레임 인덱스값 출력 - df [ df [ ' 컬럼명 ' ] == a ].index ; 리스트형태로 출력 ===
- 데이터프레임 값 조회 - df [ ' 컬럼명 ' ].str.contains ( ' 검색어 ' ) ; T/F 로 출력 =====

(데이터 삭제)
- 데이터프레임 행 삭제 1 (행 이름) - df.drop ( index = "a" )
- 데이터프레임 행 삭제 2 (중복값) - df.drop_duplicates ( [ ' 컬럼명 ' ] ) ========
- 데이터프레임 행 삭제 2 (인덱스넘버) - df.drop ( [ a ] ) ==========
- 데이터프레임 행 삭제 3 (인덱스넘버) - df.drop ( df [ df [ ' 컬럼명 ' ] == a ].index ) ====
- 데이터프레임 열 삭제 (컬럼명) - df.drop( [ " column명 " ] , axis = 1 )

(결측치)
- 데이터프레임 결측치 확인 - df.isnull
- 데이터프레임 결측치 삭제 1 (행 기준) - df.dropna ( axis = 0 )
- 데이터프레임 결측치 삭제 2 (열 기준) - df.dropna ( axis = 1 )
- 데이터프레임 결측치 대치 1 (데이터 입력) - df.fillna ( '특정값' )
- 데이터프레임 결측치 대치 2 (전 데이터) - df.fillna ( method = "ffill" or "pad" )
- 데이터프레임 결측치 대치 3 (후 데이터) - df.fillna ( method = "bfill" or "backfill" )
- 데이터프레임 결측치 특정 column의 결측치 치환 - np.where() & pd.notnull()

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
- 정규표현식 - compile / match / search
- 문자열 띄어쓰기
- 문자열 찾기 - a.count( "  " ) / a.index( "  " )
- 문자열 분리 - a.split( " " )
- 리스트 내용 삽입 - " ".join ( a )
- 리스트 특정 문자 제거 - a.remove ( )
- 리스트 특정 문자 추출 - a.pop ( )
- 행 합계 추가 - df[ ' ' ] = df.sum(axis = 1)
- 열 합계 추가 - df.loc[ ' ' ] = df.sum(axis = 0)
- 튜플
- 딕셔너리
- 집합
- 집합 연산
- id값 출력

2. 라이브러리 Numpy
- numpy 라이브러리 선언
- 배열 재정렬 - np.reshape( a , ( n , m ) )
- 배열 만들기 - np.arange( l ).reshape( n , m )
- 배열 결합(세로) - np.vstack ( ( a , b ) )
- 배열 결합(가로) - np.hstack ( ( a , b ) )

3. 라이브러리 Pandas
- "0"값을 가지는 데이터프레임 만들기 - pd.DataFrame()
- numpy 라이브러리를 사용하여 위와 같은 형태의 데이터프레임 만들기
- 결측값 채우기 회수 제한 (fillna(method="ffill", limit=number)


# 사용환경
Google Colab
