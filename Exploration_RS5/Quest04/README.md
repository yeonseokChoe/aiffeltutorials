# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 홍수정
- 리뷰어 : 홍서이


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [O] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  
- [O] 주석을 보고 작성자의 코드가 이해되었나요?
  > 각 주석마다 해당 코드를 넣은 이유를 넣어서 해당 코드를 작성한 이유를 알 수 있었다. 또한 마크다운을 이용해 중간중간 설명하는 글과 이미지를 넣었다.
  ```Python
  # !mkdir /content/checkpoints
  mc_path = '/content/checkpoints/'
  lstm_checkPoint_path = mc_path+"/lstm_model_{epoch}.ckpt"
  cnn_checkPoint_path = mc_path+"/cnn_model_{epoch}.ckpt"
  pool_checkPoint_path = mc_path+"/pool_model_{epoch}.ckpt"
  # 결과를 보고 best를 호출하기 위해서 checkpoint 만듬
  ```
- [O] 코드가 에러를 유발할 가능성이 없나요?
  > 파일 주소들을 상대 경로로 작성하여 에러를 방지하였다.
  
  ```python
  # 데이터를 읽어봅시다.
  # colab에서 사용하여 /content/ 가 기본 로컬 위치

  path  = '/content/'
  train_filename = 'ratings_train.txt'
  test_filename = 'ratings_test.txt'

  train_data = pd.read_table(path+train_filename)
  test_data = pd.read_table(path+test_filename)

  train_data.head()
     
  ```
- [O] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > LMS 기존 코드 뿐만이 아니라 다른 필요한 코드들을 추가하여 작성하였다. LSTM, 1-D CNN, GlobalAvergaePooling1D 등 여러개의 모델을 이용해 학습을 진행하였다.

- [O] 코드가 간결한가요?
  > 필요한 부분마다 주석을 달고 단락을 나누는 등 파이써닉하게 작성하였다.

  ```Python
  # LSTM
  lstm = keras.Sequential()
  lstm.add(keras.layers.Embedding(vocab_size, word_vector_dim, input_shape=(None,)))
  lstm.add(keras.layers.LSTM(16))
  lstm.add(keras.layers.Dense(8, activation='relu'))
  lstm.add(keras.layers.Dense(1, activation='sigmoid'))

  # 1-D CNN
  cnn = keras.Sequential()
  cnn.add(keras.layers.Embedding(vocab_size, word_vector_dim, input_shape=(None,)))
  cnn.add(keras.layers.Conv1D(16, 7, activation='relu'))
  cnn.add(keras.layers.MaxPooling1D(5))
  cnn.add(keras.layers.Conv1D(16, 7, activation='relu'))
  cnn.add(keras.layers.GlobalMaxPooling1D())
  cnn.add(keras.layers.Dense(16, activation='relu'))
  cnn.add(keras.layers.Dense(1, activation='sigmoid'))

  # GlobalAveragePooling
  pool = keras.Sequential()
  pool.add(keras.layers.Embedding(vocab_size, word_vector_dim, input_shape=(None,)))
  pool.add(keras.layers.GlobalAveragePooling1D())
  pool.add(keras.layers.Dense(8, activation='relu'))
  pool.add(keras.layers.Dense(1, activation='sigmoid'))
  ```

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

