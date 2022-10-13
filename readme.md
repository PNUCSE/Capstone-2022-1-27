# 클라우드 게이밍 시스템 개발

## 1. 프로젝트 소개

하드웨어 사양에 따른 제약, OS나 플랫폼에 따른 제약을 보다 개선하기 위해 Unity Render Streaming 기술을 활용하여 웹에서 게임을 즐길 수 있는 것을 목표로 프로젝트를 진행

## 2. 팀소개

### 금정산삼고라니 팀

<table>
  <tr>
    <td>
      <img src="https://github.com/gusah009.png" width="100px;" alt="shasuri"/>
      <br>
      정현모 <a href="https://www.github.com/gusah009"><b>@gusah009</b></a>
    </td>
    <td>
      <ul>
        <li>백엔드 개발(Spring Boot)</li>
        <li>로깅 개발(ELK)</li>
        <li><a href = "mailto: gusah009@naver.com">gusah009@naver.com</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td >
      <img src="https://github.com/shasuri.png" width="100px;" alt="shasuri"/>
      <br>
      이재욱 <a href="https://www.github.com/shasuri"><b>@shasuri</b></a>
    </td>
    <td>
      <ul>
        <li>DB 설계(Postgres</code>)</li>
        <li>Unity 개발</li>
        <li><a href = "mailto: ghimmk@naver.com">ghimmk@naver.com</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/redundant4u.png" width="100px;" alt="redundant4u"/>
      <br>
      전설 <a href="https://www.github.com/redundant4u"><b>@redundant4u</b></a>
    </td>
    <td>
      <ul>
        <li>Unity 개발</li>
        <li>인프라 구축</li>
        <li>프론트 개발</li>
        <li><a href = "mailto: physiogel@pusan.ac.kr">physiogel@pusan.ac.kr</a></li>
      </ul>
    </td>
  </tr>
</table>

## 3. 구성도

### Repository

- [database](https://github.com/9orani/database.git)
  - postgres db sql 모음
- [fps-microgame-urs](https://github.com/9orani/fps-microgame-urs.git)
  - Unity Render Streaming이 적용된 fps 컨셉의 unity 게임
- [front](https://github.com/9orani/front.git)
  - 프론트 관련 코드 모음
  - 시그널링 서버 설정 파일 관리(stun, turn)
  - WebRTC를 통한 비디오 수신
  - WebRTC 연결 관련 테스트 코드 작성
- [server](https://github.com/9orani/server.git)
  - 백엔드 관련 코드 모음
  - 로그인, 방 생성 로직 작성
  - 테스트 코드 작성
- [unity_server](https://github.com/9orani/unity_server.git)
  - Unity Render Streaming이 적용된 교실 컨셉의 unity 게임([Eggcation](https://github.com/LINKER-PNU/LINKER_UNITY)) 작성
- [webrtc](https://github.com/9orani/webrtc.git)
  - 시그널링 서버
  - 프론트와 unity 게임 사이 연결을 위한 통로 역할
  - WebRTC 통신 관련 테스트 코드 작성

### 전체 인프라 구조

<img src="https://user-images.githubusercontent.com/38307839/195511686-beaee34d-4f36-4a72-89f7-6daa1716145f.png" width="600" alt="gorani">

## 4. 시연 영상

## 5. 설치 및 사용법

클라우드 게이밍 시스템 구축을 위해서는 다음의 환경이 필요합니다.

- 시그널링 서버
- Unity Render Streaming이 적용된 unity 게임을 실행할 수 있는 서버
- 프론트, 백엔드, DB 서버

---

[시그널링 서버](https://github.com/9orani/webrtc.git)와 [프론트 서버](https://github.com/9orani/front.git)는 docker를 통하여 구축할 수 있습니다.

```bash
# .env 파일 작성 후
docker-compose up -d
```

백엔드 같은 경우 [server](https://github.com/9orani/server.git)의 코드를 빌드 한 후 결과물을 통해 구축할 수 있습니다.

```bash
gradle build
java -jar [JAR_BUILD_NAME].jar
```

Unity Render Streaming가 적용된 게임 예제는 [unity_server](https://github.com/9orani/unity_server.git)와 [fps-microgame-urs](https://github.com/9orani/fps-microgame-urs.git)에서 확인 할 수 있습니다.

##### <i>special thanks to [zetwhite](https://github.com/zetwhite)</i>
