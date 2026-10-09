# cpp_basic

C++을 중심으로 자료구조와 알고리즘을 공부하며 작성한 코드와 학습 기록을 모은 저장소입니다. 백준(BOJ) 문제 풀이, 자료구조 구현 연습, 알고리즘 비교 노트, 알고리즘 동아리 대회 참가 기록을 함께 담고 있습니다.

문제 풀이에는 `vector`, `list`, `stack`, `queue`, `deque`, `priority_queue`, `unordered_map` 등 STL을 활용하며, 자료구조 예제에서는 연결 리스트, 힙, 트리, 트라이 등을 직접 구현합니다. 일부 기초 문제는 Java로 작성되어 있습니다.

## 저장소 구조

```text
cpp_basic/
├── README.md
├── <문제 번호>.cpp                # 백준 문제 풀이
├── 12865-2.cpp, 1260mk2.cpp 등     # 같은 문제의 다른 구현
├── 2439.java, 8958.java           # Java로 작성한 기초 문제 풀이
├── input.cpp                     # C++ 입력 처리 메모
├── inheritance.md                # 다중 상속과 생성자 관련 노트
├── *vs*.md                       # 문제별 접근법 비교 노트
├── *.jpg, *.txt                  # 풀이 보조 이미지 및 입력 자료
└── DataStrcuture/
    ├── *.cpp                     # 자료구조와 알고리즘 구현 연습
    ├── huffman_code_is_Greedy.md  # 허프만 코딩과 그리디 알고리즘 노트
    └── Aloha/
        ├── README.md
        ├── SGH2025/              # 숭고한 알고리즘 대회
        ├── MapleCup/             # 메이플컵 관련 문제 풀이와 회고
        └── HCPC/                 # HCPC 풀이 시도와 회고
```

자료구조 폴더의 실제 이름은 `DataStrcuture`입니다. 파일을 찾거나 실행할 때 이 표기를 사용합니다.

## 백준 문제 풀이

루트의 숫자 이름 파일은 주로 해당 백준 문제 번호에 대응합니다. 예를 들어 `1463.cpp`는 1463번 문제의 풀이이며, 문제 번호로 코드를 찾을 수 있습니다. 같은 문제의 구현을 비교할 수 있도록 별도 버전을 남긴 파일도 있습니다. `12865.cpp`는 2차원 DP, `12865-2.cpp`는 1차원 DP로 배낭 문제를 풉니다.

다음은 저장소에서 찾아볼 수 있는 대표 학습 주제입니다. 하나의 문제에 여러 기법이 사용될 수 있습니다.

| 주제 | 대표 파일 | 살펴볼 내용 |
| --- | --- | --- |
| 연결 리스트와 덱 | [1406.cpp](1406.cpp), [5430.cpp](5430.cpp) | 커서 이동, 삽입·삭제, 덱의 양쪽 끝 활용 |
| 스택 | [17298.cpp](17298.cpp) | 단조 스택으로 오큰수 찾기 |
| 우선순위 큐 | [1655.cpp](1655.cpp) | 최대 힙과 최소 힙을 함께 사용한 중앙값 유지 |
| 이분 탐색 | [1654.cpp](1654.cpp) | 조건을 만족하는 최대 길이 탐색 |
| 누적 합 | [11660.cpp](11660.cpp) | 2차원 구간 합 계산 |
| 투 포인터와 슬라이딩 윈도우 | [1806.cpp](1806.cpp), [12891.cpp](12891.cpp) | 연속 구간의 합과 문자 개수 관리 |
| 그리디 | [1931.cpp](1931.cpp) | 종료 시간을 기준으로 회의 선택 |
| 동적 계획법 | [1463.cpp](1463.cpp), [1106.cpp](1106.cpp), [12865-2.cpp](12865-2.cpp) | 최소 연산 횟수, 무제한 배낭, 0/1 배낭 |
| 부분 수열과 문자열 DP | [14003.cpp](14003.cpp), [9252.cpp](9252.cpp) | LIS와 LCS 계산 및 결과 복원 |
| 그래프 탐색 | [2178.cpp](2178.cpp) | BFS를 이용한 미로 탐색 |
| 최단 경로 | [1753.cpp](1753.cpp), [11657.cpp](11657.cpp), [1865.cpp](1865.cpp) | 다익스트라, 벨만–포드, 음수 사이클 판별 |
| 최소 신장 트리 | [1197.cpp](1197.cpp) | 크루스칼 알고리즘과 Union-Find |
| 위상 정렬 | [2252.cpp](2252.cpp) | 진입 차수와 큐를 이용한 순서 결정 |
| 백트래킹과 재귀 | [15649.cpp](15649.cpp), [2447.cpp](2447.cpp) | 순열 생성, 재귀적 패턴 구성 |

