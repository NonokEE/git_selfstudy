# Calculator

## 기능 목록

- 더하기: a + b를 반환한다
- 빼기: a - b를 반환한다
- 곱하기: a * b를 반환한다
- 나누기: a / b를 반환한다 (b가 0일 때 처리 없음)

## 코드 예시

```python
def calc(a, b, op):
    if op == "add":
        return a + b
    if op == "sub":
        return a - b
    if op == "mul":
        return a * b
    if op == "div":
        return a / b
```

## 기타

- 작성자: 나
- 작성일: 오늘