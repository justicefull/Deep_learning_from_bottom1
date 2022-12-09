# Deep_learning_from_bottom1
밑바닥부터 시작하는 딥러닝1  

**22-12-06**  
유튜브 - 나도코딩의 1분 파이썬으로 파이썬의 기본적인 내용을 복습함  
책 25p - 41p  

Numpy 기초 내용 학습  

브로드캐스트  
-형상이 다른 배열의 연산을 가능케 해주는 기능  
-넘파이 배열과 스칼라값의 연산을 넘파이 배열의 원소 각각과 스칼라값의 연산으로 바꿔 수행하는 것

**22-12-07**  
책 41p - 62p  

matplotlib 라이브러리 기초 내용 학습  

퍼셉트론  
-신경망(딥러닝)의 기원이 되는 알고리즘  
-다수의 신호를 입력받아 하나의 신호를 출력  
-신호는 '흐른다/안흐른다'(1또는0) 두가지 값을 가짐  
-퍼셉트론은 정해진 한계(임계값)이 존재함 (기호로는 세타로 표시(번데기모양))  
-보내진 신호의 총합이 임계값을 넘어서면 1, 넘어서지 않으면 0을 출력  
-입력 신호에는 각각 고유한 가중치가 곱해짐  
-가중치가 클수록 중요한 신호 (전류에서의 저항과 비슷한 역할)  

편향: 뉴런이 얼마나 쉽게 활성화되는냐를 제어  
가중치: 각 신호의 영향력을 제어  

AND게이트  
-입력이 둘이고 출력은 하나  
-두 입력이 모두 1일 때만 1을 출력, 그 외에는 0을 출력  

NAND게이트  
-AND게이트의 출력을 뒤집은 것  
-AND게이트의 매개변수의 부호를 모두 반전하면 NAND게이트가 됨  

OR게이트  
-입력 신호 중 하나 이상이 1이면 1을 출력함  

XOR게이트  
-배타적 논리합이라는 논리 회로('배타적'이란 자기 외에는 거부)  
-비선형의 영역  
-다층 네트워크 구조  

퍼셉트론의 한계(단층 퍼셉트론의 경우)  
-선형의 영역만 표시할 수 있다는 한계가 있음  
-따라서 XOR게이트를 표현할 수 없음  
-하지만 다층 퍼셉트론으로는 비선형의 영역도 표시할 수 있음  

다층 퍼셉트론  
-층이 여러 개인 퍼셉트론
-단층 퍼셉트론으로는 표현하지 못한 것을 구현할 수 있음(비선형적인 표현이 가능)  

**22-12-08**  
책 63p - 90p  

신경망  
-퍼셉트론은 가중치를 사람이 수동으로 설정해줘야 함  
-신경망은 가중치 매개변수의 적절한 값을 데이터로부터 자동으로 학습하는 능력을 가짐  

활성화 함수: 입력 신호의 총합을 출력 신호로 변환하는 함수  

계단 함수  
-임계값을 경계로 출력이 바뀌는 함수  
-0을 경계로 갑자기 변화  
-0과 1 중 하나의 값만 돌려줌  
-비선형 함수  

시그모이드 함수  
-신경망에서 자주 이용하는 활성화 함수  
-h(x) = 1/1+exp(-x) (e는 자연상수=2.7182...)  
-시그모이드란 S자 모양이란 뜻  
-입력에 따라 출력이 연속적으로 변화  
-값을 실수로 돌려줌  
-비선형 함수  

ReLU 함수  
-입력이 0을 넘으면 그대로 출력, 0이하이면 0으로 출력하는 함수  

다차원 배열  
-기본적으로 '숫자의 집합'임  
-1차원 배열은 벡터  
-2차원 배열은 행렬  
-3차원 배열은 텐서라고함  
-가로는 행(row), 세로는 열(column)  

**22-12-09**  
책 91p - 106p  

소프트맥스 함수  
-소프트맥스 함수의 분자는 입력신호의 지수 함수, 분모는 모든 입력 신호의 지수 함수의 합으로 구성  
-소프트맥스의 출력은 모든 입력 신호로부터 영향을 받음  
-함수의 출력은 0에서 1.0 사이의 실수  
-출력 총합이 1 (중요한 성질)  
-위의 성질로 함수의 출력을 '확률'로 해석 가능  

MNIST dataset  
-0~9까지의 숫자로 이루어진 이미지 데이터 베이스  
-이 데이터를 통해 신경망 실습함  
-데이터는 책에서 제공하는 파일로 다운로드함  

정규화: 데이터를 특정 범위로 변화하는 처리  

전처리: 신경망의 입력 데이터에 특정 변환을 가하는 것  

배치
-하나로 묶은 입력 데이터  
-컴퓨터로 계산할 때 큰 이점을 줌  
-배치 처리를 함으로써 부하를 줄여줌  