## 자료구조 구현 연습

[`DataStrcuture/`](DataStrcuture/)에는 자료구조의 연산과 알고리즘을 연습한 코드가 있습니다. 완전한 실행 프로그램뿐 아니라 클래스·함수 구현 조각도 포함합니다.

| 주제 | 파일 | 내용 |
| --- | --- | --- |
| 연결 리스트 | [linked_lists.cpp](DataStrcuture/linked_lists.cpp) | 학생 목록의 삽입, 삭제, 검색 |
| 스택과 큐 | [stack.cpp](DataStrcuture/stack.cpp), [queue.cpp](DataStrcuture/queue.cpp), [stack_queue.cpp](DataStrcuture/stack_queue.cpp) | 배열 기반 구현, 회문과 괄호 균형 판별 연습 |
| 힙 | [maxHeap.cpp](DataStrcuture/maxHeap.cpp) | 최대 힙의 삽입과 최댓값 조회·삭제 |
| 트리 | [bst.cpp](DataStrcuture/bst.cpp), [avl.cpp](DataStrcuture/avl.cpp) | 이진 탐색 트리, 순회, AVL 트리의 회전과 균형 유지 |
| 해시 자료구조 | [hashtable.cpp](DataStrcuture/hashtable.cpp), [hash_tables_ex1.cpp](DataStrcuture/hash_tables_ex1.cpp), [hash_tables_ex2.cpp](DataStrcuture/hash_tables_ex2.cpp) | `unordered_map`과 `unordered_set` 활용 |
| 그래프 | [graph.cpp](DataStrcuture/graph.cpp), [shortest_path_and_tropological.cpp](DataStrcuture/shortest_path_and_tropological.cpp) | 인접 리스트, 위상 정렬과 최단 경로 구현 연습 |
| 서로소 집합 | [union_find.cpp](DataStrcuture/union_find.cpp) | 경로 압축과 랭크를 이용한 집합 관리 연습 |
| 트라이 | [trie.cpp](DataStrcuture/trie.cpp) | 문자열 저장·검색과 접두사 자동 완성 |
| 탐색과 정렬 | [binary_search.cpp](DataStrcuture/binary_search.cpp), [sort.cpp](DataStrcuture/sort.cpp) | 이분 탐색, 병합 정렬, 퀵 정렬 |

## 학습 노트와 대회 기록

코드 외에도 접근법의 차이와 학습 중 궁금했던 개념을 Markdown으로 정리했습니다.

| 문서 | 내용 |
| --- | --- |
| [inheritance.md](inheritance.md) | 다중 상속 시 생성자 호출 순서와 부모 클래스의 `private` 멤버 접근 |
| [1106vs12865.md](1106vs12865.md) | 무제한 배낭과 0/1 배낭에서 DP 반복 방향이 달라지는 이유 |
| [11658vs1865.md](11658vs1865.md) | 본문에서는 11657번과 1865번의 벨만–포드 초기화 전략 비교 |
| [15989vs9095.md](15989vs9095.md) | 합을 구성할 때 순서를 고려하는 경우와 고려하지 않는 경우 비교 |
| [11066vs13975.md](11066vs13975.md) | 파일 합치기 문제 비교용 문서로, 현재 `TBD` 상태 |
| [huffman_code_is_Greedy.md](DataStrcuture/huffman_code_is_Greedy.md) | 허프만 코딩의 탐욕적 선택과 DP의 차이 |

[`DataStrcuture/Aloha/`](DataStrcuture/Aloha/)에는 알고리즘 동아리 활동과 관련된 문제 풀이 및 대회 회고가 있습니다.

- [SGH2025](DataStrcuture/Aloha/SGH2025/README.md): 숭실대·고려대·한양대 연합 숭고한 알고리즘 대회 참가 기록과 풀이 코드
- [MapleCup](DataStrcuture/Aloha/MapleCup/README.md): 메이플컵 참가 회고와 관련 문제 연습 코드
- [HCPC](DataStrcuture/Aloha/HCPC/README.md): 대회 회고, 예비소집 문제, 여러 버전의 풀이 시도

문제 번호에 대응하는 이미지에는 풀이 보조 자료가, 대회 폴더의 이미지에는 결과와 참가 기록이 담겨 있습니다.
