## #1 INTRODUCTION

### 1.5 What Makes a Website?

    - Website is just text
    - 브라우저 understands your code

### 1.6 What is HTML

    - text -> language
    - website made of 3 lang : HTML, CSS, JS

    HTML : Hypertext Markup Language
        browser (google chrome, firefox, explorer)
        브라우저에게 웹사이트의 content가 어떻게 구성되어 있는지 설명할때 사용

### 1.7 What is CSS

    CSS : Cascading Style Sheets
    should be use both CSS & HTML
    browser에게 웹사이트가 어떻게 보여야하는지에 대해 알려줌

    HTML은 "brower야 이건 title이야" -> 뼈대
    CSS는 "brower야 그 title은 녹색이어야해" -> 근육

    HTML이 없다면, CSS는 쓸 수 없어

### 1.8 What is JavaScript

    JS : 웹사이트의 뇌 -> 웹 사이트의 동적인 부분
    클릭했을 때 애니메이션
    interactivity
    모든 app이 interactive가 필요한건 아님

### 1.9 Recap

    HTML -> Markup language (Borns)
    CSS -> language for design and style (Mustle)
    JS -> Web Programming language (Brain)

## #2 LEARNING HTML

### 2.0 Our First HTML File

    파일명/폴더명은 항상 소문자로 작성한다
    html -> 확장자명
    파일 내용이 변경될 때 마다, 저장 필수

### 2.1 Setup and Errors

    Extensions에서 테마와 아이콘 설치

### 2.2 Our First HTML Tag

    What is tag -> Html은 tag를 text로 넣음
    <food>김치</food>라는 tag로 인해 브라우저는 김치가 food라는 걸 알게 됨
    tag는 닫아주자
    <h1> ~ <h6>

### 2.3 More Tags and Prettier

    <ul> //unordered list
    <ol> //ordered list
    <list> //list element
    확장프로그램 prettier -> 코드 오류 자동 수정

### 2.4 Tag Attributes

    <a></a> //anchor_닻 -> link
        link는 추가적인 정보가 필요함 -> where we going
        -> tag에 추가하는 부가적인 정보 : attribute(속성)
        * href(attribute) : http reference or hyperlink reference
            href는 오직 a 태그에만 적용할 수 있다.
        * target : default 값 _self , _blank

    <img/> //닫아주는 태그가 존재하지 않음 -> self-closing tag(자체 닫기 태그)
        * src

### 2.5 More Tags and Head

    <!DOCTYPE html> //브라우저에게 text 파일이 아닌 html 문서임을 알려줌
    <html>
        <head> 웹사이트의 환경을 설정 </head>
        <body> 사용자가 볼 수 있는 content </body>
    </html>

### 2.6 Its All About the Head

    <meta> 구글 검색에서 보여지는 description
    구글이 사이트에서 title과 description을 가져오는거야

    <meta charset="utf-8"/> 브라우저에게 text를 어떻게 그려달라는지 말해줌
    * meta 태그는 self closing tag

    <html lang=""> 구글, 네이버, bing 같은 검색 엔진들에게 도움을 주기 위해서

### 2.7 More Tags

    html tags mdn 페이지에서 확인

### 2.8 Form Tags 2.9 More Tags and IDs

    <form>
    <label> form에 question을 추가할 수 있음

    for과 id에 들어가는 값은 동일해야함
    -> for과 같은 값을 가진 id를 들고있는 input을 작동시켜줌

    element당 하나의 id만 가질 수 있음
    전체 html 문서에서 id는 고유해야함

    id : scripting이나 css를 식별하려는 목적을 가진 attribute

### 2.10 Semantic HTML

    <div> - division 분할, 구분, 경계선
    div 는 박스
    <span> - for short text

    <head> != <header>

    <header>, <main>, <footer>  body 안에 포함 되어있는 태그
    div를 대체 할 수 있음 -> 하지만 알아보기 어렵기 때문에 지양

    main, footer, aside 등등 의미가 있는 box를 되도록이면 쓰자

### 2.11 Recap

    Always use ""(큰따옴표) !!

## #3 LEARNING CSS

### 3.0 How to Add CSS to HTML

    어떻게 하면 CSS를 HTML페이지에 추가할 수 있는지를 이해해야 함

    CSS와 HTML을 같이 둘 수도 있고 따로 둘 수도 있음

    방법 1. <head> 태그 내부에 <style> 태그를 작성하고 안에 CSS 기입

    방법 2. CSS 파일을 따로 두고 link로 파일을 연결
    rel(rel="stylesheet" 명시)

    styles.css는 스타일시트

### 3.1 Writing Our First CSS Lines

    selector 안에 속성 properties 명시
    HTML의 어떤 태그를 가리키고 CSS로 잡아와서 쓰면댐

    tag { property : vale; } // 세미콜론 꼭 찍어야함

### 3.2 What Does Cascading Mean

    Cascading 브라우저가 css코드를 읽을때 위에서 부터 차례대로 읽음

    inline CSS / external CSS

    만약 위 두 CSS코드가 같은 대상을 가리키게 되면 어떻게 될까?

    마지막 코드로 적용됨

### 3.3 Blocks and Inlines

    box(div)옆에는 아무것도 오지 않음
    span은 옆에 다른 요소들이 올 수 있음

    box - div , p, address, header
    inline - a(link), span, img

### 3.4 Margin Part One

    block을 inline으로 바꾸는 게 가능할까? ㅇㅇ
    inline을 block 속성으로 변경 : display

    span의 default display 속성 : inline
    inline은 높이와 너비를 가질 수 없음

    box의 엄청난 특징 3가지
    margin padding border

    * margin : box의 border(경계)로부터 바깥에 있는 공간

### 3.5 Margin Part Two

    margin: 0; //사방
    margin:20px 15px; // 위아래_양 옆
    margin: 5px; 10px; 15px; 20px;  //위 오 아래 좌 ( 시계 방향 )

    collapsing margins : 두 박스의 경계가 같다면 두 margin은 하나로 취급됨
