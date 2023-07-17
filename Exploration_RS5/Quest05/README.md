# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 홍수정
- 리뷰어 : 최철웅


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  - 모든 인물사진과 동물사진에 블러 처리와 배경 바꾸기 모두 정상적으로 처리됨
  - 자신이 실험해본 사진에서 기존 방식에서 발생하는 문제점을 찾아냄
  - 어떻게 하면 자신이 찾은 문제점을 해결할 수 있는지 직접 실험까지 해봄
- [x] 주석을 보고 작성자의 코드가 이해되었나요?
  - 코드만 보고 이해하기 어려운 정보들을 주석을 통해 제곰함
    - 해당 클래스의 컬러값을 가져오기 위해 인덱스 값을 줄 때 해당 값이 어떤 클래스를 나타내는지 보여줌
    - cv2에서 사용하는 함수를 통해 무엇을 하고자하는지와 어떤 결과가 나오는지를 서술함
- [x] 코드가 에러를 유발할 가능성이 없나요?
  - 처리과정을 대부분 함수로 정의하여 변수 스코프 문제도 해소됨
  - cv2 함수도 사용법과 데이터의 형식을 잘 맞춰 사용함
- [x] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  - 해당 코드에서 사용한 모델이 어떻게 세그멘테이션을 진행하는지 간략하게 소개함
  - 세그멘테이션을 통한 이미지 처리를 각 과정별로 잘 나눔
  - 각 코드블럭이 무언가를 하려는지가 명확함
- [x] 코드가 간결한가요?
  - 반복적인 과정은 모두 함수로 만들었기 때문에 이미지 처리 부분이 읽기가 쉽다

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 사칙 연산 계산기
class calculator:
    # 예) init의 역할과 각 매서드의 의미를 서술
    def __init__(self, first, second):
        self.first = first
        self.second = second
    
    # 예) 덧셈과 연산 작동 방식에 대한 서술
    def add(self):
        result = self.first + self.second
        return result

a = float(input('첫번째 값을 입력하세요.')) 
b = float(input('두번째 값을 입력하세요.')) 
c = calculator(a, b)
print('덧셈', c.add()) 
```

# 참고 링크 및 코드 개선
```python
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.

# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 홍수정
- 리뷰어 : 양주영


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  > 문제를 파악하고 해결방안을 제시하였습니다. 
  ![수정님 문제 파악](https://github.com/su1oo7/aiffeltutorials/assets/134067511/afde1efd-1ea6-4cdf-b4df-c5c6706b2ca3)
- [X] 주석을 보고 작성자의 코드가 이해되었나요?
  > 주석을 코드마다 작성해주셔서 이해가 잘 됐습니다. 
  ![수정님 주석](https://github.com/su1oo7/aiffeltutorials/assets/134067511/839f9fe6-9f88-4bab-95d7-2b0521cf9011)
- [X] 코드가 에러를 유발할 가능성이 없나요?
  > 코드를 실행했을때 전반적으로 에러가 발생하지 않았습니다. 
- [X] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 코드에 대해 부가적인 설명을 붙여주신걸로 보아 이해를 제대로 하고 계신 걸로 보입니다. 
  ![수정님 코드](https://github.com/su1oo7/aiffeltutorials/assets/134067511/1495edff-4be7-4d90-8c7b-ef29327f2388)
- [X] 코드가 간결한가요?
  > 핵심적으로 코드를 작성하신걸로 보입니다. 
  ![수정님 간결](https://github.com/su1oo7/aiffeltutorials/assets/134067511/e0777fd7-aa5c-449d-a470-822115ab87c6)


# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 사칙 연산 계산기
class calculator:
    # 예) init의 역할과 각 매서드의 의미를 서술
    def __init__(self, first, second):
        self.first = first
        self.second = second
    
    # 예) 덧셈과 연산 작동 방식에 대한 서술
    def add(self):
        result = self.first + self.second
        return result

a = float(input('첫번째 값을 입력하세요.')) 
b = float(input('두번째 값을 입력하세요.')) 
c = calculator(a, b)
print('덧셈', c.add()) 
```

# 참고 링크 및 코드 개선
```python
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
