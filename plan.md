# Project Documentation Plan
> 업데이트: 2026-03-13 | 상태: GitHub Pages 재설계 중

---

## 레퍼런스 분석: AURORA

- 사이트: https://auroraattack.github.io/
- 저장소: https://github.com/LexusWang/Aurora-demos

**Aurora Pages 특징:**
- 단일 스크롤 페이지 (multi-page X)
- 순서: 제목 → Abstract → 시스템 구조도 → Getting Started → 데모 GIF → Citation
- 최소한의 스타일, 타이포그래피 중심
- 논문 링크 썸네일 포함
- 코드 블록 + 네트워크 토폴로지 다이어그램

---

## 전략 (확정)

| 항목 | 결정 |
|------|------|
| Pages 스타일 | **단일 스크롤 학술 랜딩 페이지** (Aurora 스타일) |
| 테마 | Jekyll Minima (기본, 심플) — Just the Docs 제거 |
| 구성 | index.md 하나에 전체 내용 (기술 문서 서브페이지는 보조) |
| 학회/저널 표기 | **없음** |
| 저자 | 5명 플레이스홀더 |
| 실험 수치 | 실제값 모두 반영 |

---

## 새 Pages 섹션 순서 (index.md)

```
1. 제목 + 저자 5명 + [Paper] [GitHub] [Demo] 버튼
2. Abstract  (TBD — 논문 작성 후)
3. System Overview  (구조도 이미지 자리)
4. Key Results  (실제 수치 테이블)
5. Demo  (영상/GIF 자리)
6. Getting Started  (설치 + 실행 quick start)
7. Citation  (BibTeX, 학회 미표기)
```

---

## 확보된 실험 수치 (results.md / README TBD 교체용)

| 지표 | 값 |
|------|-----|
| 평균 Ability 수 | 27.3개 |
| 초기 성공률 | 69.63% |
| 최종 성공률 (Self-Correcting) | 84.22% |
| 개선량 | +14.59 pp |
| 평균 생성 시간 | 2.8분 |
| 평균 API 비용 | $0.35 |
| ATT&CK Validity | 94.91% |
| CTI Precision | 73.97% |
| CTI Recall | 52.56% |
| KISA 체크리스트 평균 패스율 | 91.11% |
| 최종 공격 목표 달성 | 11/11 (100%) |

**LLM 비교:**
| 모델 | Ability | 최종 SR | 비용 |
|------|---------|--------|-----|
| Claude Sonnet 4.5 | 27.3 | 84.22% | $0.35 |
| GPT-4o | 13.5 | 73.56% | $0.13 |
| Gemini 2.5 Pro | 13.3 | 87.86% | $0.10 |
| Grok 4 Fast | 17.3 | 73.96% | $0.01 |

**AURORA 직접 비교:**
| | AURORA | 본 시스템 |
|--|--------|---------|
| 체인 길이 | 23.87 | 28.75 |
| 실행 성공률 | 59.96% | 68.86% |
| CTI Recall | 24.26% | 34.57% |

---

## 작업 목록

### 🔴 지금 바로 (재설계)
- [x] plan.md 전략 업데이트
- [ ] docs/_config.yml — Just the Docs → Minima 테마로 교체
- [ ] docs/index.md — 단일 스크롤 학술 랜딩 페이지로 전면 재작성
- [ ] README.md — 학회 표기 제거, 저자 5명 플레이스홀더, 수치 실제값 반영
- [ ] README-ko.md — 동일 업데이트

### 🟡 이미지 확보 후
- [ ] `docs/assets/images/system-overview.png` (논문 fig)
- [ ] `docs/assets/images/system-architecture.png` (논문 fig)
- [ ] 결과 그래프 이미지들 (fig3, fig4b, fig8 등)
- [ ] 데모 GIF 또는 영상 URL

### 🟢 논문 제출/공개 후
- [ ] GitHub username → `alpakalee` 일괄 교체
- [ ] repo Private → Public
- [ ] GitHub Pages 활성화 (Settings → Pages → GitHub Actions)
- [ ] Abstract 완성 후 반영
- [ ] 저자 5명 실명 입력
- [ ] BibTeX + DOI 완성

---

## 파일 구조 (재설계 후)

```
docs/
├── _config.yml          # Jekyll Minima 설정 (Just the Docs 제거)
├── index.md             # 메인 단일 스크롤 페이지 (전체 내용)
├── pages/               # 기술 문서 보조 페이지 (유지)
│   ├── installation.md
│   ├── configuration.md
│   ├── usage.md
│   └── ...
└── assets/
    └── images/          # 논문 figure 이미지 저장
```
