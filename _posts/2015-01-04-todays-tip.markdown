---
layout: post
title: "todays tip"
date: "2015-01-04"
---
요즘 유용하게 쓰고 있는 것들이나 방법들을 정리해본다.

***

원하는 자바스크립트 라이브러리 찾기
---
<http://javascripting.com>  
CDN링크도 쉽게 찾을 수 있다.
***
원하는 웹서비스 찾기
---
<http://producthunt.com>  
하루에도 수십개의 새로운 웹서비스가 소개되는 곳이다. 키워드만 넣으면 관련 웹서비스의 목록이 뜬다.  
스코어를 확인하면 더 쉽게 찾을 수 있다.

for example)
컬러 팔레트를 찾기 위해 color을 입력해서 <http://color.hailpixel.com>을 찾았다.

***

맘에드는 Sublime Text 테마 SPACE GRAY
---
<https://github.com/kkga/spacegray>
![](https://github.com/kkga/spacegray/raw/master/Screenshots/spacegray.png)

***

Adobe Source Code Pro
---
[Release Fonts version 1.017 (OTF, TTF, WOFF, EOT, SVG) · adobe-fonts/source-code-pro](https://github.com/adobe-fonts/source-code-pro/releases/tag/1.017R)

Space Gray에서 사용한 폰트를 알려줘서 가봤더니 어도비가 개발한 오픈소스 폰트다. 예전에 쓰던 inconsolata도 나쁘지 않았는데 맘에들어 계속 쓰기로 했다.

***

Sublime Text Icon
---
[Dribbble - Sublime Text.app icon by Russ](https://dribbble.com/shots/1503805-Sublime-Text-app-icon?list=searches&tag=sublime_text&offset=19)  
![](https://d13yacurqjgara.cloudfront.net/users/491092/screenshots/1503805/st.jpeg)  
Sublime Text 3의 아이콘이 마음에 안들어 새로 바꾼 아이콘

***

[iWantHue](http://tools.medialab.sciences-po.fr/iwanthue/index.php)
---
Javascript코드에서 수십, 수백개의 색의 팔레트를 가져다 쓰고 싶은데, 랜덤하게 생성하기엔 너무 안어울릴게 걱정되었는데, 딱 맞는 웹서비스를 찾았다. IwantHue는 컬러팔레트를 선택하거나 자신이 직접 색의 범위를 성정해서 원하는 만큼의 색상을 추출해 낼 수 있는데, Make Palette를 누르면 json이나 css로 출력을 해주고, HEX는 물론 RGB, HCL까지 지원한다. 심지어 이 색상을 실시간으로 제너레이트 할 수 있는 소스코드까지 있네. 너무너무 마음에 드는 서비스.

***

D3 vs SIGMA.js
---
그래프 라이브러리로 sigma.js라는 것을 발견했는데 괜찮아보여서 혹시 d3보다 좋은가 하고 검색해보았다.  
[What is best for graph rendering: sigma.js or d3.js? Why? - Quora](http://www.quora.com/What-is-best-for-graph-rendering-sigma-js-or-d3-js-Why)  
말하자면 데이타 비주얼라이제이션은 d3가 낫지만 그래프를 그리는 것에서는 sigma.js가 월등이 낫다는 것. sigma.js는 게다가 webgl도 지원한다고 한다.

***

Javascript에서 vector연산하기
---
[glMatrix](http://glmatrix.net/)라는 것을 찾았다.  

```this.location = vec2.fromValues(x, y);```  

이런식으로 쓸 수 있다.
