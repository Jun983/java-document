# java-document

자바(Java) 관련 학습 내용을 문서화하고 정리하기 위한 저장소입니다.

## 목적

- 자바 학습 문서를 열람
- 주제별로 정리된 내용을 참고
- Obsidian 기반 문서 구조 확인

## 프로젝트 구조

현재 저장소는 문서 중심으로 운영됩니다.

- `.obsidian/`: Obsidian 워크스페이스 설정 파일
- `java/`: 자바 학습 문서
- `guides/menual/`: 설치 및 사용 가이드 문서

## 사용 방법

1. 이 저장소를 클론합니다.
2. Obsidian을 사용 중이라면 폴더를 Vault로 열어 문서를 읽습니다.

## 운영 정책

- 이 저장소는 읽기 전용으로 운영됩니다.
- 로컬에서 수정하더라도 원격 브랜치로의 push는 허용하지 않습니다.

## 다운로드 / 설치 메뉴얼

위에서부터 아래로 순차적으로 진행해야 합니다.

- [윈도우 기반 저장소 다운로드 메뉴얼](guides/menual/윈도우-기반-문서-저장소-다운로드-메뉴얼.md)
- [Visual Studio Code 설치 및 확장팩 메뉴얼](guides/menual/윈도우-기반-visual-studio-code-설치-및-확장팩-메뉴얼.md)
- [윈도우 기반 WSL 자바 개발환경 설치 메뉴얼](guides/menual/윈도우-기반-wsl-자바-개발환경-설치-메뉴얼.md)

## 문서 최신화 (main 브랜치)

원격 저장소에 문서가 반영되었을 때(예: `main`에 push된 경우) 로컬에서도 같은 내용을 쓰려면 **`main` 브랜치**에서 최신 변경을 가져옵니다.

```bash
git checkout main
git pull origin main
```

이미 `main`을 체크아웃한 상태라면 아래만 실행해도 됩니다.

```bash
git pull
```

## 로드맵

아래 로드맵 파일은 반드시 Obsidian에서 열어야 정상적으로 확인할 수 있습니다.

- [Java Programming 학습 로드맵](canvas/Java-Programming-학습-로드맵.canvas)