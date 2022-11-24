# 🎞 Whyisitreal?

- Whyisitreal (이왜진)은 평가 데이터에 기반한 영화 리뷰 / 추천 기능을 제공하는 커뮤니티 서비스입니다.

---

### 🛠 Tech Stack & Tool

- BackEnd: `Python 3.10.1`  `Django 3.2.13`
- FrontEnd: `HTML` `CSS` `Javascript` `Vue 2.7.14`
- Design: `Bootstarp` `Figma`
- Others: `Git` `Notion` `Visual Studio Code` `Octopus.do` `Draw.io`

## 👫 팀원 및 역할 분담

- 이예진 : `FrontEnd Main`, `BackEnd Sub`, `Design`
- 손민혁 : `BackEnd Main,` `FrontEnd Sub`, `Algorithm`

---

### 🛫 Why Whyisitreal?

1. 서비스의 필요성
    
    다양한 영화와 플랫폼들이 쏟아지면서 자신에게 맞는 영화를 시청하고 싶어하는 사용자가 증가하고 있다. 기존 서비스들은 영화 추천 기능 또는 커뮤니티 기능만 존재하기 때문에 모두 한 번에 이용하고 싶어하는 사용자들에게 불편함이 존재한다.
    
2. 서비스 사용자
    
    영화 검색 시간을 줄여 자신의 취향에 맞는 영화를 추천받아 시청하고, 영화에 대한 리뷰를 남겨 타인과 공유하고 싶어하는 10-30대 (이후 확장 예정)
    
3. 현 유사 서비스
    - 영화 추천 서비스
        1. 넷플릭스 
            - 유사 사용자 기반 알고리즘, 유사 아이템 기반 알고리즘, 잠재 모델 기반 알고리즘, 콘텐츠 기반 알고리즘
            
            [넷플릭스의 영화 추천 알고리즘](https://brunch.co.kr/@cysstory/159)
            
        2. 왓챠
            - 유사 사용자 기반 알고리즘, 유사 콘텐츠 기반 알고리즘
            - 넷플릭스와 차이점이 있다면 왓챠는 가입단계에서 정확한 데이터(취향)를 사용자에게 요구함
            
            [넷플릭스와 왓챠 영화추천 알고리즘](https://bumi1004.tistory.com/entry/%EB%84%B7%ED%94%8C%EB%A6%AD%EC%8A%A4-%EC%99%93%EC%B1%A0-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)
            
        
        - 기존 OTT 서비스는 주로 시청 시간, 시청 기간대, 시청 디바이스, 재시청 비율 등 다양한 데이터를 바탕으로 추천 알고리즘을 마련하는데,  API를 가져다 쓰는 우리는 이러한 기반의 알고리즘을 구현하기 쉽지 않았다.
            
            → 그래서 기존 잘 구현된 알고리즘을 바탕으로 우리만의 아이디어를 활용해 새로운 알고리즘을 구현했다.
            

- 영화 커뮤니티 서비스
    1. 왓챠
        - 각 영화별 평점과 간단한 코멘트가 있어 직관적이지만 댓글을 달거나 자세한 리뷰를 작성할 수는 없음.
        
        ![watcha](https://user-images.githubusercontent.com/67399771/203859780-80bbb170-734f-46ca-a852-fdecbfbf6b14.png)
        
    2. 네이버 영화
        - 영화에 대한 리뷰(자세함) / 평점(간단한 코멘트)가 있음. 또한 추천과 좋아요 /기능이 있어 타 사용자들의  커뮤니케이션이 비교적 활발한 편.
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c0cd7bc-5c3b-47a9-bb68-8091a3b380fe/Untitled.png)
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/caa4a396-4093-4854-baa9-f51842ce880c/Untitled.png)
        
    - 직관성/편리성 vs 자세한 정보 제공이라는 각각의 장점이 존재
    
    → 직관성과 편리성이 UX 측면에서 더 가치있다고 판단하여 영화에 대한 간단한 리뷰 기능만 구현하기로 결정
    

---

### 🛫 About Whyisitreal

- ERD
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cd1bcee2-1bfd-4dca-9a97-53d85979cff1/Untitled.png)
    

- 컴포넌트 구조도
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/13d23efc-6201-4b32-a985-e2edfeca6d02/Untitled.png)
    

- 서비스 주기능, 부기능(상세기능)
    - 주기능 (MVP)
        - 사용자 좋아요 기반 영화 추천
        - 영화별 리뷰 커뮤니티
    - 부기능
        - 최신 영화 추천
        - 관련 영화 추천
        - 오늘의 영화 추천
        - 나만 당할 수 없지 영화 추천 (최하 평점, 최하 관객 수 영화)
        - 영화 검색 기능
        - 프로필 기능
        
- DB (fixtures)
    - all_movies.json : TopRated 영화 10,000개
    - genres.json : 19개의 영화 장르

