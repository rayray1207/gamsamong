# 감사몽 PWA/TWA 준비 패키지

포함 파일
- index.html: 최종 HTML 파일
- manifest.webmanifest: PWA 매니페스트
- service-worker.js: 오프라인 캐시용 서비스워커
- icons/: PWA/Play Store용 기본 아이콘 초안
- .well-known/assetlinks.json: TWA 연결용 템플릿

다음 작업
1. 이 폴더를 HTTPS 호스팅에 배포하세요. 예: Netlify, Vercel, GitHub Pages.
2. 배포 URL에서 /manifest.webmanifest, /service-worker.js, /.well-known/assetlinks.json 이 열리는지 확인하세요.
3. Bubblewrap으로 TWA 프로젝트를 생성하세요.
4. Android App Bundle(.aab)을 빌드하세요.
5. Google Play Console에 업로드하세요.

주의
- assetlinks.json의 package_name과 sha256_cert_fingerprints는 실제 TWA 패키지명/릴리즈 키 지문으로 교체해야 합니다.
- 현재 앱 데이터는 localStorage에 저장됩니다. 앱 삭제/데이터 삭제 시 초기화됩니다.

## 2026-06 update
- Calendar now aggregates real saved daily counts from localStorage.
- Recent 7-day chart, monthly sum, active-day average, best day, and current streak now update from saved daily data.
