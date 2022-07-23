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

## 메이븐 프로젝트 생성시 오류와 해결방법

![image](https://user-images.githubusercontent.com/58906858/180588063-3f712923-7e05-43c9-927b-e86ade529498.png)

메이븐 프로젝트 생성 시 다음과 같은 오류가 발생한다면 워크스페이스 아래에 pom.xml 파일이 있는 지 확인해봐야한다.
Are you running the command from a directory that has an existing pom.xml file in it? I think that may be confusing Maven, as it thinks you're trying to add your new project as a sub-module of the project in the working directory.
기존 pom.xml 파일이 있는 디렉토리에서 명령을 실행하고 있습니까? 메이븐이 새 프로젝트를 작업 디렉터리에 있는 프로젝트의 하위 모듈로 추가하려고 한다고 생각하기 때문에 혼란스러울 수 있다고 생각합니다.
알고 보니 워크스페이스 아래에 POM 파일을 두었는데, 이것이 M2일식 플러그인에 대한 오해의 원인이 되었습니다. 삭제하면 됩니다.

이런 답변을 얻었고 워크스페이스 파일에 pom.xml 파일이 있던 나는 pom.xml 파일을 삭제하자 정상적으로 프로젝트가 생성되었다.
