# sajinpass-specs

[사진패스](https://sajinpass.com)가 쓰는 증명사진 규격 데이터입니다. 규격 하나가 JSON 파일 하나이고, 모든 파일은 [`schema.json`](schema.json)(JSON Schema draft 2020-12)을 따릅니다.

> **규정 원문이 기준이며 이 데이터는 참고용입니다.** 발급 기관의 규정이 바뀌었거나 이 데이터와 다르면 원문을 따라 주세요. 최종 판단은 발급 기관이 합니다.

## 파일

| 파일 | 규격 |
| --- | --- |
| [`kr-passport.json`](kr-passport.json) | 대한민국 여권 (성인) |

## 필드

| 필드 | 뜻 |
| --- | --- |
| `schemaVersion` | 스키마 버전. 지금은 `1`. 읽는 쪽은 모르는 버전이면 무시합니다 |
| `id` | 규격 식별자. 파일 이름과 같습니다 |
| `name` | 화면에 보이는 규격 이름 |
| `audience` | `adult` 또는 `infant`. 영유아는 입 벌림 점검을 건너뜁니다 |
| `photoMm` | 사진 크기 `[가로, 세로]` mm |
| `headMm` | 턱 끝에서 정수리까지 길이(mm). `min`·`max`는 규정 범위, `target`은 자르기 목표 |
| `topMarginMm` | 정수리에서 사진 위 가장자리까지(mm). 규정에 수치가 없어 예시 사진을 재서 정한 값 |
| `background` | 배경 종류와 점검 임계값(`minLuma` 밝기 평균 하한, `maxStd` 표준편차 상한, 0~255) |
| `expression` | 입 벌림·미소 허용 여부, 눈을 떠야 하는지 |
| `checks` | 켜고 끄는 자동 점검과 사용자가 직접 확인할 항목(`manual`) |
| `digital` | 온라인 제출 파일 규격: 크기(px)와 허용 범위, 형식, 최대 용량(KB), 해상도(dpi) |
| `print` | 인화 배치: 인화지 크기(inch, px), 행·열 수, 자르는 선 여부 |
| `notes` | 언어별 한 줄 요약 |
| `source`, `sourceDigital` | 규정 원문 링크 |
| `checkedAt` | 원문을 마지막으로 확인한 날짜 |

## 라이선스

[CC BY 4.0](LICENSE). 출처를 "사진패스(sajinpass.com)"로 표시하면 자유롭게 쓸 수 있습니다.
