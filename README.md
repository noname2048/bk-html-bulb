# bk-html-bulb

(Light Bulb On and Off Toggle Switch using Html CSS Only | No Javascript @Online Tutorials)[https://www.youtube.com/watch?v=cMRGyYLWbKc&t=3s] 의 클론 코딩

![결과물](Peek%202022-02-21%2005-13.gif)

원본결과물과는 차이가 있지만, 번쩍이는 부분은 그림자 효과를 겹친것이라 생략하였다.

중간에 checkbox를 아무리 클릭해도 check가 안되어서 많이 고생했었는데 원인은 다음과 같다.

```html
<!-- 동작하지 않는 코드 -->
<label for="">
    <input type="checked">
    <span></span>
</label>
<!-- 동작하는 코드 (바람직)-->
<label>
    <input type="checked">
    <span></span>
</label>
<!-- 동작하는 코드 -->
<label for="abcdefg">
    <input id="abcdefg" type="checked">
    <span></span>
</label>
```

label 안에 for가 붙는경우는 매칭되는 id가 있어야 한다. 또한, for을 쓰는 주된 목적은 input과 label을 연결시키기 위함인데, 이처럼 input을 label안에 적을때에는 생략하도록 한다.
