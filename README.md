# java-document

자바(Java) 관련 학습 내용을 문서화하고 정리하기 위한 저장소입니다.

## 사용 목적

이 문서를 우선 열어보면 좋은 사람은 다음과 같습니다.
- **체계적인 학습자**: 자바의 핵심 개념을 노트 형식으로 차근차근 정리하며 입문/복습하고 싶은 분
- **가이드가 필요한 입문자**: Windows 환경에서 WSL + VS Code 기반의 자바 개발 환경 설정을 한 번에 끝내고 싶은 분
- **효율적인 기록가**: Obsidian을 활용한 문서 간 연결과 지식 구조화 방식을 벤치마킹하고 싶은 분
- **정주행 선호자**: 주제별로 잘 짜인 커리큘럼에 따라 순서대로 학습 내용을 파악하고 싶은 분

## 프로젝트 구조

문서 중심으로 운영되며, 저장소 루트 기준 디렉터리 구조는 아래와 같습니다.

```txt
java-document/
├── .obsidian/                    # Obsidian Vault 설정·워크스페이스
│   └── plugins/                  # 커뮤니티 플러그인 설치 위치
│       └── note-definitions/     # 노트 정의(note definitions) 플러그인
├── canvas/                       # Obsidian Canvas 로드맵
├── definitions/                  # 용어·정의 문서
├── guides/                       # 가이드·계획 문서 상위 폴더
│   ├── menual/                   # 윈도우 환경 설치·다운로드 메뉴얼
│   └── plans/                    # 챕터 구성·학습 계획
└── java/                         # 자바 학습 문서·에셋
    ├── docs/                     # 챕터별 학습 본문
    └── img/                      # 이미지 저장 위치
        └── chapter-01/           # chapter 1 문서 관련 이미지
```

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