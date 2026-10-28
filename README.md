# sajinpass-specs

[사진패스](https://sajinpass.com)가 쓰는 증명사진 규격 데이터입니다. 규격 하나가 JSON 파일 하나이고, 모든 파일은 [`schema.json`](schema.json)(JSON Schema draft 2020-12)을 따릅니다.

> **규정 원문이 기준이며 이 데이터는 참고용입니다.** 발급 기관의 규정이 바뀌었거나 이 데이터와 다르면 원문을 따라 주세요. 최종 판단은 발급 기관이 합니다.

## 파일

| 파일 | 규격 |
| --- | --- |
| [`kr-passport.json`](kr-passport.json) | 대한민국 여권 (성인) |
| [`kr-passport-infant.json`](kr-passport-infant.json) | 대한민국 여권 (36개월 이하 영유아: 입을 조금 벌려도 됨) |
| [`kr-id.json`](kr-id.json) | 주민등록증·운전면허증 (3.5×4.5cm. 법령에 머리 길이 기준이 없어 여권 기준으로 맞춤(`unofficial`)) |
| [`kr-driver-license.json`](kr-driver-license.json) | 운전면허증 온라인 갱신·재발급 (3.5×4.5cm, 머리 길이 3.2~3.6cm. 접수 파일은 JPG 500KB 이하, 413×531px 권장, 395~431×507~550px만 업로드) |
| [`kr-resume-3x4.json`](kr-resume-3x4.json) | 반명함판 3×4cm (이력서). 공식 규정이 없는 관습 크기(`official: false`) |
| [`kr-suneung.json`](kr-suneung.json) | 수능 응시원서 (여권용 규격 3.5×4.5cm, 머리 길이 3.2~3.6cm. 온라인 사전입력 JPG 500KB 이하·413×531px 권장) |
| [`kr-toeic.json`](kr-toeic.json) | 토익 접수 (얼굴 길이 3.2~3.6cm·흰 배경, JPG 500KB 이하. 공개 안내에 사진 크기·픽셀 기준이 없어 여권 규격 3.5×4.5cm·413×531px로 만듦(`unofficial`), 사진패스 권장) |
| [`kr-kuksiwon.json`](kr-kuksiwon.json) | 보건의료인 국가시험 응시원서 (국시원: 3.5×4.5cm, 276×354px 이상·200dpi 이상, JPG·PNG. 413×531px·500KB 이하로 만듦, 사진패스 권장) |
| [`kr-history-exam.json`](kr-history-exam.json) | 한국사능력검정시험 (GIF·JPG, 권장 크기 120×160px, 약 3×4cm. 용량 기준이 없어 200KB 이하로 만듦) |
| [`kr-korcham.json`](kr-korcham.json) | 대한상공회의소 자격시험 (컴활·워드 등: 올리면 400×500px로 바뀌어 4:5 비율로 맞춤, JPG·PNG·GIF. cm 크기 기준이 없어 35×43.75mm로 둠, 사진패스 권장) |
| [`kr-teps.json`](kr-teps.json) | TEPS (3×4cm, 126×165px, JPG 50KB 이하, 6개월 이내, 무배경) |
| [`kr-topik.json`](kr-topik.json) | TOPIK (한국어능력시험) 3.5×4.5cm, 얼굴 길이 2.5~3.5cm, 흰 배경, JPG 200KB 이내 (법무부 외국인등록용 사진 규격 준용, TOPIK 자주 묻는 질문). 공식 픽셀 기준 없음, 413×531px로 만듦 |
| [`kr-arc.json`](kr-arc.json) | 외국인등록증(ARC)·한국 비자 3.5×4.5cm, 얼굴 길이 2.5~3.5cm, 흰 배경 (출입국·외국인정책본부). 공식 픽셀 기준 없음, 413×531px로 만듦 |
| [`kr-keta.json`](kr-keta.json) | K-ETA (전자여행허가) 컬러 JPG 20MB 이하, 얼굴 전체 정면이 이미지의 75%, 모자·스카프·선글라스 없이 (K-ETA 자주 묻는 질문). 크기·픽셀·배경 기준이 없어 3.5×4.5cm 비율·머리 34mm·밝은 단색·413×531px·500KB 이하로 만듦(`unofficial`) |
| [`eu-schengen.json`](eu-schengen.json) | 유럽 쉥겐 비자 (독일·프랑스 등) 3.5×4.5cm, 얼굴 32~36mm, 밝은 단색 배경. 독일 안내의 인화 600dpi 이상에 맞춰 인화지·파일 모두 600dpi(827×1063px, `print.dpi`). 공식 픽셀·용량 기준은 없음 |
| [`vn-evisa.json`](vn-evisa.json) | 베트남 전자비자 4×6cm, JPG 2MB 미만, 흰 배경, 안경 금지. 머리 길이·픽셀 기준이 없어 머리를 사진 높이의 약 3분의 2(`unofficial`)로, 파일은 472×709px·1MB 이하로 만듦 |
| [`cn-visa.json`](cn-visa.json) | 중국 비자 종이 33×48mm, 머리 28~33mm, 흰 배경. 온라인 파일 354×472~420×560px(3:4)·40~120KB JPEG(`minKB`)라 종이 사진과 비율이 달라 `frameMm` 36×48mm로 자르고, 원문이 얼굴 배치를 픽셀로 정한 354×472px로 만듦. 얼굴 폭 191~219px(그림은 191~251px, 본문을 따름)·눈 위치·정수리 위 10~70px(`digital.layout`), 종이 얼굴 폭 15~22mm(`faceWidthMm`), 허용 각도(`poseMaxDeg`)를 따로 둠, 300dpi는 사진패스가 정한 값 (중국 외교부 영사국 규격, 주한중국대사관 게시) |
| [`in-visa.json`](in-visa.json) | 인도 비자 (e-Visa) 정사각형 JPEG(e-Visa 10KB~1MB, 일반 비자 10~300KB·350~1000px), 머리카락 끝~턱 25~35mm, 흰 배경, 안경 금지. 종이 사진은 2×2인치(주한 인도 비자센터). e-Visa에 픽셀 기준이 없어 600×600px(`digital.unofficial`)·10~300KB(`minKB`)로 만듦 |
| [`jp-visa.json`](jp-visa.json) | 일본 비자 (워킹홀리데이·유학·취업) 3.5×4.5cm, 6개월 이내, 무배경 (주한일본대사관). 머리 길이·배경색 기준이 없어 여권과 같은 32~36mm·밝은 단색(`unofficial`), 파일은 413×531px·500KB 이하(사진패스 권장) |
| [`ca-visa.json`](ca-visa.json) | 캐나다 비자·워킹홀리데이(IEC) 35×45mm 이상, 턱~정수리 31~36mm, 흰색·밝은 단색 배경, 보정 금지. IEC 디지털 사진 420×540px 이상·이상적으로 240KB·60KB 이상(`minKB`). 파일은 827×1063px(600dpi)·240KB 이하(`digital.unofficial`), 기울기 자동 보정 없음 |
| [`au-visa.json`](au-visa.json) | 호주 비자 JPEG 70KB~3.5MB(`minKB`), 1200×1600px 권장, 무채색·연한 회색 배경, 보정 금지. 종이 35~40×45~50mm·턱~정수리 32~36mm(시민권 사진 안내)라 3:4 파일과 같은 비율인 36×48mm(`unofficial`)로 자름, 기울기 자동 보정 없음 |
| [`us-visa.json`](us-visa.json) | 미국 비자 (DS-160) 2×2인치 정사각형. 머리 길이는 머리카락 끝부터 잼(`headTop: "hair"`), 안경 금지 |

## 필드

| 필드 | 뜻 |
| --- | --- |
| `schemaVersion` | 스키마 버전. 지금은 `1`. 읽는 쪽은 모르는 버전이면 무시합니다 |
| `id` | 규격 식별자. 파일 이름과 같습니다 |
| `name` | 화면에 보이는 규격 이름 |
| `official` | 선택. `false`면 발급 기관 규정이 없고 흔히 쓰는 크기를 담은 관습 규격이며 `source`를 생략할 수 있습니다. 없으면 공식 규격 |
| `unofficial` | 선택. 공식 원문에 없어 사진패스가 정한 값: `photoMm` 사진 크기, `headMm` 머리 길이, `background` 배경색. 화면에는 '사진패스 권장'으로 적습니다 |
| `audience` | `adult` 또는 `infant`. 영유아는 입 벌림 점검을 건너뜁니다 |
| `photoMm` | 사진 크기 `[가로, 세로]` mm |
| `headMm` | 턱 끝에서 머리 꼭대기까지 길이(mm). `min`·`max`는 규정 범위, `target`은 자르기 목표 |
| `headTop` | 선택. 머리 꼭대기를 어디로 보는지. `crown`(기본)은 머리카락을 뺀 정수리, `hair`는 머리카락 끝 |
| `topMarginMm` | 머리 꼭대기(`headTop`)에서 사진 위 가장자리까지(mm). 규정에 수치가 없어 예시 사진을 재서 정한 값 |
| `background` | 배경 종류와 점검 임계값(`minLuma` 밝기 평균 하한, `maxStd` 표준편차 상한, 0~255) |
| `expression` | 입 벌림·미소 허용 여부, 눈을 떠야 하는지 |
| `checks` | 켜고 끄는 자동 점검과 사용자가 직접 확인할 항목(`manual`: `crownLine` 정수리 선, `hairLine` 머리카락 끝 선, `aloneInPhoto` 보호자·사물이 안 보이는지, `glasses` 안경 반사, `noGlasses` 안경을 벗었는지, `lenses` 컬러렌즈·색안경, `takenWithin6Months` 6개월 이내) |
| `digital` | 온라인 제출 파일 규격: 크기(px)와 허용 범위, 형식, 최대 용량(KB), 해상도(dpi). `unofficial`에 든 값(`px` 만드는 크기, `range` 허용 범위, `maxKB` 용량 상한, `dpi`)은 공식 원문에 없어 사진패스가 정한 권장값이라, 파일 검사기는 허용 범위·용량 상한을 벗어나도 실패 대신 주의로 봅니다. 선택 `accept`는 제출처가 받는 형식(`jpeg`·`png`·`gif`, 없으면 `format`만). 사진패스가 만드는 파일은 늘 `format`입니다. 선택 `minKB`는 제출처가 정한 최소 용량(KB), 선택 `frameMm`은 파일 비율이 종이 사진과 다를 때 파일이 담는 범위 `[가로, 세로]` mm(높이는 `photoMm`과 같고 가로는 같거나 넓음. 인화는 가운데를 `photoMm` 비율로 잘라 씀) |
| `print` | 인화 배치: 인화지 크기(inch, px), 행·열 수, 자르는 선 여부, 선택 `dpi`(없으면 300. 원문이 더 높은 인화 해상도를 요구할 때) |
| `allowedFixes` | 자동으로 고쳐도 되는 것(선택). `rotate.maxDeg`: 눈 높이 기울기가 이 각도 이하이면 바로 세워 자릅니다. 배경·밝기·피부는 규격과 상관없이 자동으로 고치지 않습니다(배경 단색·밝기는 사용자가 켤 때만 도구가 합니다) |
| `notes` | 언어별 한 줄 요약 |
| `source`, `sourceDigital` | 규정 원문 링크. 공식 규격은 `source`가 꼭 있어야 합니다 |
| `checkedAt` | 원문을 마지막으로 확인한 날짜 |

## 라이선스

[CC BY 4.0](LICENSE). 출처를 "사진패스(sajinpass.com)"로 표시하면 자유롭게 쓸 수 있습니다.
