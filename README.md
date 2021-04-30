# 코딩 컨벤션 
코딩 컨벤션은 읽고, 관리하기 쉬운 코드를 작성하기 위한 일종의 코딩 스타일 규약이다. 코딩 컨벤션을 준수하면 가독성이 좋아지고, 성능에 영향을 주거나 오류를 발생시키는 잠재적 위험 요소를 줄여준다. 특히 규모가 큰 프로젝트일수록 유지보수 비용을 줄이는 데 도움이 된다.
<br>

## 목차
  * [1. 들여쓰기](#1-----)
  * [2. 문장의 종료](#2-------)
  * [3. 전역변수](#3-----)
  * [4. 주석](#4---)
  * [5. 명명 규칙](#5------)
    + [5-1. 함수, 변수명](#5-1--------)
    + [5-2. 클래스명](#5-2-----)
    + [5-3. static 상수는 스네이크 표기](#5-3-static------------)
    + [5-4. 약어를 단어 취급](#5-4----------)
    + [5-5. 반복문 인덱스](#5-5--------)
  * [6. XML 명명 규칙](#6-xml------)
    + [6-1. Layout](#6-1-layout)
    + [6-2. String](#6-2-string)
    + [6-3. Drawables](#6-3-drawables)
    + [6-4. IDs](#6-4-ids)
    + [6-5. Dimensions](#6-5-dimensions)

<br>

## 1. 들여쓰기
space와 tab을 섞어 사용하지 않으며 기본 tab은 4칸으로 한다.

<br>

## 2. 문장의 종료
가급적 한 줄에 하나의 문장을 사용하며 너무 길어질 경우에는 줄 바꿈을 하여 가독성을 높인다.

<br>

## 3. 전역변수
가급적 전역변수의 사용을 지양한다.

<br>

## 4. 주석
해당 코드가 무엇을 하는지 간단하게 나타내며 왜 이런 코드를 작성했는지 이유가 드러나는 주석을 작성한다. 앞으로 할 일은 TODO. 문제가 있어서 다시 고쳐야 할 부분은 FIXME를 적극 활용한다.
~~~
// 뷰 홀더에 이벤트 발생시 데이터 바인딩 및 레이아웃 변화
final MyData item = items.get(position);
int itemViewType = getItemViewType(position);
        
switch (itemViewType) {
    case 0:
        // FIXME. 제대로 작동하지 않는 경우 있음
        changeItemViewOnclick(holder, item);
        break;
    case 1:
        // TODO. case 1일 때 함수 작성
        break;
        }
~~~
<br>

## 5. 명명 규칙
기본적으로 카멜 케이스를 사용한다.

### 5-1. 함수, 변수명
~~~
String customerName = "chacha";
~~~
~~~
private void getCustomerName(){
    ...
}
~~~

### 5-2. 클래스명
~~~
public class CustomerAdapter ...
~~~

### 5-3. static 상수는 스네이크 표기
~~~
public static final int SOME_CONSTANT = 42;
~~~

### 5-4. 약어를 단어 취급
~~~
// good <br>
XmlHttpRequest
class Html
String url

// bad <br>
XMLHTTPRequest
class HTML
String URL
~~~

### 5-5. 반복문 인덱스
i, j, k 를 사용하되 가급적 i, j 까지만 사용하도록 한다.

<br>

## 6. XML 명명 규칙
![example_image](https://jeroenmols.com/img/blog/resourcenaming/resourcenaming_cheatsheet.png)

### 6-1. Layout
- activity_main: content view of the MainActivity
- fragment_articledetail: view for the ArticleDetailFragment
- view_menu: layout inflated by custom view class MenuView
- item_article: list item in ArticleRecyclerView
- layout_actionbar_backbutton: layout for an actionbar with a backbutton (too simple to be a customview)

### 6-2. String
- articledetail_title: title of ArticleDetailFragment
- feedback_explanation: feedback explanation in FeedbackFragment
- feedback_namehint: hint of name field in FeedbackFragment
- all_done: generic “done” string

### 6-3. Drawables
- articledetail_placeholder: placeholder in ArticleDetailFragment
- all_infoicon: generic info icon
- all_infoicon_large: large version of generic info icon
- all_infoicon_24dp: 24dp version of generic info icon

### 6-4. IDs
- tablayout_main -> TabLayout in MainActivity
- imageview_menu_profile -> profile image in custom MenuView
- textview_articledetail_title -> title TextView in ArticleDetailFragment

### 6-5. Dimensions
- height_toolbar: height of all toolbars
- keyline_listtext: listitem text is aligned at this keyline
- textsize_medium: medium size of all text
- size_menu_icon: size of icons in menu
- height_menu_profileimage: height of profile image in menu
