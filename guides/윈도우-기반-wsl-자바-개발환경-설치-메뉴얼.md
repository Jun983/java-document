# Windows에서 WSL 자바 개발환경 설치

이 문서는 Windows 환경에서 WSL(Windows Subsystem for Linux)과 리눅스 배포판을 설치(다운로드)하는 방법을 간단히 안내합니다.

## 1. WSL 설치 여부 확인 후 설치 (터미널)

아래 명령으로 WSL이 이미 설치되어 있는지 먼저 확인합니다.

```powershell
wsl --status
```

- 정상적으로 상태/버전 정보가 표시되면 WSL이 이미 설치된 상태입니다.
- 오류가 나거나 WSL이 설치되지 않았다는 안내가 표시되면 WSL을 설치하고 **Ubuntu**까지 함께 설치합니다.

WSL이 설치되어 있지 않다면 아래 명령으로 Ubuntu를 함께 설치합니다.

```powershell
wsl --install -d Ubuntu
```

명령 실행 후 필요한 구성요소를 자동으로 추가하고, 리눅스 배포판을 설치한 뒤 재부팅을 요구할 수 있습니다.

설치가 끝난 뒤, 아래 명령으로 설치된 배포판 목록과 버전을 확인합니다.

```powershell
wsl -l -v
```

Ubuntu가 설치되어 있으면 아래 명령으로 Ubuntu를 처음 실행해 리눅스 사용자/비밀번호를 설정합니다.

```powershell
wsl -d Ubuntu
```

## 2. WSL에서 VS Code 실행 (터미널)

Windows PowerShell(또는 Windows 터미널)에서 아래 명령으로 WSL(ubuntu) 프롬프트로 진입한 뒤, 아래 순서로 `java-workspace` 폴더를 만들고 VS Code를 WSL 연동 상태로 실행합니다.

```powershell
wsl -d Ubuntu
```

WSL 프롬프트에서 아래를 실행합니다.

```powershell
mkdir -p ~/java-workspace
cd ~/java-workspace
code .
```

`code .`를 처음 실행하면 WSL 내부에 VS Code Server 설치가 진행될 수 있으며, 이후에는 항상 WSL(원격) 쪽으로 VS Code가 열립니다.

## 3. SDKMAN 이용해서 jdk 17 (openjdk) 설치 (터미널)

이 단계는 WSL(ubuntu) 터미널에서 진행합니다. (WSL 확장팩 설치는 이미 완료되어 있다고 가정합니다.)

먼저 SDKMAN 설치 여부를 확인합니다.

```powershell
test -f "$HOME/.sdkman/bin/sdkman-init.sh" && echo "SDKMAN 설치됨" || echo "SDKMAN 미설치"
```

SDKMAN이 미설치라면 아래를 진행합니다.

필수 패키지 설치(필요한 경우):

```powershell
sudo apt-get update
sudo apt-get install -y curl zip unzip ca-certificates
```

SDKMAN 설치:

```powershell
curl -s "https://get.sdkman.io" | bash
```

SDKMAN 설치가 끝났거나 이미 설치되어 있으면, 현재 터미널에서 바로 사용하려면 아래를 실행합니다.

```powershell
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

SDKMAN 버전 확인:

```powershell
sdk version
```

현재 `java -version` 결과가 이미 `17`로 되어 있다면 `sdk install`/`sdk use` 단계는 생략하고 종료합니다.

OpenJDK 17 설치(필요한 경우):

```powershell
sdk install java 17.0.18-tem
```

설치가 끝난 뒤 기본으로 사용(또는 prompt에서 기본으로 설정)합니다.

```powershell
sdk use java 17.0.18-tem
```

설치 확인:

```powershell
java -version
```
