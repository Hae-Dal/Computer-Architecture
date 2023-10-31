# 컴퓨터 구조  
  
## 3장 컴퓨터 산술과 논리 연산
  
### ALU의 구성 요소
>#### 산술 연산장치  
>   : 산술 연산들을 수행  
>#### 논리 연산장치  
>   : 논리 연산들을 수행  
>#### 시프트 레지스터  
>   : 비트들을 좌측, 우측으로 이동시키는 기능의 레지스터  
>#### 보수기
>   : 2진 데이터를 2의 보수로 변환(음수화)  
>#### 상태 레지스터
>   : 연산 결과의 상태를 나타내는 플래그를 저장하는 레지스터  
>
>   <img src="../images/ALU Component.png"/>  
  
### 정수의 표현
>#### 정수의 표현
>   : 0, 1, 부호 및 소수점으로 수를 표현  
  
### 소수와 음수의 표현  
>#### 소수의 표현  
>   <img src="../images/minority expression.png"/>  
>
>#### 음수의 표현 방법  
>   1. 부호화-크기 표현 : 제일 좌측 비트를 부호 비트, 나머지는 수를 나타내는 비트  
>   2. 1의 보수 표현 : 모든 비트를 반전  
>   3. 2의 보수 표현 &larr; 제일 많이 씀 : 모든 비트를 반전시키고 결과에 1을 더함  
>  
>#### 2의 보수 &rarr; 10진수 변환  
>   - 2의 보수 양수 &rarr; 10진수
>       - 2<sup>n-2</sup> + 2<sup>n-3</sup> + .... + 2<sup>1</sup> + 2<sup>0</sup>  
>   - 2의 보수 음수 &rarr; 10진수
>       - -2<sup>n-1</sup> + (2<sup>n-2</sup> + 2<sup>n-3</sup> + .... + 2<sup>1</sup> + 2<sup>0</sup>)  

### 비트 확장
>#### 하드웨어의 구성
>   - 선택 신호들에 의하여 멀티플렉서의 네 입력들 중의 하나를 출력  
>   <img src="../images/Logical operation hardware.png"/>  
>
>#### N-비트 데이터들을 위한 논리 연산 장치  
>   <img src="../images/4bit logical operation.png"/>   
>   <img src="../images/4bit logical operation2.png"/>  

### 연산들  
>**AND 연산 : 둘 다 1일경우 1**  
>**OR 연산 : 둘 중 1개만 1일경우 1**  
>**XOR 연산 : 두 비트가 다를 경우 1**  
>**NOT 연산 : 모든 비트 반전**  
>**선택적-세트 연산**  
>   **예.**<img src="../images/selective-set operation.png"/>  
>**선택적-보수 연산**  
>   **예.**<img src="../images/selective-complement operation.png"/>  
>**마스크 연산**  
>   **예.**<img src="../images/mask operation.png"/>  
>**삽입 연산**  
>   1. 삽입할 비트 위치들에 대하여 <u>마스크 연산 수행</u>  
>   2. 새로이 삽입할 비트들과 <u>OR 연산을 수행</u>  
>   <img src="../images/insert operation.png"/>  
>**비교 연산**  
>   - A, B 레지스터의 내용 비교 &Rightarrow; XOR 연산  
>   - 서로 다르면 1, 같으면 0  
>   <img src="../images/compare operation.png"/>  
>**시프트 연산**  
>   - 좌측 시프트
>   - 우측 시프트
>   - 순환 시프트