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

## HTML Elements

Below is just about everything you'll need to style in the theme. Check the source code to see the many embedded elements within paragraphs.

# 레시피 검색 프로그램


### 프로그램 설명

사용자가 선택한 재료들을 바탕으로 만들 수 있는 요리법을 검색해서 보여주는 PC용 프로그램.  **This is strong**.

###프로그램 세부 기능

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

###북마크 기능

*This is emphasized*. Donec faucibus. Nunc iaculis suscipit dui. 53 = 125. Water is H2O. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. The New York Times (That’s a citation). Underline.Maecenas ornare tortor. Donec sed tellus eget sapien fringilla nonummy. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus.

HTML and CSS are our tools. Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus. Praesent mattis, massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam eget metus.

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
