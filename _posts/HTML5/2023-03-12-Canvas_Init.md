---
title: Canvas 시작하기
author: LazyLonghorn
date: 2023-03-12 11:33:00 +0800
categories: [HTML5, Canvas]
tags: [HTML5, Canvas]
math: true
mermaid: true
image:
  path: ../commons/devices-mockup.png
  # lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  # alt: Responsive rendering of Chirpy theme on multiple devices.
---

## Canvas 란?
w3schools 에 정의된 내용은 아래와 같다. <br/>
( 출처 : <a href='https://www.w3schools.com/tags/tag_canvas.asp'>https://www.w3schools.com</a> )


> Canvas 는 스크립팅(일반적으로 JavaScript)을 통해 즉석에서 그래픽을 그리는 데 사용됩니다.<br/>
> Canvas 는 투명하고 그래픽의 컨테이너일 뿐이므로 실제로 그래픽을 그리려면 스크립트를 사용해야 합니다.<br/>
> Canvas 요소 내부에 존재하는 텍스트는 해당 브라우저가 Canvas 요소를 지원하지 않을 경우 브라우저 화면에 대신 나타나게 됩니다.

---

## Canvas Tag 기본 사용
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canvas Start</title>
    <style>
        .canvas {
            width: 500px;
            height: 500px;
            background-color: #333;
        }
    </style>
</head>
<body>
    <canvas id="canvas"class="canvas"></canvas>
    
    <script>
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');

        canvas.width = 400;
        canvas.height = 400;
    </script>
</body>
</html>
```

<h3 data-toc-skip>■ HTMLCanvasElement.getContext()</h3>
캔버스의 드로잉 컨텍스트를 반환합니다.<br/>
파라미터로 넣은 "2d" 는 2차원 렌더링 컨텍스트를 나타내는 CanvasRenderingContext2D (en-US) 객체를 생성하게 합니다.

( 출처 : <a href='https://developer.mozilla.org/ko/docs/Web/API/HTMLCanvasElement/getContext'>https://developer.mozilla.org/ko/docs/Web/API/HTMLCanvasElement/getContext</a> )

---

## Canvas width & height

> 캔버스의 표시 크기는 CSS로도 수정할 수 있습니다.<br/>
> 그러나, CSS를 사용할 경우 렌더링 과정에서 CSS 크기에 맞추기 위해 이미지의 크기를 조절하므로, 최종 그래픽이 변형될 수 있습니다.

위와 같은 이유로 `<canvas>` 는 Javascript 나 HTML 로 직접 변경해주는 변경해주는 것이 좋다.

[출처]<br/> 
<a href='https://developer.mozilla.org/ko/docs/Web/HTML/Element/canvas'>https://developer.mozilla.org/ko/docs/Web/HTML/Element/canvas</a>
<a href='https://developer.mozilla.org/ko/docs/Web/API/Canvas_API/Tutorial/Basic_usage'>https://developer.mozilla.org/ko/docs/Web/API/Canvas_API/Tutorial/Basic_usage</a>
<a href='https://velog.io/@yojeongjin'>https://velog.io/@yojeongjin</a>

---

## Drawing
```javascript
ctx.fillStyle="red";
ctx.fillRect(0,0,300,300);
```
![AA](/posts/20190808/mockup.png){: width="972" height="589" }
![AA](/posts/20230312/a.png){: width="972" height="589" }
_Full screen width and center alignment_
![AA](/../../images/a.png){: width="400" }
