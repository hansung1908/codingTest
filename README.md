# codingTest
코딩 테스트 대비 문제 연습

### 대표적인 파이썬 내장 함수
| 함수명         | 기능 요약                       | 예시                                                     |
|:--------------|:-------------------------------|:-------------------------------------------------------|
| `len()`       | 객체의 길이(항목 개수) 반환      | `len()` → 3                                            |
| `type()`      | 객체의 타입 반환                | `type(3)` → `<class 'int'>`                            |
| `print()`     | 콘솔에 출력                     | `print("hi")` → hi                                     |
| `input()`     | 사용자 입력 받기                | `input()`                                              |
| `sum()`       | 항목들의 합 반환                | `sum()` → 6                                            |
| `max()`       | 가장 큰 값 반환                 | `max()` → 3                                            |
| `min()`       | 가장 작은 값 반환               | `min()` → 1                                            |
| `sorted()`    | 정렬된 리스트 반환              | `sorted()` → [0, 1, 2, 3, 4]                           |
| `list()`      | 리스트로 변환                   | `list("abc")` → ['a','b','c']                          |
| `tuple()`     | 튜플로 변환                     | `tuple()` → (1,2,3)                                    |
| `set()`       | 집합으로 변환                   | `set()` → {1,2,3}                                      |
| `dict()`      | 딕셔너리로 변환                 | `dict([('a',1), ('b',2)])` → {'a':1,'b':2}             |
| `range()`     | 숫자 시퀀스 생성                | `list(range(3))` →  [0, 1, 2]                          |
| `enumerate()` | 인덱스와 항목을 튜플로 반환     | `list(enumerate(['a','b']))` → [(0,'a'), (1,'b')]      |
| `zip()`       | 여러 시퀀스를 묶어서 반환        | `list(zip([1,2], [3,4]))` → [(1, 3), (2, 4)]           |
| `map()`       | 함수 적용 결과 반환             | `list(map(lambda x: x**2, [1, 2, 3]))` → [1, 4, 9]     |
| `filter()`    | 조건에 맞는 항목만 반환         | `list(filter(lambda x: x > 1, [0, 1, 2, 3]))` → [2, 3] |
| `any()`       | 하나라도 True면 True 반환       | `any([0, 0, 3, 0])` → True                                        |
| `all()`       | 모두 True여야 True 반환         | `all([1, 2, 3, 4])` → True                                         |
| `abs()`       | 절대값 반환                     | `abs(-5)` → 5                                          |
| `round()`     | 반올림                          | `round(3.14)` → 3                                      |
| `divmod()`    | (몫, 나머지) 반환               | `divmod(7,3)` → (2,1)                                  |
| `pow()`       | 거듭제곱                        | `pow(2,3)` → 8                                         |
| `id()`        | 객체의 고유 id 반환             | `id(3)` → (실행할 때마다 달라지는 정수값)                                                |
| `isinstance()`| 타입 체크                       | `isinstance(3,int)` → True                             |
| `chr()`       | 유니코드→문자 변환              | `chr(65)` → 'A'                                        |
| `ord()`       | 문자→유니코드 변환              | `ord('A')` → 65                                        |
- lambda는 익명함수 (lambda 매개변수: 반환값)
---

### 파이썬 주요 문자열(str) 메소드 정리

