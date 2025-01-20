## 소프트웨어 자동화 테스트 도구

### 1. 프로젝트 소개

**프로젝트 이름**: 소프트웨어 자동화 테스트 도구

**목적**: 소프트웨어의 기능을 자동으로 테스트하고, 코드 커버리지를 측정하여 소프트웨어의 품질을 향상시키기 위한 도구입니다.

**주요 기능**:

- 테스트 케이스 작성 및 관리
- 자동화된 테스트 실행
- 테스트 결과 리포트 생성
- 코드 커버리지 측정 및 리포트 생성

---

### 2. 환경 설정

**프로젝트 구조**:

```css
automation_test_project/
│
├── src/
│   └── math_functions.py
│
└── tests/
    └── test_math_functions.py

```

---

### 3. 주요 코드 설명

**src/math_functions.py**:

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

```

**tests/test_math_functions.py**:

```python
import sys
import os
sys.path.insert(0, os.path.abspath(os.path.join(os.path.dirname(__file__), '../src')))

from math_functions import add, subtract

def test_add():
    assert add(1, 2) == 3
    assert add(-1, 1) == 0

def test_subtract():
    assert subtract(2, 1) == 1
    assert subtract(2, 2) == 0

```

---

### 4. 테스트 실행 및 결과

**테스트 실행**:

```bash
pytest --junitxml=report.xml
```

**코드 커버리지 측정**:

```bash
coverage run -m pytest tests/
coverage report -m
coverage html
```

**테스트 결과 및 커버리지 리포트**:

![스크린샷 2024-08-07 오후 4.45.11.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f9f35de7-0091-4a79-819a-501ef9435828/c21f07c7-eaa1-49f3-a528-2e3bf2d08866/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-08-07_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.45.11.png)

![스크린샷 2024-08-07 오후 4.46.11.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f9f35de7-0091-4a79-819a-501ef9435828/cf3c7196-83d5-4659-9c36-b32fb5cb17a3/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2024-08-07_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.46.11.png)

---

### 5. 추가 기능 구현 및 개선 사항

**추가 기능**:

- 더 복잡한 수학 함수 테스트 추가
- 다른 유형의 테스트 케이스 작성 (예: 예외 처리 테스트)
- 코드 커버리지 100% 달성

**개선 사항**:

- 테스트 케이스 추가로 더 많은 함수 테스트
- pytest 플러그인을 사용하여 테스트 효율성 향상

---

### 6. 프로젝트 요약 및 결론

이 프로젝트는 소프트웨어 자동화 테스트와 코드 커버리지 측정 도구를 개발하는 과정을 통해 Python 프로그래밍과 테스트 자동화에 대한 기본기를 쌓았습니다.

---
