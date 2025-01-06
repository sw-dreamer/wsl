# Kubernetes (K8s)란?

## 1. Kubernetes란?
  **Kubernetes (K8s)** 는 **컨테이너화된 애플리케이션을 관리하는 오픈소스 플랫폼**입니다.
  
  주로 **컨테이너화된 애플리케이션**을 배포, 확장 및 운영하는 데 사용됩니다.
  
  Kubernetes는 **Google**에서 처음 개발되었고, 현재는 **Cloud Native Computing Foundation (CNCF)**의 일부로 관리되고 있습니다.

  Kubernetes는 여러 대의 서버(노드)에서 애플리케이션을 자동으로 배포하고 관리할 수 있게 해주며, 각 애플리케이션이 제대로 실행되도록 보장하는 **자기 치유(self-healing)** 기능을 제공합니다.

## 2. Kubernetes의 주요 개념

Kubernetes에서 중요한 몇 가지 개념을 소개합니다:

- **Pod**: Kubernetes에서 실행되는 애플리케이션의 기본 단위입니다. 하나 이상의 컨테이너가 포함될 수 있습니다.
- **Node**: Kubernetes 클러스터에서 애플리케이션을 실행하는 물리적 또는 가상 서버입니다.
- **Cluster**: 여러 노드로 구성되어 애플리케이션을 실행하는 환경입니다.
- **Deployment**: 애플리케이션의 배포 및 업그레이드를 관리하는 방법입니다.
- **Service**: 클러스터 내부에서 서로 통신할 수 있도록 도와주는 네트워크 서비스입니다.
- **ReplicaSet**: 애플리케이션의 여러 복제본을 관리하는 객체입니다.

## 3. Kubernetes의 장점

  Kubernetes는 다양한 기능과 장점을 제공하는 플랫폼입니다. 주요 장점은 다음과 같습니다:

### 3.1. **자동화된 배포 및 확장**
  - Kubernetes는 애플리케이션의 배포 및 확장을 자동으로 처리합니다. 새로운 컨테이너를 배포하거나 애플리케이션의 트래픽이 증가하면 Kubernetes는 자동으로 필요한 리소스를 할당하고, 애플리케이션의 수를 확장합니다.

### 3.2. **셀프 힐링(Self-healing)**
  - 장애가 발생한 컨테이너를 자동으로 재시작하거나 교체하여 애플리케이션의 가용성을 보장합니다. 예를 들어, 실패한 노드나 컨테이너가 있을 경우 이를 자동으로 감지하고 복구합니다.

### 3.3. **컨테이너 오케스트레이션**
  - 여러 개의 컨테이너를 효율적으로 관리하고 조정할 수 있습니다. Kubernetes는 분산된 환경에서 컨테이너의 배치, 스케줄링, 네트워킹, 스토리지 등을 자동으로 처리합니다.

### 3.4. **환경 일관성**
  - Kubernetes는 애플리케이션을 개발 환경, 테스트 환경, 프로덕션 환경 모두에서 일관되게 실행할 수 있도록 도와줍니다. 이는 개발과 운영 간의 **DevOps** 작업을 효율적으로 지원합니다.

### 3.5. **플랫폼 독립성**
  - Kubernetes는 다양한 클라우드 제공업체(예: AWS, GCP, Azure)와 온프레미스 환경에서 실행될 수 있습니다. 따라서 **멀티클라우드** 또는 **하이브리드 클라우드** 환경에서도 유연하게 운영 가능합니다.

## 4. Kubernetes의 단점

  Kubernetes는 매우 강력한 도구지만, 몇 가지 단점도 존재합니다:

### 4.1. **학습 곡선**
  - Kubernetes는 매우 강력하고 다양한 기능을 제공하지만, 그만큼 배우는 데 시간이 걸릴 수 있습니다. 특히 초보자에게는 설정과 관리가 복잡할 수 있습니다.

### 4.2. **자원 소비**
  - Kubernetes는 많은 리소스를 소비할 수 있습니다. 작은 규모의 애플리케이션에서는 Kubernetes가 과도한 오버헤드를 생성할 수 있어, 간단한 프로젝트에서는 오히려 부담이 될 수 있습니다.

### 4.3. **복잡성**
  - Kubernetes는 여러 컴포넌트와 기능을 제공하기 때문에, 운영하기 위해서는 각 구성 요소에 대한 깊은 이해가 필요합니다. 특히 대규모 시스템을 운영할 때는 더욱 복잡해질 수 있습니다.

## 5. Kubernetes 활용 예시

