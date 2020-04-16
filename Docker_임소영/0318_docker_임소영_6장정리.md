4~5장 실습

# 6장 Docker 이미지 공개
-GitHub, Bitbucket 연결하여 Automated Build 기능 : dockfile을 바탕으로 Docker 이미지를 자동으로 빌드함.

## 6.1 docker 이미지의 자동생성 및 공개
- GitHub에 Dockerfile 공개
- Docker Hub 로그인 후, GitHub와 연결 설정
- GitHub 상의 dockerfile오 Docker Hub에 이미지 생성
- 이미지 다운로드 후 확인

## 6.2 Docker Registry를 사용한 프라이빗 레지스트리 구축
- 로컬 환경에 Docker 레지스트리 구축 : registry 검색하여 다운로드, 컨테이너 시작 후 확인
- Docker 이미지 업로드 : dockerfile 로 빌드하고 업로드(로컬 이미지 삭제) 
	-> dockerfile 버전설치 오류 (설치버전 재확인)
- Docker 이미지 다운로드와 작동 환경 

## 6.3 클라우드 서비스를 사용한 브라이빗 레지스트리 구축
- GCP Container Registry : 구글 GCP 활성화, 프로젝트 생성, API라이브러리(Container Registry)설정

- gcloud 사용준비

- 참조 : https://cloud.google.com/sdk/docs/quickstart-debian-ubuntu

$ sudo echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] http://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

$ sudo curl https://packages.cloud.google.com/apt/doc/apt-key.gpg |  apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -

$ sudo apt-get update && sudo apt-get install google-cloud-sdk

- gcloud 초기설정

 $ gcloud init

 $ gcloud auth login
	project ID: solar-muse-271408
	zone : asia-east2-c

- Docker 이미지 업로드
	에러 발생
	(gcloud로 GCP 이미지 업로드 에러)