| 메소드                    | 설명                                  | 예시                                    |
|------------------------|-------------------------------------|-----------------------------------------|
| `capitalize()`         | 첫 글자를 대문자로 변환                       | 'hello'.capitalize() → 'Hello'          |
| `casefold()`           | 소문자로 변환(유니코드 지원)                    | 'HELLO'.casefold() → 'hello'            |
| `center(width)`        | 지정한 폭에서 문자열을 중앙 정렬                  | 'hi'.center(6) → '  hi  '               |
| `count(sub)`           | 부분 문자열의 등장 횟수 반환                    | 'banana'.count('a') → 3                 |
| `encode()`             | 인코딩된 바이트 객체 반환                      | '한글'.encode()                         |
| `endswith(suffix)`     | 해당 접미사로 끝나면 True                    | 'test.py'.endswith('.py') → True        |
| `expandtabs(tabsize)`  | 탭 문자를 지정한 크기의 공백으로 변환               | 'a\tb'.expandtabs(4) → 'a   b'          |
| `find(sub)`            | 부분 문자열의 첫 인덱스 반환(없으면 -1)            | 'hello'.find('e') → 1                   |
| `format()`             | 문자열 포매팅                             | '이름: {}'.format('홍길동') → '이름: 홍길동' |
| `format_map(dict)`     | 딕셔너리 기반 포매팅                         | '{x}, {y}'.format_map({'x':1,'y':2}) → '1, 2' |
| `index(sub)`           | 부분 문자열 첫 인덱스 반환(없으면 오류)             | 'hello'.index('e') → 1                  |
| `isalnum()`            | 영문자/숫자로만 구성됐는지 검사                   | 'abc123'.isalnum() → True               |
| `isalpha()`            | 영문자(한글 포함)로만 구성됐는지 검사               | '가나다'.isalpha() → True               |
| `isascii()`            | 모든 문자가 ASCII인지 검사                   | 'abc'.isascii() → True                  |
| `isdecimal()`          | 10진수 숫자로만 구성됐는지 검사                  | '123'.isdecimal() → True                |
| `isdigit()`            | 숫자로만 구성됐는지 검사                       | '②'.isdigit() → True                    |
| `isidentifier()`       | 파이썬 식별자로 쓸 수 있는지 검사                 | 'var_1'.isidentifier() → True           |
| `islower()`            | 모두 소문자인지 검사                         | 'abc'.islower() → True                  |
| `isnumeric()`          | 숫자로만 구성됐는지 검사                       | 'Ⅲ'.isnumeric() → True                  |
| `isprintable()`        | 모두 출력 가능한 문자면 True                  | 'abc'.isprintable() → True              |
| `isspace()`            | 모두 공백 문자면 True                      | '   '.isspace() → True                  |
| `istitle()`            | Title Case(단어 첫글자만 대문자)인지 검사        | 'Hello World'.istitle() → True          |
| `isupper()`            | 모두 대문자인지 검사                         | 'ABC'.isupper() → True                  |
| `join(iterable)`       | 반복 가능한 객체의 요소들을 문자열로 연결             | ','.join(['a','b','c']) → 'a,b,c'       |
| `ljust(width)`         | 지정한 폭에서 문자열을 왼쪽 정렬                  | 'hi'.ljust(5) → 'hi   '                 |
| `lower()`              | 모두 소문자로 변환                          | 'ABC'.lower() → 'abc'                   |
| `lstrip([chars])`      | 왼쪽(시작)에서 지정 문자 제거                   | '  hi  '.lstrip() → 'hi  '              |
| `maketrans(x, y)`      | 문자 치환용 변환 테이블 생성                    | str.maketrans('ae', '12')               |
| `partition(sep)`       | 구분자로 3분할 튜플 반환                      | 'a:b'.partition(':') → ('a', ':', 'b')  |
| `replace(old, new)`    | 부분 문자열 치환                           | 'banana'.replace('a', 'o') → 'bonono'   |
| `rfind(sub)`           | 부분 문자열의 마지막 인덱스 반환(없으면 -1)          | 'banana'.rfind('a') → 5                 |
| `rindex(sub)`          | 부분 문자열 마지막 인덱스 반환(없으면 오류)           | 'banana'.rindex('a') → 5                |
| `rjust(width)`         | 지정한 폭에서 문자열을 오른쪽 정렬                 | 'hi'.rjust(5) → '   hi'                 |
| `rpartition(sep)`      | 구분자로 3분할(오른쪽 기준) 튜플 반환              | 'a:b:c'.rpartition(':') → ('a:b', ':', 'c') |
| `rsplit([sep])`        | 오른쪽부터 분리하여 리스트 반환                   | 'a,b,c'.rsplit(',', 1) → ['a,b', 'c']   |
| `rstrip([chars])`      | 오른쪽(끝)에서 지정 문자 제거                   | '  hi  '.rstrip() → '  hi'              |
| `split([sep])`         | 구분자로 분리하여 리스트 반환                    | 'a,b,c'.split(',') → ['a','b','c']      |
| `splitlines()`         | 줄바꿈 기준으로 분리하여 리스트 반환                | 'a\nb\nc'.splitlines() → ['a','b','c']  |
| `startswith(prefix)`   | 해당 접두사로 시작하면 True                   | 'hello.py'.startswith('hello') → True   |
| `strip([chars])`       | 양쪽 끝에서 지정 문자 제거                     | '  hi  '.strip() → 'hi'                 |
| `swapcase()`           | 대소문자 반전                             | 'AbC'.swapcase() → 'aBc'                |
| `title()`              | 각 단어의 첫 글자만 대문자로 변환                 | 'hello world'.title() → 'Hello World'   |
| `translate(table)`     | 변환 테이블을 이용해 문자 치환                   | 'abc'.translate(str.maketrans('a','A')) → 'Abc' |
| `upper()`              | 모두 대문자로 변환                          | 'abc'.upper() → 'ABC'                   |
| `zfill(width)`         | 지정한 길이가 되도록 왼쪽에 0 추가                | '42'.zfill(5) → '00042'                 |
| `removeprefix(prefix)` | 접두사(prefix) 제거 (3.9+)               | 'unittest'.removeprefix('unit') → 'test'|
| `removesuffix(suffix)` | 접미사(suffix) 제거 (3.9+)               | 'misc.py'.removesuffix('.py') → 'misc'  |
- 모든 문자열 메소드는 원본을 변경하지 않고 새 문자열을 반환합니다.
- 파이썬 버전에 따라 일부 메소드(예: removeprefix, removesuffix)는 3.9 이상에서만 지원됩니다.


