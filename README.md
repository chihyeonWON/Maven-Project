# Maven-Project
Maven Project 

## 메이븐 프로젝트

메이븐 프로젝트는 이클립스에서 생성하거나, 도스 명령행에서 mvn 명령어를 사용하여 생성하는 방법이 있다.

첫 번째로 진행할 실습은 메이븐 구조를 이해하기 위해서, 메이븐 아키타입 플러그인을 이용하여 메이븐 프로젝트를 생성한다.   

https://maven.apache.org/archetype/maven-archetype-plugin/usage.html에서 해당 플러그인의 정보를 확인한다.   
아키타입 플러그인은 정해진 구조로 프로젝트를 생성해 주기도 하고, 기존 프로젝트로부터 메이븐 프로젝트를 만들어 주기도 한다.

m2eclipse를 사용하면 이클립스 안에서 메이븐의 디펜던시 설정, 플러그인 설정, pom.xml의 편집, 리포팅 설정 등을 간편하게 실행할 수 있다.   

먼저 이클립스에서 New -> Other -> Maven -> Maven Project 를 선택한다.   

org.apache.maven.archetypes의 maven-archetype-quickstart 1.4을 선택한다.
![image](https://user-images.githubusercontent.com/58906858/180365186-b46b074a-99d5-4a04-8482-cfd93a915cf1.png)

GroupId, Artifact Id, Version, Package는 다음과 같이 입력한다.
![image](https://user-images.githubusercontent.com/58906858/180365297-f43c8491-2b04-4b53-ab03-9293eba539bf.png)

생성된 프로젝트의 구조는 다음과 같다.
![image](https://user-images.githubusercontent.com/58906858/180374807-b67ac0fa-5272-43d5-b5c4-f4fbae792553.png)
  
