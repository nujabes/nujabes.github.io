shader의 이해 - gl_FragCoord와 gl_FragColor의 이해
===============


gl_FragColor은 화면 전체의 색상 값을 가지고 있는 색상 표라고 볼 수 있다.
![img](http://monosnap.com/image/OH4gn5yoSrRzlPhCUs1QADSDEgQUql.png)

우리가 배우는 GLSL은 그래픽 카드에 직접 말하는 언어라고 볼 수 있는데, 그래픽 카드가 하는 일은 바로 우리가 보는 화면에 색을 칠하는 것이다. 그 화면이 애니메이션이 됬든, 그림판이 됬든, 동영상이든, 사진이든 모두 다 빨강, 파랑, 녹색 세가지 색을 이용해서 보여주는 것임을 이미 알고 있을 것이다. 위의 이미지는 그걸 아주 간단히 보여주는건데, 0은 검은색, 1은 흰색을 의미하는 것이다. 1로 칠해져 있기 때문에 모두 흰색이다. 그럼 다음은 어떨까.

![name](http://monosnap.com/image/LlSqrNMNzn7qQTDvMl7IJnK5v8TsVY.png)
이렇게 보일 것이다. 한 칸 하나하나를 픽셀이라고 볼 수 있는 것이다.  
흑백은 심심하니 여러가지 색을 써보고 싶다. 그럼 어떤 규칙을 가져야 할까. 모든 색은 RGB의 합성으로 나타낼 수 있으니 픽셀 하나당 세가지 값을 가지도록 해보자.

![n1](http://monosnap.com/image/evu4iC9jlsTeFVLBgJ3mVXXQJXfKeQ.png)

이렇게 표현될 것이다. 우리가 모든 디스플레이에서 보는 모든 것은 이런 과정을 거친다고 볼 수 있다. 글씨나 그림 영상 모두 마찬가지인 것이다. 자 그럼 다시 glsl로 돌아오자. 이 코드들은 무엇인가. 바로 어느 위치에 어떤 색을 칠하라 라는 내용들을 말해준다.

![n2](http://monosnap.com/image/DMVK2GbsjAZ0YWGVmq2So7fAaEofem.png)

화면을 이렇게 그리고 싶다면 어떻게 해야 할까? 그림판에서는 쉽다. 마우스로 화면의 반을 선택하고 검은색으로 칠하면 된다. glsl에서는 이런게 통하지 않는다. 프로그래밍을 통해 이야기를 해야 하는 것이다.

  화면의 가운데부터 왼쪽 끝까지는 색 1로, 오른쪽 끝까지 색을 0으로 칠해라

라는 명령을 전달해야 저런 모양이 되는 것이다. 이 내용을 glsl에서 표현하면 다음과 같다.

```glsl
	vec2 position = ( gl_FragCoord.xy / resolution.xy );
	float color = 1.0;
	if(position.x > 0.5) color = 0.0;
	gl_FragColor = vec4( color, color, color, 1 );
```
![n3](http://monosnap.com/image/u63FRiTix7BtYLxFrmYkcnoSo8iUC0.png)

이해가 가는가? 맨 마지막 줄 부터 보자.


gl_FragColor이 이해가 안갈 수 있는데, 이를 어떤 틀이라고 생각해보자. 계란판이라고 생각하면 쉽다.

![gl_fragcolor](http://monosnap.com/image/4X9mHjWww8AUigDDN68dLGsbImAWov.png)

```glsl
gl_FragColor = vec4( color, color, color, 1 );`
//계란판 = 무슨계란
```
이때 계란에는 4가지 성분으로 색상값이 들어간다. vec4는 4가지 요소를 묶어주는 방법이라고 할 수 있는데 각각 R, G, B, Alpha값이 들어간다.
color라는 변수에 어디에 어떤 색이 들어가는지를 결정해 주어야 하는데, 이를 바로 그 위해서 전달하게 된다. 현재 RGB에 같은 color가 들어가는 것을 알 수 있다.

```glsl
	vec2 position = ( gl_FragCoord.xy / resolution.xy );
	float color = 1.0;
	if(position.x > 0.5) color = 0.0;
	gl_FragColor = vec4( color, color, color, 1 );
```
2번째 줄에서 color
