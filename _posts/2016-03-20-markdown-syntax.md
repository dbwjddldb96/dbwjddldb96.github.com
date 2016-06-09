---
layout: post
title:  "레시피 검색 프로그램"
date:   2016-03-15
excerpt: "내용내용 내용내용"
tag:
- markdown 
- syntax
- sample
- test
- jekyll
comments: true
---

# 레시피 검색 프로그램


## 프로그램 설명

사용자가 선택한 재료들을 바탕으로 만들 수 있는 요리법을 검색해서 보여주는 PC용 프로그램.  **This is strong**.

## 프로그램 세부 기능

![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}

위의 화면은 프로그램 시작화면이다. 왼쪽 파랑색 상자 안에는 프로그램의 사용방법이 적혀있다. 사용자가 음식 재료를 선택하고 검색버튼을 누르게 되면 거기에 해당하는 레시피가 등록된 웹사이트 주소들이 나온다. 음식재료는 빨간색 상자 안의 체크박스 또는 검색란을 이용하여 선택할 수 있다. 북마크 기능을 사용하여 

![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}

또한, 이 UI는 “F-Shaped Pattern” 기반으로 만들었다. F-shaped Pattern이란, HCI (Human- computer interaction) 분야에 기반한, 이론인데, 일반적인 사용자는 먼저 콘텐츠 영역의 상부에 걸쳐 수평 이동에서 판독하고, 이 초기 요소는 F의 상단 막대를 형성한다는 이론이다. 이 프로그램 또한, F-shaped pattern에 기반하여 콘텐츠 내용은 왼쪽에, 체크박스는 오른쪽에 배치했다.

![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}

 그리고 프로그램의 배경색, 제목색, 설명색이 조금씩 다르다. 이는 당연히 잘 보이게 하기
위함이지만, 사용자의 눈에 피로가 덜 가게 하기 위해, 그러한 색깔들 그리고 서로간의 보색작용을 일으키는 색깔들을 사용하였다. 이러한 색깔, 패턴을 바탕으로 한 UI 안에 세부기능들이 삽입되어 있다.

## 북마크 기능

![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}


 북마크 기능은 핵심적이다. 사용자가 마음에 드는 웹을 발견 했다면, 북마크 버튼을 눌러, 자신의 북마크 데이터 베이스에 삽입할 수 있다. 또한 데이터 베이스에 삽입할 때, 북마크 이름을 자신이 원하는 데로 적을 수 있다. (초기 북마크 이름은 북마크 주소와 동일하다)
 
 ![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}
 
 그렇게 하여 삽입한 후에, 북마크 보기를 누르면 자신이 넣은 웹 주소와 웹 주소를 찾을 때, 체크한 재료들 그리고 자신이 입력한 제목을 볼 수 있는 다이얼로그가 뜬다. 그리고 이 리스트박스는 체크하여 북마크 열기와 삭제가 가능하다. 북마크 스키마는 다음과 같다.
 
 
## 프로그램 동작 설명
 
 ![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}

처음에 검색 버튼을 클릭하면, NAVER OPEN API에 쿼리문을 날려 검색 결과를 요청한다.
그리고 본인 컴퓨터에 있는 MYSQL DATABASE에도 쿼리문을 날려, 유사 재료를 사용한 북마크 결과값이 있는 지 요청한다.
이렇게 요청한 값들을 모두 HTML 언어로 변환하여 사용자가 쉽게 알아볼 수 있도록 한다.
그리고 이 값을 통해 쉽게 navigate함수를 사용할 수 있도록, html파일로 저장한 후 (파일 입출력을 통하여) 저장된 파일을 인자 값으로 하여 navigate함수를 사용한다.

좀 더 자세한 설명을 하자면 OPEN API에 쿼리문을 만드는 방법은 다음과 같다.
 (설명을 돕기 위해 불가피하게 소스를 삽입하였습니다.)

 ![Smithsonian Image](https://mmistakes.github.io/minimal-mistakes/images/3953273590_704e3899d5_m.jpg)
{: .image-right}

위의 소스는 open api를 이용하기 위한 소스 인데, 원하는 음식재료를 query문에 합치는 방법이다. query에는 체크박스에서 누른 재료들이 추가된다. 또, linkPage는 체크한 재료가 없다면 아무 것도 뜨지 않도록 하기 위해 설정하였다. 또 MYSQL DATABASE에도 날릴 쿼리문 위에서 작성하였는데 그 변수는 m_sql_query이다.

**if (!mysql_real_connect(&mysql,MYSQL_HOST,MYSQL_USER,MYSQL_PWD,MYSQL_DB, MYSQL_PORT, 0, 0))
	{
		MessageBox(mysql_error(&mysql),MB_OK);
		return "";
	}
	else
		mysql_query(&mysql,"set names euckr"); //한글인식**
		
위와 같이 mysql에 접속한 후에, 


		
**CStringA sql;
MYSQL_ROW recordSet = NULL;	// mysql 의 행을 맡는다.
MYSQL_RES *sql_res; // mysql의 결과를 받아온다

        sql = CStringA(m_sql_query);

	// 쿼리 요청

	if(mysql_query(&mysql,sql)) {
		MessageBox("쿼리 에러",MB_OK);
		return "";
	}

	if((sql_res=mysql_store_result(&mysql))==NULL)
		return "";

	int index=0;
	while((recordSet=mysql_fetch_row(sql_res))!=NULL)
	{
		title_data = recordSet[0];

		temp = recordSet[1];
		result = result + "<tr bgcolor=""#FFFFB3""><td>"+ "<a href = \"" + temp + "\">" + title_data + "</a></td></tr>" ;

		temp = recordSet[2];
		result = result + "<tr bgcolor=""#C6E8FF""><td>" +"사용된 재료 : "+temp +"</td></tr>";
		index++;
	}

	result = result + "</table>";**
	
  받아온 변수를 sql에 String으로 저장한 다음에, mysql_query인자에 넣어, database에서 쿼리를 요청한다. 뒤에 소스들은, database에 유사 재료를 사용한 북마크 결과 값이 없으면 아무것도 출력하지 않고, 있으면 table(html형식으로)에 넣어 출력되게 한다. 
	
### Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.

## List Types

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3
{: rules="groups"}

## Code Snippets

{% highlight css %}
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
{% endhighlight %}

## Buttons

Make any link standout more when applying the `.btn` class.

{% highlight html %}
<a href="#" class="btn btn-success">Success Button</a>
{% endhighlight %}

<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn-success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn-warning">Warning Button</a></div>
<div markdown="0"><a href="#" class="btn btn-danger">Danger Button</a></div>
<div markdown="0"><a href="#" class="btn btn-info">Info Button</a></div>

## KBD

You can also use `<kbd>` tag for keyboard buttons.

{% highlight html %}
<kbd>W</kbd><kbd>A</kbd><kbd>S</kbd><kbd>D</kbd>
{% endhighlight %}

Press <kbd>W</kbd><kbd>A</kbd><kbd>S</kbd><kbd>D</kbd> to move your car. **Midtown Maddness!!**

## Notices

**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
{: .notice}