---

### 리스트(list) 메소드
| 메소드             | 설명                                | 예시                                       |
|:----------------|:----------------------------------|:-----------------------------------------|
| `append(x)`     | 리스트 끝에 요소 x 추가                    | a = [1,2]; a.append(3) → [1,2,3]         |
| `extend(iter)`  | iterable의 모든 요소를 리스트 끝에 추가        | a = [1,2]; a.extend([3,4]) → [1,2,3,4]   |
| `insert(i, x)`  | 인덱스 i에 요소 x 삽입                    | a = [1,3]; a.insert(1,2) → [1,2,3]       |
| `remove(x)`     | 첫 번째로 나오는 요소 x 삭제                 | a = [1,2,3]; a.remove(2) → [1,3]         |
| `pop([i])`      | 인덱스 i의 요소를 꺼내서 반환 (기본은 마지막)       | a = [1,2,3]; a.pop() → 3, a → [1,2]      |
| `clear()`       | 모든 요소 삭제                          | a = [1,2,3]; a.clear() → []              |
| `index(x)`      | 첫 번째로 나오는 요소 x의 인덱스 반환            | a = [1,2,3]; a.index(2) → 1              |
| `count(x)`      | 요소 x의 개수 반환                       | a = [1,2,2,3]; a.count(2) → 2            |
| `sort()`        | 리스트 정렬(원본 변경)                     | a = [3,1,2]; a.sort(); a → [1,2,3]       |
| `reverse()`     | 리스트 순서 뒤집기(원본 변경)                 | a = [1,2,3]; a.reverse(); a → [3,2,1]    |
| `copy()`        | 리스트 얕은 복사본 반환                     | a = [1,2]; b = a.copy(); b → [1,2]       |

---

### 튜플(Tuple) 메소드
| 메소드              | 설명                                              | 예시                        |
|:-----------------|:-------------------------------------------------|:----------------------------|
| `count(x)`       | 요소 x의 개수 반환                                | t = (1,2,2,3); t.count(2) → 2 |
| `index(x)`       | 첫 번째로 나오는 요소 x의 인덱스 반환             | t = (1,2,3); t.index(2) → 1   |

---

### 딕셔너리(Dictionary) 메소드
| 메소드        | 설명                                 | 예시                                  |
|:--------------|:-----------------------------------|:--------------------------------------|
| `get(key)`      | key에 대응되는 값 반환(없으면 None 또는 기본값)    | d = {'a':1}; d.get('a') → 1           |
| `keys()`        | 모든 키 반환                            | d = {'a':1}; list(d.keys()) → ['a']   |
| `values()`      | 모든 값 반환                            | d = {'a':1}; list(d.values()) → [1]   |
| `items()`       | (키, 값) 쌍의 튜플 리스트 반환                | d = {'a':1}; list(d.items()) → [('a',1)] |
| `update()`      | 다른 딕셔너리나 키-값 쌍으로 갱신                | d = {'a':1}; d.update({'b':2}); d → {'a':1,'b':2} |
| `pop(key)`      | key에 해당하는 값 반환 후 삭제                | d = {'a':1}; d.pop('a') → 1, d → {}   |
| `popitem()`     | 마지막 (키, 값) 쌍 반환 및 삭제               | d = {'a':1,'b':2}; d.popitem() → ('b',2) |
| `clear()`       | 모든 항목 삭제                           | d = {'a':1}; d.clear(); d → {}         |
| `copy()`        | 딕셔너리 얕은 복사본 반환                     | d = {'a':1}; e = d.copy(); e → {'a':1} |

---

### 집합(Set) 메소드
| 메소드                         | 설명                            | 예시                                  |
|:----------------------------|:------------------------------|:--------------------------------------|
| `add(x)`                    | 요소 x 추가                       | s = {1,2}; s.add(3); s → {1,2,3}      |
| `remove(x)`                 | 요소 x 삭제(없으면 에러)               | s = {1,2,3}; s.remove(2); s → {1,3}   |
| `discard(x)`                | 요소 x 삭제(없으면 무시)               | s = {1,2,3}; s.discard(4); s → {1,2,3}|
| `pop()`                     | 임의의 요소 제거 및 반환                | s = {1,2,3}; s.pop() → 1 (예시), s → {2,3} |
| `clear()`                   | 모든 요소 삭제                      | s = {1,2,3}; s.clear(); s → set()     |
| `copy()`                    | 집합 얕은 복사본 반환                  | s = {1,2}; t = s.copy(); t → {1,2}    |
| `update(iter)`              | iterable의 모든 요소 추가            | s = {1}; s.update([2,3]); s → {1,2,3} |
| `union(set)`                | 합집합 반환                        | {1,2}.union({2,3}) → {1,2,3}          |
| `intersection(set)`         | 교집합 반환                        | {1,2,3}.intersection({2,3,4}) → {2,3} |
| `difference(set)`           | 차집합 반환                        | {1,2,3}.difference({2}) → {1,3}       |
| `symmetric_difference(set)` | 대칭차집합 반환                      | {1,2,3}.symmetric_difference({2,3,4}) → {1,4} |
| `issubset(set)`             | 부분집합 여부 반환                    | {1,2}.issubset({1,2,3}) → True        |
| `issuperset(set)`           | 상위집합 여부 반환                    | {1,2,3}.issuperset({1,2}) → True      |
| `isdisjoint(set)`           | 공통 요소 없는지 여부 반환               | {1,2}.isdisjoint({3,4}) → True        |

