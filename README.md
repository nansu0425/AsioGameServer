# Byteborne World

C++ 2D MMORPG 프로그래밍 포트폴리오 프로젝트입니다.

## 프로젝트 개요

Byteborne World는 2025년 7월에 시작된 C++ 기반 2D MMORPG 프로젝트입니다. 특정 클라이언트/서버 기술보다는 **핵심 게임 로직과 시스템 구현**에 중점을 두고 개발하고 있습니다.

### 현재 상태
- ✅ 더미 클라이언트 - 월드 서버 간 메시지 통신 구현 완료
- 🚧 게임 클라이언트 개발 예정 (SFML + ImGui 기반)
- 🚧 게임 로직 및 시스템 확장 예정

## 개발 환경

- **IDE**: Visual Studio 2022
- **플랫폼**: Windows (추후 Linux 지원 예정)
- **버전 관리**: Git

## 기술 스택

### 핵심 기술
- **언어**: C++17
- **빌드 시스템**: CMake
- **패키지 관리**: vcpkg

### 사용 라이브러리
- **네트워킹**: [ASIO](https://think-async.com/Asio/) (Standalone)
- **프로토콜**: [Protocol Buffers](https://protobuf.dev/)
- **로깅**: [spdlog](https://github.com/gabime/spdlog)
- **게임 클라이언트 (예정)**: [SFML](https://www.sfml-dev.org/) + [ImGui](https://github.com/ocornut/imgui)

## 프로젝트 구조

```
src/
├── Core/           # 핵심 유틸리티 및 기반 시스템
├── Network/        # 네트워크 통신 모듈
├── Protocol/       # 메시지 프로토콜 처리
├── WorldServer/    # 게임 월드 서버
└── DummyClient/    # 테스트용 더미 클라이언트
```

## 빌드 방법 (윈도우 기준)

### 전제 조건
- Visual Studio 2022
- Visual Studio Installer에서 **C++를 사용한 데스크톱 개발** 설치

### 빌드 단계

1. **의존성 설치**
    - 프로젝트를 키면 보통 자동으로 vcpkg 의존성 설치가 진행된다. 
    - 자동으로 진행되지 않는 경우 `vcpkg install` 커맨드를 실행한다.

2. **프로젝트 빌드**
    - 디버그 빌드는 x64 Debug, 릴리즈 빌드는 x64 Release로 **configuration** 설정
    - DummyClient.exe, WorldServer.exe 중 빌드 **target** 설정
    - Ctrl + B 누르면 빌드 시작
    - `out/build`에서 특정 빌드의 결과물(.exe, .lib, .obj, .log 등)을 찾을 수 있다

3. **실행**
    - **configuration**과 **target** 설정
    - 디버깅을 원하면 Ctrl + F5, 프로그램 실행만 원하면 F5를 누른다.

---

*이 프로젝트는 C++ 게임 프로그래밍 기술 습득 및 포트폴리오 구축을 목적으로 개발되고 있습니다.*