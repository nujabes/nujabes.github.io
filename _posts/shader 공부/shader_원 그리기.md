Shader의 이해 - 원 그리기
===============

원 그리기
----------------

- [Glsl Sandbox](http://glslsandbox.com)

Glsl Sandbox에 접속해서 **Create new effect!** 버튼을 눌러 다음의 코드를 넣자.

마우스의 움직임에 따라 패턴이 달라지는 기본 코드인데, 지금 이해하기에는 어려움이 있으니 아래의 코드를 복사해 넣자.
다음의 기본적인 코드를 복사해 붙여넣자.

```glsl
#ifdef GL_ES
precision mediump float;
#endif

uniform float time;
uniform vec2 resolution;

void main( void ) {
	vec2 position = ( gl_FragCoord.xy / resolution.xy );
	position = 2.0 * position - 1.0;
	position.x *= resolution.x / resolution.y;

	float color = 0.0;
	float d = length(position);
	d = distance(position, vec2(0,0));
	color = d;
	gl_FragColor = vec4( color, color, color, 1 );
}
```
![image](http://kmyh.kr/markdown_images/BynJ0fOJLf.png)

이런 화면이 나올 것이다. 한줄씩 침착하게 나아가자. 한줄씩 지워가며 속성을 이해해 볼건데, 실제로 지워버리면 나중에 다시 써야하니 주석으로 막으면서 해보도록 하겠다.

10번째 줄과 11번째 줄의 앞에 '//'를 넣어보자
```glsl
//position = 2.0 * position - 1.0;
//position.x *= resolution.x / resolution.y;
```
해당 줄을 주석으로 바꾼 것이다. 다시 '//'를 제거하면 다시 원래대로 동작하니 모르는 코드가 있을 때 하나하나 스위치를 꺼고 켜듯이 주석처리를 해서 이해해 볼 수 있다.
