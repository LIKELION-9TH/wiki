# 개요

### 버전관리

내가 원하는 시점(버전)으로 이동할 수 있게 해주는 것. 내가 원하는 시점에 표시하고 언제든지 표시한 시점으로 자유롭게 이동할 수 있다. 

### Git & GitHub

Git = 소스코드 버전 관리 시스템

GitHub = Git 호스팅 사이트 (로컬을 서버로!)

# 1. 로컬 저장소에서 커밋 관리하기

### 로컬저장소 만들기

Git과 로컬저장소 연결 = Git 통해서 버전 관리 이루어짐 = 내 컴퓨터(로컬)에 있는 폴더

1. Git Bash Here 

    폴더에서 시작한다. 로컬 저장소 안에서 Git 작업 시작한다!

2. 정보 등록

git config —global [user.email](http://user.email) "[GitHub 이메일]"
git config —global [user.name](http://user.name) "[GitHub 아이디]"

각 버전을 누가 만들었는지 알아야 협업이 가능하기 때문에 GitHub의 계정 정보 등록!

# 2. GitHub 원격저장소 만들기

### 원격저장소 만들기

- 로컬 저장소
- 원격 저장소 = 레포지토리(repository)

원격 저장소는 GitHub 웹 사이트에 프로젝트를 위한 공용 폴더를 만드는 것

"생성 시 name, description, public 확인"

### 원격 저장소의 커밋을 로컬저장소에 내려받기

1. 파일 관리할 폴더 만들기
2. 클론 = 원격 저장소의 코드와 버전 전체를 내 컴퓨터(로컬)에 내려받는 것

    → 최신 버전, 이전 버전, 원격저장소 주소 등이 모두 로컬 저장소에 저장됨

    (처음 클론 한다면 생성 정보만 내려받음!)

    git clone [repo 주소] .
    → 현재 폴더에 받는다는 뜻 (마침표 찍어야 폴더 구조 깔끔함)

    [.git] 폴더가 생성됨 (로컬 저장소 자동으로 생김)
    [.git] 폴더에는 버전 정보와 원격저장소 주소 등이 들어있다. ⇒이 폴더를 로컬저장소라고 부름
    

# 3. 로컬 저장소에서 커밋 관리하기

### ✨커밋 만들기✨ → 반복하는 부분

커밋 = 하나의 버전

1. 커밋(버전)에 추가할 파일 선택

    git add [추가할 파일] (예시: git add README.txt)
    git add . 
    → 모든 파일을 추가하고 싶을 때 사용

2. 커밋 메세지 작성

    git commit -m "[커밋메세지 작성]"

    설명 잘 적어두기! (파일 만든 이유, 수정한 이유) → 원하는 버전 찾기 쉬움

    -m = message

    영어로 적기, 규칙 맞춰서 적기

    ~~어디서 주워들은 바로는...면접관들이 깃헙 볼 때 커밋 메세지 & 브랜치 위주로 본다고 합니다~~

# 4. GitHub 원격저장소에 커밋 올리기

### 원격저장소에 커밋 올리기

![Image](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7bf597f2-9d52-4641-8d1c-2424e5f69108/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20210517%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20210517T124957Z&X-Amz-Expires=86400&X-Amz-Signature=0fa113abfba72defdb5c65ab27834563b9776c688eab8c15ed0b250d9835043b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)

- 원격 저장소가 어디인지 URL을 로컬 저장소에 알려준다. (로컬 저장소는 내 컴퓨터에만 있으니까 repo에 대한 아무런 정보도 없다)
- 로컬 저장소에서 작업을 완료하고 저장해둔 버전(커밋)을 원격 저장소에 올린다.

⚠ 원격 저장소에 올리지 않으면 다른 사람과 코드를 공유할 수 없다! 로컬 저장소는 온전히 나만의 공간임을 잊지 말자!!

1. 원격 저장소에 커밋 올리기

    git push origin [브랜치]
    git push origin main
    → 100% 완료 텍스트 나오면 성공

    로컬 저장소의 커밋을 원격저장소로 push 명령을 사용해서 올린다 = 푸시한다
