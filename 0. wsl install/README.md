# WSL 설치 가이드

  이 가이드는 Windows Subsystem for Linux(WSL)를 설치하는 방법을 설명합니다.

## 1. PowerShell 관리자 권한 실행

  PowerShell을 관리자 권한으로 실행합니다.

## 2. 리눅스를 위한 Windows 하위 시스템 사용

  아래 명령어를 실행하여 리눅스를 위한 Windows 하위 시스템을 활성화합니다.

   ```powershell
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
   ```
## 3. Virtual Machine 사용

  WSL 2를 사용하려면 가상 머신 기능을 활성화해야 합니다. 아래 명령어를 실행합니다.

   ```powershell
   dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
   ```
## 4. WSL 설치

  WSL을 설치하려면 다음 명령어를 실행합니다.

   ```powershell
   wsl --install
   ```
  ### 문제 발생 시
  만약 문제가 발생한다면, 아래 명령어를 실행하여 웹에서 WSL을 다운로드하여 설치할 수 있습니다.

   ```powershell
   wsl --install --web-download
   ```
## 5. 재부팅

  설치 후 재부팅을 진행합니다.

## 6. WSL 2로 버전 변경

  WSL 2를 기본 버전으로 설정하려면 powershell 관리자 권한으로 실행 후 아래 명령어를 실행합니다.

   ```powershell
   wsl --set-default-version 2
   ```
## 7. 재부팅

  설정을 완료한 후 시스템을 다시 재부팅합니다.
  
## 8. WSL 상태 확인

  설치된 WSL 버전 및 상태를 확인하려면 아래 명령어를 사용합니다.
  
   ```powershell
   wsl --status
   ```
   ```powershell
   wsl -l -v
   ```
<hr/>

## 참조 링크

[Microsoft Learn Challenge] : *https://learn.microsoft.com/ko-kr/windows/wsl/install*

