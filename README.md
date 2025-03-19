# 🐳Dockerized Spring Boot Application

# 📝 프로젝트 소개
Spring Boot 애플리케이션을 Docker 환경에서 실행할 수 있도록 도커 이미지로 변환하고, Docker Hub에 업로드하는 프로젝트입니다. 

이 프로젝트에서는 Docker의 기본 개념부터 이미지화, 최적화, 컨테이너 실행까지의 과정을 다룹니다.

# 🎯 프로젝트 목표
- 다양한 환경에서 손쉽게 실행할 수 있도록 Spring Boot 애플리케이션을 Docker화
- 최적화된 Docker 이미지 생성
- Docker Hub에 업로드하여 재사용성 향상

# 💻 개발 환경

<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" /> <img src="https://img.shields.io/badge/VirtualBox-4B6E8E?style=for-the-badge&logo=virtualbox&logoColor=white" alt="VirtualBox" /> <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu" /> <img src="https://img.shields.io/badge/JDK-007396?style=for-the-badge&logo=openjdk&logoColor=white" alt="JDK" /> <img src="https://img.shields.io/badge/JRE-007396?style=for-the-badge&logo=openjdk&logoColor=white" alt="JRE" /> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot" /> 

# 🔨 개발 순서
### 1. JAR 파일 도커 이미지화

   -jar파일, Dockerfile 생성
   
   ![1  jar생성](https://github.com/user-attachments/assets/100a6f49-a4d1-433c-9410-0e220c6fa56c)

   -Dockerfile 내용
   
   ![1  dockerfile 내용](https://github.com/user-attachments/assets/a2dc7953-e3d1-4edf-ae2e-b1a8f34c1d40)

   -Docker 이미지 빌드 및 생성 확인
   
   ![1  docker 이미지 빌드 및 생성 확인](https://github.com/user-attachments/assets/a2358dd8-588d-431f-9893-ff566effc19f)
   ![1  docker 이미지 빌드 및 생성 확인2](https://github.com/user-attachments/assets/3771ef00-a902-45c4-81a4-b833fa3cd024)

   -commit 명령어로 이미지 생성 및 생성 확인
   
   ![1  commit 명령어로 이미지 생성 및 생성 확인](https://github.com/user-attachments/assets/60f77a3e-0893-4b29-bc48-af06e968d26e)
   ![1  commit명령어로 이미지 생성 및 생성확인2](https://github.com/user-attachments/assets/b0344a85-e562-4e33-823a-b3b9ecbd660d)

   -생성된 이미지에 Tag 적용
   
   ![1  생성된 이미지에 tag 적용](https://github.com/user-attachments/assets/4a4ee799-df4d-4894-8324-34f9e3a36710)
   ![1  생성된 이미지에 tag적용](https://github.com/user-attachments/assets/556083f3-587d-4470-abbd-e5db04bf0fe7)

   -도커 hub에 푸쉬
   
   ![1  도커 허브에 푸쉬](https://github.com/user-attachments/assets/914a430c-dfe0-436b-9cf6-f7fafd445cf1)
   ![1  도커 허브에 푸쉬2](https://github.com/user-attachments/assets/09bf655f-b913-413c-abfc-73e4540d4668)

### 2. 이미지 파일 최적화

   -최적화 위해 JDK 대신 실행에 필요한 최소 환경만 제공하는 JRE를 사용(eclipse-temurin:17-jre-alpine)
   
   ![3  이미지파일 최적화1](https://github.com/user-attachments/assets/a5738da7-0d9f-4a8e-b297-f0154beb08dc)

   -용량 JDK보다 경량화
   
   ![3  이미지파일 최적화2](https://github.com/user-attachments/assets/0b3f3e11-5a58-480d-892c-4cc750aacd46)

   
### 3. Docker Hub Pull 받아와 컨테이너 생성 및 실행
   
   -도커 hub에서 pull
   
   ![4  도커 PULL1](https://github.com/user-attachments/assets/a715a6a6-b292-4463-909e-4e529288a89a)
   ![4  도커 PULL2](https://github.com/user-attachments/assets/bcea622f-7a07-4fb8-9015-eee94e6aa05c)

   -도커 컨테이너 생성

   ![4  도커 PULL3](https://github.com/user-attachments/assets/9d5d9767-ff78-415a-958f-bca20a5cd21a)
   ![4  도커 PULL4](https://github.com/user-attachments/assets/cda22e4a-6278-4764-bf89-6574593930ad)

   -스프링 정상 작동 확인
   
   ![4  도커 PULL5](https://github.com/user-attachments/assets/2831a408-f917-479b-8e50-7f4b83e8367f)

### 4. 트러블 슈팅
   
   -도커 hub pull시 tag 미 입력 시 오류 발생 -> tag 입력하여 pull 성공

   ![5  트러블 슈팅](https://github.com/user-attachments/assets/1b7aa5bc-0984-4925-bc40-5143f46de616)

   




      
