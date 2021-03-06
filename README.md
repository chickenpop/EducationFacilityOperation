
# DB 프로젝트
> 오라클 서버로 교육센터 운영에 필요한 DB를 구현하였습니다. (진행기간: 2022.05. 11일 ~ 05.20)

## 개발환경/도구

<img src="https://img.shields.io/badge/Oracle Database 11g-F80000?style=for-the-badge&logo=Oracle&logoColor=white"> <img src="https://img.shields.io/badge/eXERD-7952B3?style=for-the-badge&logo=Bootstrap-7952B3&logoColor=white"> <img src="https://img.shields.io/badge/SQL Developer-4169E1?style=for-the-badge&logo=SQL Developer-4169E1&logoColor=white">
  
### ERD
![DBErd](https://user-images.githubusercontent.com/50548923/181484669-40030eed-9ac5-4bfd-acc1-a967cf47889f.png)
  
## 핵심 업무

[공통]
- 교육기관에서 과정을 구성하고 강의 일정을 운영하는 것을 목표
- 교육기관에서 과정을 수강한 교육생들에 대한 전반적인 관리를 목표
- 운영을 위해 관리자, 교사, 교육생으로 사용자를 구분

[관리자]
- 기초 정보 관리	교사 계정 관리 및 개설 과정, 개설 과목에 사용하게 될 기초 정보를 등록 및 관리
- 교사/교육생 관리	여러 명의 교사와 교육생 정보를 등록 및 관리
- 출결 관리 및 조회	특정 개설 과정을 선택하는 경우 다양한 방식으로 조회 및 시스템 관리
- 개설 과정/과목 관리	여러 개의 개설 과정과 과목을 등록 및 관리
- 훈련비 지급 관리	훈련비 측정 시스템을 관리
- 전체 상담 관리	전반적인 상담시스템을 등록 및 관리

[교사]
- 개인 정보 조회	자신의 강의 스케줄을 확인
- 배점 입출력	강의를 마친 과목에 대한 성적 처리를 위해서 배점 입출력
- 성적 정보 관리	강의를 마친 과목에 대한 성적 처리를 위해서 성적 입출력
- 교육생 출결 관리	강의한 과정에 한해 선택하는 경우 모든 교육생의 출결을 조회
- 교육생 상담 관리	교육생의 상담 내용 관리

[교육생]
- 훈련비 조회	본인의 월 별 훈련비 조회 가능
- 상담 내역 관리	진행 과목에 대한 상담 조회 및 관리
- 출결 관리 및 조회	매일 근태 기록 및 현황 조회


### 개인 아이디어 : 학생들의 취업관리를 도울 수 있는 제도 

- 수료한 학생은 개인 포트폴리오를 교육센터에서 보관해줄수있다.

- 교육센터에서는 수료한 학생이 6개월동안 원하는 기업을 조회할 수 있는 데이터를 관리한다.

- 수료한 학생은 기업을 업종, 모집분야, 구인형태에 따라 조회할 수 있다.

### 개인 파트
- 구현
  - [관리자] 수료 교육생 취업활동 관리, 협력기업관리, 개설 과정관리 수료날짜 지정, 출결 관리 및 출결 조회
  - [교사] 배점 입출력
  - [교육생] 수료 교육생 취업활동 조회, 협력기업 조회
- 개인 작업 파일 위치  
  - [ANSI-SQL](https://github.com/chickenpop/EducationFacilityOperation/tree/master/6.%EC%BF%BC%EB%A6%AC%EB%AC%B8/ANSI)
  - [PL-SQL](https://github.com/chickenpop/EducationFacilityOperation/tree/master/6.%EC%BF%BC%EB%A6%AC%EB%AC%B8/PL)

## 진행하면서 느낀점
- 쿼리문을 작성하는 거 자체는 어렵지 않았지만, 논리적 오류나 데이터의 관계를 이해하지 못했던 부분에서 문제가 발생했었다
- 해결을 위해 간단하게 구조를 생각하여 쿼리문을 작성, 테스트하고 팀원들과 연결과정이 맞는 지 서로 소통하면서 진행하였다. 덕분에 원하는 결과가 나오는 프로시저, 뷰, select문 등을 생성할 수 있었다