### Python math 모듈 주요 메소드/상수 표

| 메소드/상수              | 설명                                                     | 예시 코드                          | 결과                |
|--------------------------|----------------------------------------------------------|-------------------------------------|---------------------|
| math.ceil(x)             | x보다 크거나 같은 최소 정수(올림) 반환                   | math.ceil(2.3)                      | 3                   |
| math.floor(x)            | x보다 작거나 같은 최대 정수(내림) 반환                   | math.floor(2.7)                     | 2                   |
| math.trunc(x)            | x의 소수점 이하를 버리고 정수 부분만 반환                | math.trunc(-2.7)                    | -2                  |
| math.fabs(x)             | x의 절댓값을 float로 반환                                | math.fabs(-3)                       | 3.0                 |
| math.factorial(x)        | x의 팩토리얼 반환 (x!)                                   | math.factorial(5)                   | 120                 |
| math.gcd(a, b)           | a와 b의 최대공약수(GCD) 반환                             | math.gcd(12, 18)                    | 6                   |
| math.sqrt(x)             | x의 제곱근 반환                                          | math.sqrt(9)                        | 3.0                 |
| math.pow(x, y)           | x의 y제곱 반환 (float)                                   | math.pow(2, 3)                      | 8.0                 |
| math.exp(x)              | e의 x제곱 반환                                           | math.exp(1)                         | 2.718281828...      |
| math.log(x[, base])      | x의 로그(base 지정 가능, 기본은 자연로그)                | math.log(8, 2)                      | 3.0                 |
| math.log10(x)            | x의 상용로그(밑 10) 반환                                 | math.log10(100)                     | 2.0                 |
| math.log2(x)             | x의 밑 2 로그 반환                                       | math.log2(16)                       | 4.0                 |
| math.sin(x)              | x(라디안)의 사인 반환                                    | math.sin(math.pi/2)                 | 1.0                 |
| math.cos(x)              | x(라디안)의 코사인 반환                                  | math.cos(0)                         | 1.0                 |
| math.tan(x)              | x(라디안)의 탄젠트 반환                                  | math.tan(math.pi/4)                 | 1.0                 |
| math.degrees(x)          | 라디안을 도(degree)로 변환                               | math.degrees(math.pi)               | 180.0               |
| math.radians(x)          | 도(degree)를 라디안으로 변환                             | math.radians(180)                   | 3.141592653...      |
| math.hypot(x, y)         | sqrt(x*x + y*y) 반환 (피타고라스 정리)                   | math.hypot(3, 4)                    | 5.0                 |
| math.isfinite(x)         | x가 유한수면 True 반환                                   | math.isfinite(1.0)                  | True                |
| math.isinf(x)            | x가 무한대면 True 반환                                   | math.isinf(math.inf)                | True                |
| math.isnan(x)            | x가 NaN(Not a Number)이면 True 반환                      | math.isnan(math.nan)                | True                |
| math.comb(n, k)          | n개 중 k개를 순서 없이 뽑는 조합의 수 반환               | math.comb(5, 2)                     | 10                  |
| math.perm(n, k)          | n개 중 k개를 순서 있게 뽑는 순열의 수 반환               | math.perm(5, 2)                     | 20                  |
| math.fsum(iterable)      | iterable의 모든 값을 더해 정확한 부동소수점 합 반환      | math.fsum([0.1, 0.2, 0.3])          | 0.6                 |
| math.pi                  | 원주율 π (3.141592...)                                   | math.pi                             | 3.141592653...      |
| math.e                   | 자연상수 e (2.718281...)                                 | math.e                              | 2.718281828...      |
| math.tau                 | 2π (6.283185...)                                         | math.tau                            | 6.283185307...      |
| math.inf                 | 양의 무한대                                              | math.inf                            | inf                 |
| math.nan                 | Not a Number (숫자가 아님)                               | math.nan                            | nan                 |
