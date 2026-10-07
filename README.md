# 극한 주기 궤도와 갈래치기 다시 보기: 비선형 동역학 7~8장 인터랙티브 데모

스티븐 스트로가츠(Steven H. Strogatz)의 『[비선형 동역학과 카오스 2/e](https://www.acornpub.co.kr/product/%EB%B9%84%EC%84%A0%ED%98%95-%EB%8F%99%EC%97%AD%ED%95%99%EA%B3%BC-%EC%B9%B4%EC%98%A4%EC%8A%A4-2e/6061/category/25/display/1/)』(에이콘출판사, 2025) 7장 **극한 주기 궤도(limit cycles)** 와 8장 **갈래치기 다시 보기(bifurcations revisited)** 를 위상 평면(phase plane) 위에서 직접 궤적을 그려 보며 배우는 웹 데모 모음입니다.

경상국립대학교 물리학과 이상훈 교수가 한국복잡계학회 주최 [2026 복잡계 여름학교](https://www.complexity.kr/?p=1365)에서 진행한 7~8장 강의의 강의노트를 기반으로, Claude Opus 5.5(Anthropic)가 제작했습니다.

**데모 바로가기:** `https://lshlj82.github.io/nonlinear-dynamics-summer-school/`

## 데모 목록

| 번호 | 파일 | 다루는 내용 | 교재 절 |
|:---:|---|---|:---:|
| 01 | [`01-limit-cycles.html`](01-limit-cycles.html) | 극한 주기 궤도의 정의와 안정성, 선형 중심과의 비교, 극좌표계 예제, 반 데르 폴 진동자, 기울기 시스템, 에너지 함수, 리아푸노프 함수, 둘락 기준 | 7.0~7.2 |
| 02 | [`02-poincare-bendixson-relaxation.html`](02-poincare-bendixson-relaxation.html) | 푸앵카레-벤딕슨 정리와 가두는 영역, 해당과정 모형, 위상 평면에는 카오스가 없음, 리에나르의 정리, 완화 진동과 주기 추정 | 7.3~7.5 |

<!-- 새 데모를 추가하면 위 표에 한 줄씩 추가하세요. -->

## 주요 기능

- **클릭 한 번으로 궤적 그리기**: 위상 평면을 클릭하거나 탭하면 그 점을 초기조건으로 하는 궤적이 실시간으로 그려집니다.
- **매개변수 조작**: 반 데르 폴 진동자의 μ, 리아푸노프 함수 V = x² + ay²의 계수 a, 둘락 기준의 가중치 함수 g, 해당과정 모형의 a와 b, 리에나르 방정식의 f와 g 등을 바꾸면 벡터장과 배경 지도가 즉시 다시 계산됩니다.
- **조건 자동 점검**: 가두는 영역의 경계에서 흐름이 안쪽을 향하는지, 리에나르의 정리의 다섯 조건을 만족하는지를 화면에서 바로 판정해 보여 줍니다.
- **연결된 그래프**: 위상 평면의 궤적과 시계열 x(t), 1차원 흐름 ṙ–r, 궤적을 따라 잰 V(t)와 E(t)가 함께 움직입니다.
- **한국어 본문, 영어 원어 병기**: 용어와 예제 번호는 번역서 『비선형 동역학과 카오스 2/e』를 따르고, 중요한 용어는 괄호 안에 영어 원어를 함께 적었습니다.
- **반응형, 다크 모드, 동작 줄이기 설정 지원**: 휴대폰에서도 사용할 수 있고, 운영체제의 다크 모드와 "동작 줄이기(reduced motion)" 설정을 따릅니다.

## 저장소 구조

```
.
├── index.html                                 # 전체 데모 목록(첫 화면)
├── 01-limit-cycles.html                       # 7.0~7.2절 데모
├── 02-poincare-bendixson-relaxation.html      # 7.3~7.5절 데모
└── README.md
```

각 HTML 파일은 CSS와 JavaScript를 모두 안에 담은 독립된 단일 파일입니다. 빌드 과정이나 외부 라이브러리가 없으며, 외부에서 불러오는 것은 Google Fonts(Noto Serif KR, Noto Sans KR, STIX Two Text)뿐입니다. 글꼴을 불러오지 못해도 시스템 글꼴로 정상 동작합니다.

## 로컬에서 실행하기

HTML 파일을 브라우저로 바로 열어도 동작합니다. 로컬 서버로 확인하려면 다음과 같이 실행합니다.

```bash
git clone https://github.com/lshlj82/nonlinear-dynamics-summer-school.git
cd nonlinear-dynamics-summer-school
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000 접속
```

## 구현 메모

- 수치 적분은 4차 룽게-쿠타(Runge–Kutta, RK4) 방법을 사용합니다. 반 데르 폴 진동자처럼 μ가 커서 뻣뻣해지는(stiff) 경우에는 시간 간격을 자동으로 줄입니다.
- 완화 진동처럼 μ가 큰 경우에도 안정적으로 적분되도록 시간 간격을 μ에 맞춰 줄이고, 주기 그래프의 수치값은 페이지를 열 때 브라우저에서 직접 계산합니다.
- 위상 평면은 `<canvas>`에 그리며, 화면에 보이는 그림만 다시 그려 휴대폰에서도 가볍게 동작하도록 했습니다.
- 기울기 시스템 예제(예제 7.2.1)에서는 y가 각도 변수이므로 위아래 경계를 이어 붙이는 주기적 경계조건을 적용했습니다.
- 예제 7.2.4는 교재의 g = 1/(xy) 외에 g = 1로도 ∇·ẋ = −(x − 1)² − y < 0이 되어 양의 사분면에서 둘락 기준이 성립합니다. 데모에는 부호가 섞여 결론을 내리지 못하는 사례로 g = x, g = y를 함께 넣었습니다.

## 참고문헌

1. 스티븐 스트로가츠, 『[비선형 동역학과 카오스 2/e](https://www.acornpub.co.kr/product/%EB%B9%84%EC%84%A0%ED%98%95-%EB%8F%99%EC%97%AD%ED%95%99%EA%B3%BC-%EC%B9%B4%EC%98%A4%EC%8A%A4-2e/6061/category/25/display/1/)』 (에이콘출판사, 2025).
   * 원서: [Steven H. Strogatz](https://scholar.google.com/citations?user=FxyRWlcAAAAJ), [Nonlinear Dynamics and Chaos: 2nd Edition](https://www.amazon.com/Nonlinear-Dynamics-Student-Solutions-Manual/dp/0813349109) (Westview Press, 2014).
2. D. W. Jordan and P. Smith, *Nonlinear Ordinary Differential Equations*, 2nd ed. (Oxford University Press, 1987).
3. Phase Plane Plotter, https://aeb019.hosted.uark.edu/pplane.html

## 제작

- **내용**: 이상훈 (경상국립대학교 물리학과), [2026 복잡계 여름학교](https://www.complexity.kr/?p=1365) 7~8장 강의노트
- **제작**: Claude Opus 5.5 (Anthropic)