- API (TMDB)
    - TopRatedMovies
    - GetMovie
    - Recommendation
    - Latest
    - Similar

- 사용자 좋아요 기반 영화 추천
    - 회원가입 시 48개의 영화 목록을 띄워주는 페이지로 이동해 사용자가 즐겨봤던 영화를 고를 수 있게 합니다.
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2b07bc0b-b3e1-48a5-a3bc-25d604c1cf38/Untitled.png)
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/84e9fcfc-83b0-4ee2-b082-42574f256d57/Untitled.png)
        
        - <알고리즘>
            1. 10,000개의 영화 DB를 for문을 이용해 장르별로 분류
            2. 유저가 기존에 봤던 익숙한 영화를 노출시키기 위해 `popularity` 필드가 100이상인 영화만 필터링
            3. 장르 별 최소 1개 이상의 영화가 포함될 수 있도록 하여 사용자에게 노출 (genre_id 99번인 다큐멘터리는 10,000개 DB에 하나도 없으므로 제외)
            
    - 사용자가 좋아요를 누른 영화에 대한 정보를 기반으로 다른 영화를 추천해줍니다.
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/da4e3e22-ce75-42dc-8f2c-569dc302c339/Untitled.png)
        
    
    - <알고리즘>
        1. 해당 사용자를 불러와서 `like_movies.all()`을 사용하여 좋아요한 영화 리스트를 생성
        2. for문으로 list를 순회하여 recommendation API로부터 추천영화 목록을 받아옴
        3. 추천된 영화의 횟수를 카운트하여 중복을 제거하고 내림차순으로 정렬
        4. 0~19번 인덱스까지 슬라이싱해서 가져오고 이 중에서 12개의 영화를 랜덤으로 추출
        5. 12개의 영화가 현재 DB에 존재하지 않는다면 DB에 저장도 해줌
        6. 메인페이지가 렌더링될 때마다 12개의 좋아요 기반 추천영화들을 보여줌
    
- 영화별 리뷰 커뮤니티
    - 관련 영화 추천
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/afa96e64-177c-46cd-a970-5b7d7b7c3265/Untitled.png)
        
    
    - <알고리즘>
        1. Similar API를 이용하여 관련 영화 리스트를 가져옴 (영화당 약 80개의 목록이 조냊)
        2. 관련 영화가 12개 이상이면 랜덤으로 12개의 영화를 추출하여 보여주고, 미만이면 갯수만큼 페이지에 보여줌
    - 영화 좋아요 기능
    - 리뷰 CRUD 기능
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/33a2dd06-350c-46d0-b9c3-4be504a3f660/Untitled.png)
    
    - 리뷰 작성자 클릭시 해당 유저 프로필로 넘어가기 기능

- 최신 영화 추천
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/11f404b1-67b4-4d69-8ea7-530aa89da315/Untitled.png)
    

- <알고리즘>
    1. Latest API를 이용하여 3페이지까지 (약 120개)의 영화를 불러옴 (페이지가 더 존재하지만 이미 popularity 기준 내림차순으로 정렬되어 있어 그 이후 영화를 가져오는 것은 무의미하다고 판단했기 때문)
    2. 120개의 영화 중에서 12개를 랜덤으로 추출
    3. 12개의 영화가 기존 DB에 없다면 DB에 저장해줌 (DB에 없으면 영화 Detail 페이지에 정보를 노출할 수 없기 때문)
    4. 메인페이지가 렌더링될 때마다 12개의 최신 영화들을 보여줌
    
- 오늘의 영화 추천
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/827e8d2f-c6c9-4c14-a0a2-e1553b72c159/Untitled.png)
    
    - <알고리즘>
        1. 현재 날짜 (ex) 20221124) int화하여 일정한 식을 만든 뒤 이와 가장 근접한 movie_id를 추천해줌

- 나만 당할 수 없지 영화 추천 (이런 영화도 있어요!)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8f9f4465-2e0a-403f-8410-62b56672b612/Untitled.png)
    
    - <알고리즘>
        1. DB에서 popularity가 20 미만,  vote_average가 5.5 미만인 영화들을 뽑아서 1개를 랜덤으로 추천해줌

- 영화 검색 기능

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b4eab0a9-dce1-4405-abc1-0185ae5159a0/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a519d1dc-1ce6-411e-b2ed-726ef0fc62fa/Untitled.png)

- 글자단위로 검색가능

- 프로필 페이지

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b07931bc-cc63-43ce-83d5-4437dde72f7a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edd718a7-a28d-43a6-9a30-dd660248a298/Untitled.png)

- 프로필 이미지 업로드 기능
- 내가 좋아요한 영화 목록
- 내가 작성한 리뷰 목록

---

### 💡우리들의 오류 목록

---

### 📗 느낀점

- 손민혁 :
- 이예진 :
