---
layout: post
title: "Three.js 공부하기"
date: "2015-01-01"
---

## links
- http://www.reddit.com/r/threejs/  
래딧의 threejs. 우측하단의 Useful resources들이 유용하다.  
![](http://kmyh.kr/markdown_images/Three.js_-_3D_JavaScript_Engine_2014-12-08_01-15-35.jpg)

- http://learningwebgl.com/blog/  
Native Webgl을 다루는 것으로 보인다. Lesson도 괜찮아보이고, WebGL around the net과 같은 글들이 계속 올라온다. 하지만 three.js보다 힘들겠지..  
![](http://kmyh.kr/markdown_images/Learning_WebGL_2014-12-08_01-14-50.jpg)

- [Three.js Examples](https://stemkoski.github.io/Three.js/)

- [Learning Three.js](http://learningthreejs.com/)  
webgl을 공부하는 사람 같이 보이는데 다양한 라이브러리들을 소개하기도 하고 자신의 공부도 올리는갯 같다.  잘 읽어봐야지.  
![](http://kmyh.kr/markdown_images/Blog_Archive_-_Learning_Three.js_2014-12-08_01-13-27.jpg)

- [THREEx Game Extensions for Three.js](http://www.threejsgames.com/extensions/)  
![img](http://monosnap.com/image/8Gks2kh9GeQmwKJq72J4dra4OGRac3.png)


- [Creative Code: CSS, JavaScript, WebGL and Three.js Experiments](http://www.awwwards.com/creative-code-css-javascript-webgl-and-three-js-experiments.html)  
![](http://kmyh.kr/markdown_images/Creative_Code_CSS_JavaScript_WebGL_and_Three.js_Experiments_2014-12-09_16-07-50.jpg)

- [Animating a Million Letters Using Three.js](http://www.html5rocks.com/en/tutorials/webgl/million_letters/)  
![](http://kmyh.kr/markdown_images/Animating_a_Million_Letters_Using_Three.js_-_HTML5_Rocks_2014-12-15_16-09-01.jpg)

- [WORKSHOP . CHROMEEXPERIMENTS](http://workshop.chromeexperiments.com/)  
![](http://kmyh.kr/markdown_images/Workshop__Chrome_Experiments_2014-12-16_17-22-11.jpg)

- [Chapter 4. 3D Graphics and Rendering in Three.js](http://chimera.labs.oreilly.com/books/1234000000802/ch04.html#the_scene_graph_and_transform_hierarchy)  
![](http://kmyh.kr/markdown_images/p3da_Figure_4-1.png)

- [Codeflow by Florian Boesch](http://codeflow.org/tags/webgl.html)  
![](http://kmyh.kr/markdown_images/Webgl_-_Codeflow_2014-12-31_03-04-07.jpg)


- [Smartjava.org](http://www.smartjava.org/)  
Three.js에 대해 책을 쓴 저자 Jos Dirksen의 블로그. 많은 예제들이 있다. 정보의 보고!  
![](http://kmyh.kr/markdown_images/Smartjava.org_2015-01-01_22-49-26.jpg)

- [NeHe Three.js tutorials](http://www.johannes-raida.de/tutorials.htm)  
![](http://kmyh.kr/markdown_images/NeHe_Three.js_tutorials_2015-01-03_20-35-32.jpg)

## Articles

### WebGL Renderer와 Canvas Renderer의 차이  
http://stackoverflow.com/questions/11949076/three-js-renderers  
요약하자면 3D로 무언가를 그리는 거의 모든 동작은 WebGL Renderer을 쓰는게 좋다. GPU를 쓰기 때문에, 하지만 정말 간단한 PNG나 GIF애니메이션을 만든다던가 아주 간단한 3D오브젝트(텍스쳐 없는 회전하는 큐브처럼)를 만든 때에는 Canvas Renderer가 더 효과적일 수도 있다.

### 2D Canvas Library의 승자는?  
웹에서 보면 3D-context의 승자는 Three.js가 확실해 보인다. 2D Canvas는 그에 비해 각축적전이 벌어지고 있는데 저마다 선호하는 라이브러리가 다르고, 실제로 너무 많은 라이브러리 들이 경합을 하고 있다.
- [html5 - Current State of Javascript Canvas Libraries? - Stack Overflow](http://stackoverflow.com/questions/8938969/current-state-of-javascript-canvas-libraries) 를 보면 라이브러리 제작자들까지 등장하여 더 좋은 라이브러리를 위한 뜨거운 토론이 벌어졌다.  

- [What is the current state of the art in HTML canvas JavaScript libraries and frameworks? - Stack Overflow](http://stackoverflow.com/questions/3474608/what-is-the-current-state-of-the-art-in-html-canvas-javascript-libraries-and-fra?rq=1)  
4년전에 시작한 논쟁이다.

- [Javascript 2D Canvas Libraries](https://docs.google.com/spreadsheet/ccc?key=0Aqj_mVmuz3Y8dHNhUVFDYlRaaXlyX0xYSTVnalV5ZlE#gid=0)에서 각 라이브러리들의 채점표를 확인할 수 있다.



### studying

- http://kmyh.kr/webgl/webgl_interactive_particles.html
- http://kmyh.kr/webgl/threejs_1.html
