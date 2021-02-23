# html tip

- a tag 속성에 target="_blank" 를 추가하면 새로운 탭으로 이동. 



# css tip

  * class vs id
    - 같은 클래스 이름을 여러 요소가 가질 수 있지만, 같은 아이디를 여러 요소가 공유할 수는 없다.
    - 한 요소가 여러 클래스를 가질 수 있지만, 한 요소는 하나의 아이디만 가질 수 있다. (단, 한 요소가 클래스도 여러 개 갖고 아이디도 하나 가질 수 있다!)

  * font-weight
    - font-weight 속성이 지원하는 값은 100, 200, 300 ,,,,, 900 이다.  
    - font와 브라우저에 따라 사용 가능한 font-weight가 정해져있다. -> test 해보며 사용하기
    - font-weight: normal; = font-weight: 400 / font-weight: bold; =  font-weight: 700

  * font-family
    - font-family: 폰트1, 폰트2, 폰트종류 -> 폰트 1이 없으면 폰트 2로 설정하고, 그것도 없으면 폰트 종류 중에 설치되어있는 것으로 설정

  * text-align
    - a tag 를 가운데 정렬할 때는 div tag로 감싸주기

  * text-decoration
    - a tag의 밑줄을 없애기 위해서는 text-decoration: none; 속성을 추가한다.

  * image 가운데 정렬
    - display: block; margin-left: auto; margin-right: auto;
