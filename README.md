# 극한 주기 궤도와 갈래치기 다시 보기: 비선형 동역학 7~8장 인터랙티브 데모

스티븐 스트로가츠(Steven H. Strogatz)의 『[비선형 동역학과 카오스 2/e](https://www.acornpub.co.kr/product/%EB%B9%84%EC%84%A0%ED%98%95-%EB%8F%99%EC%97%AD%ED%95%99%EA%B3%BC-%EC%B9%B4%EC%98%A4%EC%8A%A4-2e/6061/category/25/display/1/)』(에이콘출판사, 2025) 7장 **극한 주기 궤도(limit cycles)** 와 8장 **갈래치기 다시 보기(bifurcations revisited)** 를 위상 평면(phase plane) 위에서 직접 궤적을 그려 보며 배우는 웹 데모 모음입니다.

경상국립대학교 물리학과 이상훈 교수가 [2026 복잡계 여름학교](https://www.complexity.kr/?p=1365)에서 진행한 7~8장 강의의 강의노트를 기반으로, Claude Opus 5.5(Anthropic)가 제작했습니다.

**데모 바로가기:** `https://lshlj82.github.io/nonlinear-dynamics-summer-school/`

## 데모 목록

| 번호 | 파일 | 다루는 내용 | 교재 절 |
|:---:|---|---|:---:|
| 01 | [`01-limit-cycles.html`](01-limit-cycles.html) | 극한 주기 궤도의 정의와 안정성, 선형 중심과의 비교, 극좌표계 예제, 반 데르 폴 진동자, 기울기 시스템, 에너지 함수, 리아푸노프 함수, 둘락 기준 | 7.0~7.2 |
| 02 | [`02-poincare-bendixson-relaxation.html`](02-poincare-bendixson-relaxation.html) | 푸앵카레-벤딕슨 정리와 가두는 영역, 해당과정 모형, 위상 평면에는 카오스가 없음, 리에나르의 정리, 완화 진동과 주기 추정 | 7.3~7.5 |
| 03 | [`03-weakly-nonlinear-oscillators.html`](03-weakly-nonlinear-oscillators.html) | 약한 비선형 진동자, 에너지를 이용한 추정, 정규 섭동 이론과 그것의 실패, 두 타이밍, 평균 방정식, 포락선, 더핑 진동자와 단진자 | 7.6 |
| 04 | [`04-bifurcations-hopf.html`](04-bifurcations-hopf.html) | 안장점, 초월임계, 갈퀴 갈래치기와 허깨비, 유전자 제어 시스템, 대칭성과 갈퀴 갈래치기, 초임계와 준임계 호프 갈래치기, 다른길오고감, 겹쳐진 호프 갈래치기 | 8.0~8.2 |
| 05 | [`05-chemical-global-josephson.html`](05-chemical-global-josephson.html) | 진동하는 화학반응, 순환 궤도의 전역적 갈래치기(안장점, 무한 주기, 같은 모임)와 척도 조정 법칙, 구동 진자와 조지프슨 접합, 푸앵카레 사상, 전류-전압 다른길오고감 곡선 | 8.3~8.5 |
| 06 | [`06-coupled-oscillators-poincare-maps.html`](06-coupled-oscillators-poincare-maps.html) | 결합된 진동자와 준주기성, 토러스 매듭, 위상 고정과 절충 진동수, 푸앵카레 사상과 거미줄 구성, 사인파로 구동되는 RC 회로, 플로케 승수, 결합된 조지프슨 접합 | 8.6~8.7 |

<!-- 새 데모를 추가하면 위 표에 한 줄씩 추가하세요. -->

## 주요 기능

- **클릭 한 번으로 궤적 그리기**: 위상 평면을 클릭하거나 탭하면 그 점을 초기 조건으로 하는 궤적이 실시간으로 그려집니다.
- **매개변수 조작**: 반 데르 폴 진동자의 μ, 리아푸노프 함수 V = x² + ay²의 계수 a, 둘락 기준의 가중치 함수 g, 해당과정 모형의 a와 b, 리에나르 방정식의 f와 g, 평균 방정식의 h(x, ẋ), 약한 비선형 진동자의 ε, 갈래치기 표준형과 호프 갈래치기의 μ 등을 바꾸면 벡터장과 배경 지도가 즉시 다시 계산됩니다.
- **조건 자동 점검**: 가두는 영역의 경계에서 흐름이 안쪽을 향하는지, 리에나르의 정리의 다섯 조건을 만족하는지를 화면에서 바로 판정해 보여 줍니다.
- **연결된 그래프**: 위상 평면의 궤적과 시계열 x(t), 1차원 흐름 ṙ–r, 궤적을 따라 잰 V(t)와 E(t)가 함께 움직입니다.
- **갈래치기 도표와 고윳값**: 매개변수를 움직이면 고정점과 극한 주기 궤도의 갈래치기 도표, 원점 고윳값의 복소평면 위치가 함께 바뀝니다. 준임계 호프 갈래치기에서는 μ를 천천히 오르내리며 다른길오고감을 직접 관찰할 수 있습니다.
- **근사와 수치 해의 비교**: 정규 섭동 이론, 두 타이밍, 평균 방정식으로 얻은 근사식을 같은 화면에서 수치 적분 결과와 겹쳐 보고 최대 오차를 확인할 수 있습니다.
- **한국어 본문, 영어 원어 병기**: 용어와 예제 번호는 번역서 『비선형 동역학과 카오스 2/e』를 따르고, 중요한 용어는 괄호 안에 영어 원어를 함께 적었습니다.
- **반응형, 다크 모드, 동작 줄이기 설정 지원**: 휴대폰에서도 사용할 수 있고, 운영체제의 다크 모드와 "동작 줄이기(reduced motion)" 설정을 따릅니다.

## 저장소 구조

```
.
├── index.html                                 # 전체 데모 목록(첫 화면)
├── 01-limit-cycles.html                       # 7.0~7.2절 데모
├── 02-poincare-bendixson-relaxation.html      # 7.3~7.5절 데모
├── 03-weakly-nonlinear-oscillators.html       # 7.6절 데모
├── 04-bifurcations-hopf.html                  # 8.0~8.2절 데모
├── 05-chemical-global-josephson.html          # 8.3~8.5절 데모
├── 06-coupled-oscillators-poincare-maps.html  # 8.6~8.7절 데모
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
- 기울기 시스템 예제(예제 7.2.1)에서는 y가 각도 변수이므로 위아래 경계를 이어 붙이는 주기적 경계 조건을 적용했습니다.
- 예제 7.2.4는 교재의 g = 1/(xy) 외에 g = 1로도 ∇·ẋ = −(x − 1)² − y < 0이 되어 양의 사분면에서 둘락 기준이 성립합니다. 데모에는 부호가 섞여 결론을 내리지 못하는 사례로 g = x, g = y를 함께 넣었습니다.
- 예제 8.7.1의 푸앵카레 사상은 교재 그대로이면 특성 승수가 e^(−4π) ≈ 3.5×10⁻⁶이라 거미줄이 한 번에 수렴해 보이지 않으므로, 데모에서는 ṙ = c·r(1 − r²)로 일반화해 c를 줄여 볼 수 있게 했습니다(c = 1이 교재의 경우).
- 조지프슨 접합 데모의 푸앵카레 사상 P(y)는 원통을 한 바퀴 돌 때까지 궤적을 직접 적분해 계산하고, 안정성 그림의 같은 모임 갈래치기 곡선은 각 α에서 회전하는 해가 존재하는 최소 I를 이분법으로 찾아 그립니다. 첫 화면의 나선파는 BZ 반응을 흉내 낸 Barkley 모형 시뮬레이션이며 교재의 방정식은 아닙니다.
- 유전자 제어 시스템(예제 8.1.1)의 끌림 영역은 격자의 각 점에서 궤적을 적분해 어느 안정점으로 가는지로 칠하고, 임곗값은 안장점의 안정한 고유벡터 방향에서 시간을 거꾸로 적분해 그립니다. 예제 8.2.1의 불안정한 극한 주기 궤도 크기도 x축 위의 초기 조건을 이분법으로 찾아 수치로 구합니다.
- 평균 방정식 데모의 ⟨h sin θ⟩, ⟨h cos θ⟩는 고른 h에 대해 한 주기를 256개 점으로 나눠 수치로 평균합니다. r′ = 0인 점(극한 주기 궤도의 반지름 예측)과 그 안정성도 자동으로 찾습니다.

## 참고문헌

1. 스티븐 스트로가츠, 『[비선형 동역학과 카오스 2/e](https://www.acornpub.co.kr/product/%EB%B9%84%EC%84%A0%ED%98%95-%EB%8F%99%EC%97%AD%ED%95%99%EA%B3%BC-%EC%B9%B4%EC%98%A4%EC%8A%A4-2e/6061/category/25/display/1/)』 (에이콘출판사, 2025).
   * 원서: [Steven H. Strogatz](https://scholar.google.com/citations?user=FxyRWlcAAAAJ), [Nonlinear Dynamics and Chaos: 2nd Edition](https://www.amazon.com/Nonlinear-Dynamics-Student-Solutions-Manual/dp/0813349109) (Westview Press, 2014).
2. D. W. Jordan and P. Smith, *Nonlinear Ordinary Differential Equations*, 2nd ed. (Oxford University Press, 1987).
3. Shane D. Ross, 강의 영상 [Limit Cycles, Part 5: Van der Pol Oscillator, Weakly Nonlinear Limit, Energy Method](https://youtu.be/MdJEUqUTf5w), [Averaging Theory for Weakly Nonlinear Oscillators](https://youtu.be/UzQU1nyM-No)
4. Shane D. Ross, [초임계와 준임계 호프 갈래치기 강의 영상](https://youtu.be/20O6v1X92P4)
5. Shane D. Ross, [BZ 반응과 호프 갈래치기 강의 영상](https://youtu.be/4vOC7zw2YME), [무한 주기 갈래치기 강의 영상](https://youtu.be/iphb2GlNtCk)
6. Steven H. Strogatz, 강의 영상 [Poincaré–Lindstedt method](https://youtu.be/kkN13nEn2WA)
7. Steven H. Strogatz, *Nonlinear Dynamics and Chaos*, 3rd ed. (CRC Press, 2024), 13장 Kuramoto Model.
8. Shane D. Ross, [토러스 위의 흐름과 결합된 진동자 강의 영상](https://youtu.be/nrAcgXYp1hc)
9. D. Barkley, “A model for fast computer simulation of waves in excitable media,” *Physica D* 49, 61–70 (1991).
10. Phase Plane Plotter, https://aeb019.hosted.uark.edu/pplane.html

## 제작

- **내용**: 이상훈 (경상국립대학교 물리학과), [2026 복잡계 여름학교](https://www.complexity.kr/?p=1365) 7~8장 강의노트
- **제작**: Claude Opus 5.5 (Anthropic)
