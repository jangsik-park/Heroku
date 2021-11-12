# **Heroku**
Flask App을 Heroku에 배포하는 과정을 설명합니다.

## Heroku란?
Heroku는 Java, Node.js, Python등 여러 언어를 지원하는 클라우드 Paas이다.

※ Paas란?

서비스형 플랫폼(Platform as a Service, PaaS)은 클라우드 컴퓨팅 서비스 분류 중 하나다. 일반적으로 앱을 개발하거나 구현할 때, 관련 인프라를 만들고 유지보수하는 복잡함 없이 애플리케이션을 개발, 실행, 관리할 수 있게 하는 플랫폼을 제공한다. SaaS의 개념을 개발 플랫폼에도 확장한 방식으로, 개발을 위한 플랫폼을 구축할 필요 없이, 필요한 개발 요소를 웹에서 쉽게 빌려쓸 수 있게 하는 모델이다.

## 과정

[Heroku 배포](https://ebbnflow.tistory.com/220)
<br>
[배포후 수정 방법](https://velog.io/@ansfls/Heroku%EB%A1%9C-%EA%B0%84%EB%8B%A8%ED%95%98%EA%B2%8C-%EC%9B%B9-%EC%82%AC%EC%9D%B4%ED%8A%B8-%EB%B0%B0%ED%8F%AC%ED%95%98%EA%B8%B0)

## 진행하면서 생긴 Error

### 1. heroku에 파일 올릴 때 requirements.txt 안에 파일과 관련된 오류

- ex) JPype1==C:\Anaconda\envs\flask\JPype1-1.0.2-cp38-cp38-win_amd64.whl [형태](https://github.com/jangsik-park/Heroku)로 되어 있는 것을 ```JPype1==1.0``` 이런 식으로 수정함
  - 애초에 새로운 가상환경을 만들어서 필수적인 라이브러리만 설치하면 깔끔하다.<br>
-   tensorflow의 용량이 [너무 커서](https://github.com/jangsik-park/Heroku) ```tensorflow-cpu```를 설치함 (애초에 gpu사용은 heroku에서 불가능하다.) <br>
-   ```git remote add [주소] ``` 를 해주지 않아서 Error 발생함 <br>
    - ```git remote -v``` 를 통해 현재 어떤 github 주소를 바라보고 있는지 확인해야 한다.<br>
  
- 또 하나, Heroku내에서 처음 탐색(?)하는 언어를 python으로 설정하는 방법을 통해 Error를 해결했었는데  [이건 찾아봐야겠다](https://github.com/jangsik-park/Heroku) (까먹음) <br>
- 처음 배포 할 때는 ```git init```을 통해 초기화 해주는 과정이 필요하다


## 결과

[웹사이트 주소](https://jangapp.herokuapp.com/)

![image](https://user-images.githubusercontent.com/56535821/141412263-e658e257-0899-4754-9556-02ffdcaefb19.png)




  
