# 외부 자원 · 라이선스 목록

이 ERP의 HTML·CSS·JavaScript는 직접 작성했고, 외부 라이브러리는 아래 1개만 **저장소에 파일로 포함**해 씁니다(CDN에서 불러오지 않음).

| 이름 | 버전 | 라이선스 | 위치 | 출처 |
|---|---|---|---|---|
| supabase-js (`@supabase/supabase-js`, UMD 빌드) | 2.117.2 | MIT | `vendor/supabase.js` (라이선스 전문: `vendor/supabase-js.LICENSE.txt`) | https://github.com/supabase/supabase-js · https://www.npmjs.com/package/@supabase/supabase-js |

| 구분 | 사용 여부 | 비고 |
|---|---|---|
| 서버 · 데이터 | Supabase(Auth · Postgres · Storage · Edge Functions) | 외부 서비스. 무료 요금제 한도(DB·Storage 1GB 등) 안에서 사용 |
| Edge Function 의존성 | `jsr:@supabase/supabase-js@2` | Supabase 함수 실행 환경에서만 불러옴(MIT, 사이트에는 포함되지 않음) |
| 공공데이터 | 기상청 낙뢰관측자료 조회서비스(data.go.kr 15058079) | 공공누리 제1유형(출처표시) — 화면에 "기상청 낙뢰관측" 표기. Edge Function `lightning` 에서만 호출 |
| 행정구역 경계 | 강원도 경계 폴리곤(258개 정점) — `supabase/functions/lightning/index.ts` 상수 | southkorea/southkorea-maps `kostat/2013/json/skorea_provinces_geo_simple.json`(통계청 2013 경계 기반, KOSTAT: "Free to share or remix") · https://github.com/southkorea/southkorea-maps |
| 웹폰트 | 없음(다운로드 안 함) | CSS 글꼴 목록은 **사용자 PC에 이미 설치된 글꼴**만 이름으로 지정합니다. |
| 이미지 · 아이콘 | 없음 | 로고 자리는 글자로 표시. 직접 로고를 넣을 때는 사용권이 있는 이미지만 쓰세요. |

## 나중에 외부 자원을 추가할 때

상업적 사용이 허용되는 라이선스(MIT · Apache-2.0 · BSD · SIL OFL-1.1 등)만 쓰고, 이 표에 **이름 · 버전 · 라이선스 · 출처 주소**를 추가하세요.
