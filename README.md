# Lottie

[Lottie](https://airbnb.design/lottie/)

Lottie는 Airbnb가 공개하고 있는 애니메이션을 표시하기 위한 라이브러리.

![](https://airbnb.design/wp-content/uploads/2017/01/babu.png)

Lottie 애니메이션은 Adobe의 "After Effects"로 "[Bodymovin](https://github.com/airbnb/lottie-web)"이라는 플러그인을 사용하여 JSON 파일을 렌더링.



### 메리트

- 구현 코스트가 낮다

Lottie을 사용하면 약간의 코드만으로 쉽게 애니메이션을 만들수 있음.

애니메이션 대부분을 디자이너 측에서 지내기 대문에 불필요한 수정 작업과 확인 작업을 줄일 수 있음.

- 여러 플랫폼에 대응

Web은 물론 IOS 및 Android 네이티브 앱에서도 애니메이션을 볼 수 있고 React등 인기 프레임 워크에서도 사용할 수 있음. 

한 번 만든 애니메이션은 다른 플랫폼에서도 돌려 사용할 수 있기 때문에 각각에서 유사한 사용자 경험을 제공하는 것이 가능.

하지만 플랫폼 별로 지원되지 않는 디자인 요소가 있어 확인한 뒤 사용해야한다.

[Lottie 지원 기능 목록](https://airbnb.io/lottie/#/supported-features)

[예시 파일들](https://codepen.io/collection/nVYWZR/)을 확인하면 알 수 있듯이 아직 그라디언트, 블러, 레이어 효과 같은 기능은 지원하지 않는다. 벡터 Shape의 변형과 움직임 위주일 때 효과적으로 사용할 수 있다. 

- 동영상 파일보다 압도적으로 경량



### **Web 에서 Lottie를 사용하는 방법**

#### 준비물

- lottie.js

- 애니메이션 파일(.json)



**lottie.js**

Lottie의 메인이되는 Javascript 파일.

[lottie Github](https://github.com/airbnb/lottie-web/tree/master/build/player)

[lottie CDN](https://cdnjs.com/libraries/bodymovin)



**애니메이션 파일(.json)**

애니메이션 파일은 After Effects에서 Bodymovin 플러그인 사용하여 JSON 형식으로 파일을 내보냄.

[LottieFiles](https://lottiefiles.com/) 라는 사이트에서 애니메이션 샘플을 다운로드 할 수 있음.



#### Web 사이트에 표시하는 방법

필요한 파일이 준비되면, 폴더 아래에 3개 파일 생성.

```html
|-- index.html
|-- main.js
|-- animation.json
```



**index.html**

```html
<head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bodymovin/5.5.9/lottie.min.js" type="text/javascript"></script>
</head>
```



```html
<body>
    <div id="lottie"></div>
    <script src="main.js" type="text/javascript"></script>
</body>
```



**main.js**

```javascript
lottie.loadAnimation({
    container:document.getElementById("lottie"),
    render:"svg",
    loop:true,
    autoplay:true,
    path:"animation.json"
});
```



<iframe height="265" style="width: 100%;" scrolling="no" title="Articulation Pieces by Al Boardman" src="https://codepen.io/airnan/embed/GOvebO?height=265&theme-id=light&default-tab=js,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/airnan/pen/GOvebO'>Articulation Pieces by Al Boardman</a> by kittons
  (<a href='https://codepen.io/airnan'>@airnan</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>



** 자세히 [Web - Lottie Docs](http://airbnb.io/lottie/#/web)

------

**참고**

https://feel5ny.github.io/2018/02/25/interaction_01/

[https://medium.com/@congjang/f-%EB%B2%88%EC%99%B8%ED%8E%B8-lottie%EB%A1%9C-animation-%EB%A7%8C%EB%93%A4%EA%B8%B0-93135f18e450](https://medium.com/@congjang/f-번외편-lottie로-animation-만들기-93135f18e450)

http://uidesignguides.com/airbnb-lottie/

https://tagilog.tistory.com/620