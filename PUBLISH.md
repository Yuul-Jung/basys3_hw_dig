# Basys 3 웹 매뉴얼 게시

저장소: https://github.com/Yuul-Jung/basys3_hw_dig

## 전체 파일 업로드 (Ubuntu)

ChatGPT에서 내려받은 `basys3_hw_dig.zip`이 `~/다운로드/`에 있다고 가정합니다.

```bash
# 게시 파일 압축 해제
mkdir -p ~/basys3_hw_dig_publish
unzip -o ~/다운로드/basys3_hw_dig.zip -d ~/basys3_hw_dig_publish

# 기존 GitHub 저장소를 가져옴
git clone https://github.com/Yuul-Jung/basys3_hw_dig.git ~/basys3_hw_dig_git

# 압축 파일 내 HTML과 그림들을 저장소로 복사
cp -a ~/basys3_hw_dig_publish/basys3_hw_dig/. ~/basys3_hw_dig_git/

# 전체 파일 기록 및 게시
cd ~/basys3_hw_dig_git
git add .
git commit -m "Publish Basys 3 manual and figures"
git push origin main
```

## GitHub Pages

저장소의 **Settings → Pages → Build and deployment**에서 **Deploy from a branch**, **main**, **/(root)**를 선택하고 저장합니다.

게시 주소: https://yuul-jung.github.io/basys3_hw_dig/

그림 파일을 제외하고 HTML만 올리면 본문 회로도와 사진이 표시되지 않습니다.
