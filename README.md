# 국화 품종 QR 안내 사이트

PDF 7개를 모바일 웹에서 크게 볼 수 있도록 만든 GitHub Pages용 정적 사이트입니다. 별도 서버나 유료 서비스가 필요 없습니다.

## 페이지 구성

- `/` : 전체 품종 목록
- `/1/` : 마이윙 (My Wing)
- `/2/` : 마이시티 (My City)
- `/3/` : 마이엘프 (My Elf)
- `/4/` : 마이허밍 (My Humming)
- `/5/` : 마이티니 (My Teeny)
- `/6/` : 마이허니 (My Honey)
- `/7/` : 마이써니 (My Sunny)
- `/qr-maker.html` : 배포 주소로 QR 코드 7개 생성

## GitHub Pages에 무료로 올리는 방법

### 1. GitHub 저장소 만들기

1. [GitHub](https://github.com/)에 로그인합니다.
2. 오른쪽 위 `+` → `New repository`를 누릅니다.
3. Repository name에 `gukhwa-qr`을 입력합니다.
4. 공개 QR에서 접속할 수 있도록 `Public`을 선택합니다.
5. `Create repository`를 누릅니다.

### 2. 이 사이트 파일 업로드하기

1. 이 압축파일을 풉니다.
2. 새 저장소 화면에서 `uploading an existing file`을 누릅니다.
3. 압축을 푼 폴더 자체가 아니라, 폴더 **안의 파일과 폴더 전부**를 업로드합니다.
4. 아래쪽 `Commit changes`를 누릅니다.

업로드 후 저장소 첫 화면에 `index.html`, `style.css`, `assets`, `1`부터 `7` 폴더가 바로 보여야 합니다.

### 3. GitHub Pages 켜기

1. 저장소의 `Settings` → 왼쪽 `Pages`로 이동합니다.
2. `Build and deployment`의 Source에서 `Deploy from a branch`를 선택합니다.
3. Branch를 `main`, 폴더를 `/(root)`로 선택하고 `Save`를 누릅니다.
4. 잠시 뒤 같은 화면 위쪽에 공개 주소가 표시됩니다.

화면 구성이 달라졌거나 배포가 되지 않으면 [GitHub 공식 Pages 배포 설정 문서](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)를 확인하세요.

저장소 이름이 `gukhwa-qr`이라면 주소는 보통 아래 형식입니다.

```text
https://내-GitHub-아이디.github.io/gukhwa-qr/
```

## QR 코드 7개 만들기

배포된 사이트에서 아래 주소를 엽니다.

```text
https://내-GitHub-아이디.github.io/gukhwa-qr/qr-maker.html
```

1. 입력란에 사이트 기본 주소가 맞는지 확인합니다.
2. `QR 7개 생성`을 누릅니다.
3. 품종별 `PNG 저장` 버튼으로 QR 이미지를 저장합니다.
4. 실제 인쇄 전에 휴대전화로 각 QR을 스캔해 `/1/`부터 `/7/`까지 올바르게 열리는지 확인합니다.

QR 생성 화면은 QR 코드 라이브러리를 불러오기 위해 인터넷 연결이 필요합니다. 품종 안내 페이지 자체는 외부 라이브러리를 사용하지 않습니다.

## 로컬에서 미리 보기

터미널에서 이 폴더로 이동한 뒤 다음 명령을 실행합니다.

```bash
python3 -m http.server 8000
```

웹 브라우저에서 `http://localhost:8000`을 엽니다.

