# Visual Studio Code 설치

[README로 돌아가기](../../README.md)

이 문서는 Windows 환경에서 **powershell 터미널을 사용해** `winget`으로 Visual Studio Code를 설치하는 방법을 간단히 안내합니다.

## 1. Visual Studio Code 버전 확인 후 설치 (터미널)

```powershell
winget list --id Microsoft.VisualStudioCode
```

목록에 Visual Studio Code와 버전이 보이면 설치를 건너뜁니다.  
표시되지 않으면 아래 명령으로 설치합니다.

```powershell
winget install --id Microsoft.VisualStudioCode -e --source winget
```

설치 후 다시 확인:

```powershell
code --version
```

`code` 명령이 동작하지 않으면 VS Code를 한 번 실행한 뒤 PowerShell을 다시 열어 확인합니다.

## 2. Java 관련 확장팩 설치 (VS Code)

1. VS Code를 실행합니다.
2. 좌측 메뉴에서 `확장(Extensions)` 탭을 엽니다. (단축키: `Ctrl + Shift + X`)
3. 검색창에 `Extension Pack for Java`를 입력하고 설치합니다.
   - 이 확장팩에는 Java 개발에 필요한 핵심 기능(언어 지원, 디버깅, 테스트, Maven/Gradle 등)이 묶여 있습니다.

## 3. 추가로 권장하는 확장팩 설치 (VS Code)

1. VS Code 좌측 메뉴에서 `확장(Extensions)` 탭을 엽니다. (단축키: `Ctrl + Shift + X`)
2. 검색창에 밑의 항목을 입력하고 설치합니다.
   - `Indent Rainbow`
   - `Material Icon Theme`
   - `WSL`
