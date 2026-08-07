# nestplanet-web

네스트플래닛 회사 페이지 및 서비스 법적 고지.

## 구조

```
index.html            회사 소개
style.css             공통 스타일
doran/privacy.html    도란 개인정보처리방침
doran/terms.html      도란 이용약관
```

정적 HTML입니다. 빌드 과정이 없습니다.

## 배포

Vercel에 리포를 연결하면 자동 배포됩니다. Framework Preset은 **Other**,
빌드 명령과 출력 디렉터리는 비워 둡니다.

도메인 `nestplanet.app`을 Vercel 프로젝트에 연결합니다.

> ⚠️ DNS를 바꿀 때 Resend 레코드를 지우지 마세요.
> `send` 서브도메인의 MX·TXT와 `resend._domainkey` TXT는 이메일 발송에
> 쓰입니다. 웹사이트는 루트의 A 레코드(또는 CNAME)를 쓰므로 서로
> 충돌하지 않습니다.

## 앱이 참조하는 URL

- `https://nestplanet.app/doran/privacy.html`
- `https://nestplanet.app/doran/terms.html`

Play Console 앱 콘텐츠와 App Store Connect에 위 주소를 등록합니다.
앱 안의 "이용약관"·"개인정보처리방침" 행도 이 주소로 연결합니다.

## 문서를 고칠 때

두 문서는 실제 구현과 일치해야 합니다. 아래가 바뀌면 문서도 함께 고칩니다.

- 수집하는 항목 (새 기능이 새 정보를 받을 때)
- 위탁 업체 (새 외부 서비스를 붙일 때)
- 보관 기간 (미디어 만료 정책, 유예 기간)
- 구독 혜택과 코인 정책
- 연령 하한

시행일을 바꾼 경우 두 문서의 날짜를 모두 갱신합니다.
