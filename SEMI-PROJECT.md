# 11월 24일 세미 프로젝트 과제

## 주제

Ubuntu VM에 앤서블 플레이북을 작성하여 Wordpress를 자동화 배포하기

## 참고 링크

[Install and configure WordPress](https://ubuntu.com/tutorials/install-and-configure-wordpress#1-overview)

## 과제

단일 VM에 Apache + Wordpress + MySQL 데이터베이스 배포 플레이북 작성

## (옵션) 도전 과제

두개의 VM(워드프레스, 데이터베이스)에 Wordpress 배포 플레이북 작성

- 워드프레스 VM: Apache + Wordpress 배포
- 데이터베이스 VM: MySQL 데이터베이스 배포

### 관리 노드 2대 생성 방법

`Vagrantfile`

```ruby
...
  $number_of_nodes = 2
...
```

```bash
vagrant up
```

## 제출 및 프로젝트 방법

지금 까지 학습한 내용 중 필요한 기능을 사용

- 변수, 조회, 필터, 팩트 변수, 특수 변수, 템플릿
- 반복, 조건, 위임, 블록, 오류처리
- 등

현재 스터디 조 인원이 함께 의견 나누며 소회의실에서 프로젝트 진행

제출 방법:

- sgjang@nobreak.co.kr 이메일
  - 개인 제출이 아니라 조별 아무나 한사람이 완성본 제출
  - 아래 첨부 방법 중 하나 택일
    - Git 저장소 주소 공유
    - (단일 파일) 그냥 첨부
    - (여러 파일) zip 압축으로 첨부

