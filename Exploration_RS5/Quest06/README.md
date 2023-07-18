# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 홍수정 (팀: 이태훈(코더), 최지수, 홍수정)
- 리뷰어 : 서희원


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.
- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  
- [X] 주석을 보고 작성자의 코드가 이해되었나요?
  > 네 자세하게 설명을 적어 잘 이해했습니다
  ```python
  # 샘플 길이 안넘는 애들만 살리기
  # 샘플 길이를 넘으면 사용안함
  # text_max_len = 50
  # summary_max_len = 14
  def check_length(row):
      text_len = len(row['text'].split())
      summary_len = len(row['headlines'].split())
      return text_len <= text_max_len and summary_len <= summary_max_len
  
  # apply 함수와 lambda 식을 사용하여 조건에 맞는 샘플만 남기기
  data = data[data.apply(lambda row: check_length(row), axis=1)]
  
  # 결과 출력
  print('전체 샘플수 :', (len(data)))
  ```
- [X] 코드가 에러를 유발할 가능성이 없나요?
  >네 결과가 바로바로 나와 오류없이 돌아가는 것을 확인했습니다.
- [X] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 네 Summa 의 결과가 잘 나오지 않아 새로운 방식으로 적용한 것을 보면 잘 이해하고 있다는 것을 알 수 있습니다.
- [X] 코드가 간결한가요?
  > 네 코드가 기능별로 구분되어있어서 간결하게 나와있습니다.

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.

# 참고 링크 및 코드 개선
