## 클파쓰 (Cl-PaaS) 

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

## 🧑🏻‍💻 Organizer
| ![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/pinetree2?v=4&h=250&w=250&fit=cover&mask=circle&maxage=7d) | ![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/dayeon1201?v=4"?v=4&h=250&w=250&fit=cover&mask=circle&maxage=7d) | [![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/devyubin?v=4"?v=4&h=250&w=250&fit=cover&mask=circle&maxage=7d)](https://avatars.githubusercontent.com/u/80163835?v=4) | ![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/hnnynh?v=4"?v=4&h=250&w=250&fit=cover&mask=circle&maxage=7d) | ![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/tmddus2?v=4"?v=4&h=250&w=250&fit=cover&mask=circle&maxage=7d)
| :-------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------:
|                                                    [이해송](https://github.com/pinetree2)                                                    |                                                      [양다연](https://github.com/dayeon1201)                                                       |                                                      [김유빈](https://github.com/devyubin)                                                       |                                                      [한윤호](https://github.com/hnnynh)                                                       |   [이승연](https://github.com/tmddus2)     

---
# 프로젝트 소개
## 디지털 취약계층을 위한 피싱 문자 탐지 서비스, 누구쇼?
제 8회 개방형 클라우드 플랫폼(K-PaaS) 기반 서비스 개발 아이디어 공모전 출품작

### 💡 프로젝트 배경
최근 피싱 문자 및 스미싱 범죄로 인해 고령층이 큰 피해를 입고 있습니다. 디지털 취약 계층인 고령층은 악성 앱 설치나 가짜 웹사이트 방문을 유도하는 피싱 메시지를 식별하기 어려워, 심각한 금융적 피해를 입는 경우가 많습니다. 본 프로젝트는 노인층이 직관적이고 안전하게 사용할 수 있는 피싱 문자 탐지 앱을 개발하여 디지털 소외 계층을 보호하고자 합니다. **사용자 친화적 UI, 실시간 피싱 탐지, AI 기반 피싱 문자 분석**을 통해 안전한 디지털 환경을 제공합니다.

---

### 🌟 서비스 개요
피싱 문자 탐지 서비스는 다음과 같은 기능을 통해 사용자에게 문자 피싱을 방지하는 솔루션을 제공합니다:

- **SMS 및 URL 안전성 검사**: 메시지 내 URL과 전화번호를 분석하여 피싱 여부를 실시간으로 경고합니다.
- **피싱 문자 실시간 경고**: 의심스러운 메시지가 감지되면 즉시 사용자에게 경고 알림을 보내어 예방합니다.
- **URL 직접 확인 기능**: 사용자가 URL을 직접 입력하여 안전성을 검증할 수 있는 기능을 제공합니다.
- **스미싱 관련 교육 자료 제공**: 스미싱 예방과 피싱 인식 개선을 위한 다양한 교육 자료를 제공합니다.

---

### 📂 주요 기능 설명

#### 1. SMS/URL 안전성 검사
- 메시지 내 포함된 URL과 전화번호를 **Google Safe Browsing API**와 **PhishTank API**로 분석하여 피싱 여부를 판별합니다.
- 단축 URL의 원본 주소를 확인하고, 의심 사이트로 리디렉션되는 경우 사용자에게 경고합니다.

#### 2. 피싱 문자 실시간 경고
- AI 모델을 활용하여 메시지 내 피싱 가능성을 실시간으로 분석하며, 위험성이 있는 경우 즉시 경고 알림을 제공합니다.

#### 3. URL 직접 확인 기능 (추후 추가)
- 사용자가 URL을 앱 내에서 직접 입력하여 피싱 위험을 확인할 수 있으며, 특히 자주 사용되는 사기성 웹 주소를 방지하는 데 도움을 줍니다.

---

### 백엔드 API

---

#### 2.1 백엔드: Spring Boot

본 프로젝트의 백엔드 개발은 Spring Boot 프레임워크를 기반으로 구현되었습니다. 주요 기능으로는 사용자로부터 입력된 메시지에서 URL, 이메일, 전화번호를 추출하고, 이를 검증하여 피싱 여부를 판단하는 다양한 API가 포함됩니다. 특히, **Google Safe Browsing API**와 **PhishTank API**를 연동하여 실시간으로 URL의 안전성을 확인하는 검증 과정을 강화하였습니다.

---

#### 2.2 주요 API 기능

---

##### 2.2.1 파싱 API
파싱 API는 사용자로부터 전달받은 메시지 내에서 URL, 이메일, 전화번호와 같은 중요한 정보를 추출합니다. 추출된 데이터를 바탕으로 검증 API에서 피싱 여부를 확인합니다.

- **요청 예시**:
  ```json
  {
    "message": "[Web발신] 국민건강보험공단: 건강검진 결과가 발송되었습니다. http://bit.ly/short 확인하세요."
  }
  ```

- **추출된 데이터**:
  - URL: http://bit.ly/short
  - 이메일: 없음
  - 전화번호: 없음

---

##### 2.2.2 Validate API
Validate API는 두 가지 검증 과정을 통해 메시지의 피싱 여부를 판단합니다:

1. **단축 URL 원본 주소 확인**: 단축 URL의 원본 주소를 추출하여 검증. 단축된 URL은 악성 사이트로 연결될 가능성이 높아 이를 원본 주소로 변환 후 검증합니다.
2. **특수문자 처리 및 유사 이메일 도메인 검증**: 이메일에 키릴 문자나 유사한 이메일 도메인(예: "facebok", "never")이 포함된 경우 예외를 발생시켜 피싱 가능성을 알립니다.

- **요청 예시**:
  ```json
  {
    "message": "[Web발신] 국민건강보험공단: 건강검진 결과가 발송되었습니다. http://bit.ly/short 확인하세요."
  }
  ```

---

##### 2.2.3 URL 검증 API

Google Safe Browsing API와 PhishTank API를 사용하여 URL을 검증합니다. 두 API가 모두 안전하다고 판단하는 경우 `true`를 반환하며, 그렇지 않을 경우 `false`를 반환하여 실시간으로 URL의 안전성을 평가합니다.

- **API 연동 예시**:
  - Google Safe Browsing API: [API 문서 링크](https://developers.google.com/safe-browsing/v4/lookup-api?hl=ko)
  - PhishTank API: [API 문서 링크](https://www.phishtank.com/)

- **결과 예시**:
  ```json
  {
    "isPhishing": false,
    "originalUrl": "http://원본주소"
  }
  ```

---

#### 3. 구현 세부 사항

---

##### 3.1 URL 확장 및 단축 URL 검증

`UrlExpanderService`는 HTTP 요청을 통해 단축된 URL의 원본 주소를 확인하고, 이를 검증 API에서 URL 안전성을 판단하는 데 사용합니다. HTTP의 HEAD 요청을 사용하여 리디렉션 여부를 확인하고, Location 헤더 값에서 원본 URL을 추출합니다.

- **주요 기능**:
  - URL 길이나 단축 URL 도메인(`bit.ly`, `goo.gl`, `tinyurl.com`)이 포함된 경우 원본 URL로 변환합니다.
  - HTTP 응답 코드(301, 302 등)에 따라 리디렉트가 발생한 경우 Location 헤더에서 원본 URL을 추출합니다.

---

##### 3.2 이메일 및 URL 검증

**ValidateService**는 입력된 이메일 및 URL을 검증하여 피싱 여부를 판단합니다. 

1. **유사 도메인 검증**: Levenshtein 거리 알고리즘을 사용하여 이메일 도메인이 유명한 도메인과 유사한지 여부를 계산합니다. 유사성이 높은 경우 예외를 발생시켜 피싱 의심을 알립니다.

   - **알고리즘 설명**: Levenshtein 거리 알고리즘은 두 문자열 사이의 최소 편집 거리를 계산하여 문자열 간 유사성을 평가합니다. 예를 들어 `google.com`과 `gooogle.com`의 편집 거리가 1일 때 유사 도메인으로 간주할 수 있습니다.

2. **키릴 문자 검출**: 이메일 및 URL에 키릴 문자가 포함되어 있는지 확인합니다. 정규 표현식을 사용하여 피싱에 자주 사용되는 특수 문자인 키릴 문자를 검출하고 예외를 발생시킵니다.

---

##### 3.3 서비스 통합 및 로깅

Spring Boot의 Slf4j 로깅 기능을 도입하여 전체 흐름을 추적하고, 발생하는 문제를 파악하여 즉각적인 대응이 가능합니다. 모든 주요 API 호출과 검증 과정에서 발생하는 이벤트와 오류를 로그로 기록하여 향후 문제 해결 및 시스템 개선에 필요한 데이터를 제공합니다.

---

##### 3.4 HTTP 예외 처리 및 안정성 확보

Google Safe Browsing API나 PhishTank API 호출 중 발생할 수 있는 예외 상황을 로깅하여 문제 해결을 위한 정보를 제공합니다. HTTP 응답 상태에 따라 결과를 처리하며, 예외 상황 발생 시 로그에 기록하여 분석이 가능하도록 설계되었습니다.

- **주요 처리 방법**:
  - HTTP 응답 코드가 200이 아닌 경우 URL 검증 결과를 'unknown'으로 처리하고, 예외 상황을 로그로 기록하여 추후 분석에 활용할 수 있습니다.

---

### 🔐 데이터 보호 및 보안 정책

1. **SSL/TLS 암호화**: 사용자와 서버 간의 모든 통신을 암호화하여 데이터 안전성을 확보합니다.
2. **API 인증 및 권한 관리**: 사용자의 접근 권한을 철저히 관리하고, 인증 절차를 강화하여 외부 공격으로부터 데이터를 보호합니다.
3. **개인정보 보호 및 익명화**: 수집된 데이터는 법적 요구 사항을 준수하며, 필요 시 익명화하여 처리됩니다.

---

### 🌐 서비스 배포 및 운영

- **배포 환경**: Kubernetes, Docker, ArgoCD를 사용하여 안정적인 컨테이너 기반 운영 환경을 구축했습니다.
- **CI/CD 파이프라인**: GitLab과 Jenkins를 활용하여 자동화된 빌드 및 배포 과정을 지원하며, Nexus로 이미지를 관리합니다.
- **모니터링**: Kubernetes Dashboard를 이용해 실시간 리소스 사용량을 가시적으로 관리하고, 각 Pod의 상태를 모니터링합니다.

---

### 📈 성능 최적화 및 확장성

1. **비동기 처리 및 캐싱**: 빠른 응답을 위해 비동기 처리와 데이터 캐싱을 적용하여 실시간 피싱 탐지 반응 속도를 최적화했습니다.
2. **클러스터 확장**: Kubernetes의 오토스케일링을 통해 사용자 수와 트래픽에 따라 동적으로 확장 가능하며, 서비스 가용성을 높입니다.

---

### 📊 데이터 및 성능 모니터링 도구

- **Kubernetes Dashboard**: Pod 상태, 리소스 사용량, 서비스 상태를 실시간으로 모니터링합니다.
- **로그 관리 및 알림 설정**: 로그를 수집하여 실시간 오류 추적 및 자동 알림 설정을 통해 장애를 사전 예방합니다.


---

### 📊 프로젝트 성과
- **사용자 친화적 인터페이스**로 디지털 취약계층의 접근성을 높임
- **실시간 피싱 경고**를 통해 문자 피싱 피해를 예방
- **AI 기반 탐지**로 고정밀 피싱 감지 모델 구축

---

### 성능 최적화 및 확장 가능성

---

#### 🔄 성능 최적화 방법

피싱 탐지 앱의 성능을 최적화하기 위해 다음과 같은 방안을 적용했습니다:

- **데이터베이스 쿼리 최적화**: 필요에 따라 인덱싱을 적용하고, 쿼리 구조를 최적화하여 데이터 검색 속도를 높였습니다.
- **캐싱 전략 구현**: 빈번하게 참조되는 데이터를 캐싱하여 API 응답 시간을 단축했습니다.
- **비동기 처리**: 병목이 발생할 수 있는 작업을 비동기로 처리하여, 앱의 실시간 반응 속도를 개선했습니다.

특히, 노인층 사용자가 실시간으로 피싱 경고를 받을 수 있도록 빠른 데이터 처리와 응답 속도 확보가 필수적입니다. 이를 위해 성능 모니터링 도구를 활용하여 애플리케이션의 병목 현상을 분석하고, 정기적인 성능 점검과 개선 작업을 지속적으로 수행하고 있습니다.

---

#### 📈 클러스터 확장 전략 및 계획

사용자 수 증가와 트래픽 변동을 대비하여 안정적인 서비스 운영을 위한 클러스터 확장 전략을 수립하였습니다:

- **수평 확장(Horizontal Scaling)**: 클러스터에 새로운 노드를 추가하여 부하를 분산하고, 성능을 향상시키기 위한 확장 가능한 인프라를 구축했습니다.
- **자동 스케일링(Auto-Scaling)**: 트래픽에 따라 동적으로 리소스를 조정하여 가용성을 높이며, 사용자 증가에 따른 성능 저하를 최소화합니다.
- **클라우드 기반 인프라**: 클라우드 환경을 통해 리소스를 즉시 확장할 수 있는 유연한 시스템을 구현하여 필요 시 신속하게 대응할 수 있습니다.

이러한 확장 및 최적화 전략을 통해, 노인층 사용자를 포함한 모든 사용자가 안정적으로 피싱 탐지 서비스를 이용할 수 있도록 지원하며, 서비스의 신뢰성을 강화하였습니다.


---
## Git Convention

Hotfix

- 치명적인 버그 긴급 수정

Chore

- 빌드 업무, 패키지 매니저, 패키지 관리자 구성 등 업데이트 / 프로덕션 코드 변경 없음



Comment

- 주석 추가 및 변경



Docs

- 문서 수정



Feat

- 신규 기능 추가



Fix

- 버그 수정



Refactor

- 프로덕션 코드 리팩토링



Style

- 코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우



Test

- 테스트 코드 추가 / 프로덕션 코드 변경 없음

--- 

## Architecture

1. 서비스 전체 아키텍쳐
![ClPaaS - 서비스 전체 아키텍처](https://github.com/user-attachments/assets/bbe399b7-b8a6-4411-9f6c-b451b567aa33)

2. k8s 아키텍쳐
![ClPaaS - k8s architecture](https://github.com/user-attachments/assets/645c93d9-5d67-496b-8a92-8f28faf02f1b)

3. k8s 아키텍쳐 - 컨트롤플레인 구조
![ClPaaS - Page 4](https://github.com/user-attachments/assets/dbc10ddf-c759-4e1f-bfd9-baa738cffa33)

4. 사용자 화면 흐름도
![ClPaaS - userflow](https://github.com/user-attachments/assets/7c61c287-337d-443c-82c0-651c9a685334)

--

## Tool

FrontEnd : Android <br>
BackEnd : Spring boot, python , Nest JS <br>
API : phishtank, openAI <br>
Infra : kubernetes, jenkins, nexus, dockerhub, ArgoCD , kustomize , kubernetes dashboard <br>



