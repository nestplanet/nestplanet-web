# nestplanet-web

네스트플래닛 회사 페이지 및 서비스 법적 고지.

## 구조

```
index.html                  회사 소개
style.css                   공통 스타일
doran/privacy.html          도란 개인정보처리방침
doran/terms.html            도란 이용약관
doran/delete-account.html   도란 계정 삭제 요청 (Play 필수)
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
- `https://nestplanet.app/doran/delete-account.html`

Play Console 앱 콘텐츠와 App Store Connect에 위 주소를 등록합니다.
앱 안의 "이용약관"·"개인정보처리방침" 행도 이 주소로 연결합니다.

계정 삭제 URL은 Play **데이터 안전** 양식이 별도로 요구하며, 앱 안에 삭제
기능이 있어도 면제되지 않습니다. Apple은 반대로 **앱 내 삭제**를 요구하므로
이 페이지만으로는 5.1.1(v)를 충족하지 못합니다.

## ⚠️ 앱 내 탈퇴가 나가면 네 곳을 함께 고친다

세 문서 모두 **앱에 탈퇴 기능이 아직 없다는 전제**로 쓰여 있습니다. 기능이
나가는 순간 아래가 전부 거짓이 되므로, 배포와 같은 날 고칩니다.

| 파일 | 고칠 곳 | 지금 문장 |
|---|---|---|
| `doran/delete-account.html` | 1. 삭제 요청 방법 | "현재는 이메일로 요청해 주시면" |
| `doran/delete-account.html` | 1번 절 아래 안내 박스 | "앱 안에서 직접 삭제하는 기능을 준비하고 있습니다" |
| `doran/privacy.html` | 7. 이용자의 권리 | "앱 안에서 직접 탈퇴하는 기능은 준비 중이며" |
| `doran/terms.html` | 제13조 (회원 탈퇴) | 〃 |

`index.html`의 링크 줄은 그대로 두면 됩니다(페이지 자체는 계속 유효합니다 —
앱을 지운 뒤에도 요청할 수 있는 웹 경로를 Play가 계속 요구합니다).

## 문서를 고칠 때

세 문서는 실제 구현과 일치해야 합니다. 아래가 바뀌면 문서도 함께 고칩니다.

- 수집하는 항목 (새 기능이 새 정보를 받을 때)
- 위탁 업체 (새 외부 서비스를 붙일 때)
- 보관 기간 (미디어 만료 정책, 유예 기간)
- 구독 혜택과 코인 정책
- 연령 하한
- **탈퇴 절차** (위 ⚠️ 표)

날짜를 바꾼 경우 세 문서를 함께 갱신합니다. 방침·약관은 "시행일",
계정 삭제 페이지는 "최종 업데이트"입니다.