### 5.1. **마이크로서비스 아키텍처**
  - Kubernetes는 **마이크로서비스 아키텍처**를 구현하는 데 매우 유용합니다.
    
    여러 개의 마이크로서비스가 각기 다른 컨테이너에서 실행되고, Kubernetes는 이를 자동으로 관리합니다.

    예를 들어, 쇼핑몰 애플리케이션에서는 주문 관리 서비스, 결제 서비스, 사용자 관리 서비스 등을 각각 다른 컨테이너로 실행하고 Kubernetes가 이들을 조정할 수 있습니다.

### 5.2. **CI/CD 파이프라인 자동화**
  - Kubernetes는 CI/CD(지속적 통합/지속적 배포) 파이프라인을 자동화하는 데 유용합니다.
  
    Kubernetes 클러스터 내에서 테스트, 빌드, 배포 작업을 자동화하여 소프트웨어 개발 및 배포 프로세스를 더욱 효율적으로 만들 수 있습니다.

### 5.3. **클라우드 네이티브 애플리케이션**
  - Kubernetes는 클라우드 네이티브 애플리케이션을 실행하는 데 매우 적합합니다.

    여러 클라우드 제공업체에서 클러스터를 실행하고, 클러스터를 자동으로 확장하거나 축소하여 애플리케이션이 언제나 최적의 상태로 동작하게 만듭니다.

### 5.4. **대규모 웹 애플리케이션**
- Kubernetes는 대규모 웹 애플리케이션을 운영하는 데 강력한 도구입니다.

  예를 들어, 웹 사이트나 API 서버가 높은 트래픽을 처리해야 할 때, Kubernetes는 이를 자동으로 확장하고 로드 밸런싱을 통해 트래픽을 효율적으로 분배합니다.

### 5.5. **AI/ML 작업**
- Kubernetes는 AI/ML 워크로드의 관리를 돕습니다.

  여러 대의 머신에서 AI/ML 모델을 학습하고 배포하는 작업을 Kubernetes를 통해 자동화할 수 있습니다.

  특히 **GPU 지원** 및 **분산 학습**을 Kubernetes에서 손쉽게 구현할 수 있습니다.

<hr/>

## 준비 사항
- **WSL**(Windows Subsystem for Linux)
- **Ubuntu 22.04**
- **Docker**가 이미 설치된 상태

## 1. Docker 설치 확인

  Docker가 설치가 제대로 되었는지 확인합니다.

  ```bash
  docker --version
  ```

  Docker 버전 정보가 출력되면 정상적으로 설치된 것입니다. 
  
  만약 정상적으로 설치가 되어 있지 않으면 [Docker 설치](https://github.com/sw-dreamer/wsl-docker.git)를 참고하세요.

## 2. kubectl 설치 (Kubernetes 관리 도구)

  Kubernetes 클러스터를 관리하려면 kubectl이 필요합니다. kubectl을 설치하려면 아래 명령어를 실행합니다.

  ```
  # Google Kubernetes 저장소 추가
  curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
  
  # 설치
  sudo snap install kubectl --classic
  sudo apt update
  ```

## 3. kubectl 설치 확인

설치가 완료되면, kubectl 버전을 확인해 설치가 정상적으로 이루어졌는지 확인합니다

  ```bash
  kubectl version --client
  ```

## 4. kind 설치 (로컬 Kubernetes 클러스터 관리 도구)

  kind는 Kubernetes 클러스터를 로컬에서 실행할 수 있게 해주는 도구입니다. 
  
  ```
  # kind 바이너리 다운로드
  curl -Lo kind https://github.com/kubernetes-sigs/kind/releases/download/v0.18.0/kind-linux-amd64
  
  # 실행 권한 부여
  sudo chmod +x kind
  
  # /usr/local/bin 디렉토리로 이동
  sudo mv kind /usr/local/bin/
  ```

## 5. kind 설치 확인

  ```bash
  kind version
  ```
## 6. Kubernetes 클러스터 생성 및 확인

  kind를 사용하여 Kubernetes 클러스터를 생성합니다. 

  - Kubernetes 클러스터가 생성됩니다:

  ```bash
  kind create cluster
  ```

  - 클러스터가 정상적으로 생성되었는지 확인

  ```bash
  kubectl cluster-info
  ```

  정상적으로 실행되면, Kubernetes API 서버 정보가 출력됩니다.

## 7. Kubernetes 클러스터 상태 확인

  클러스터가 정상적으로 실행되고 있는지 확인하려면, kubectl 명령어를 사용해 클러스터 상태를 확인할 수 있습니다

  ```bash
  kubectl get pods
  ```
  pods는 Kubernetes에서 실행되는 컨테이너의 최소 단위입니다.

## 8. Kubernetes 클러스터 삭제
  만약 더 이상 클러스터를 사용하지 않으려면, 클러스터를 삭제할 수 있습니다
  
  ```bash
  kind delete cluster
  ```
