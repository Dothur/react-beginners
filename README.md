# Nomad -  ReactJS 영화 웹 서비스

## 2023 03 06 Start

- ReactJS 설치를 위한 JavaScript URL Code
    
    ```jsx
    <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    ```
    
    최신 버전은 React 공식 홈페이지 참조
    
- #1.2  2023. 03. 06
    1. React JS :  어플리케이션이 인터랙티브하도록 만들어주는 library (=엔진)
    2. ReactDOM : Library or Package. 모든 React Element 들을 html body 에 둘 수 있게 해줌
    
    ```jsx
    ReactDOM.render(span, root);
    ```
    
    1. .render( a, b) : a 가 b 로 갈 수 있도록 함
    2. Vanilla JS 는 html → JS 순서 
    3. 리액트는 JS → html 순서
- #1.3  2023. 03. 06
    
    ![스크린샷 2023-03-06 오후 9.48.05.png](Nomad%20-%20ReactJS%20%E1%84%8B%E1%85%A7%E1%86%BC%E1%84%92%E1%85%AA%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%B5%E1%84%89%E1%85%B3%20a4bf1fe7952045f59012e64bc6383772/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-06_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_9.48.05.png)
    
    ```jsx
    const root = document.getElementById("root");
    const h3 = React.createElement(
          "h3",
          { onMouseEnter: () => console.log("mouse enter") },
          "Hello i'm span"
    );
    const btn = React.createElement(
          "button",
          { onClick: () => console.log("im clicked") },
          "Click me"
    );
    const container = React.createElement("div", null, [h3, btn]);
    ReactDOM.render(container, root);
    ```
    
    1. 두 가지 이상을 render 하고 싶은경우엔 **div 를 createElement** 해주고 위와 같이 배열을 만들어준다.
    2. js 에서 eventListener를 하나하나 만들었지만 **React에선 바로바로 property 로 적용**해 줄 수 있다. 
    3. 위와 같이 onClick 등등 on + @ 식으로 추가해주면되고 내가 겪었던 문제중 하나는 onclick 으로 자동완성이 되어서 자연스럽게 그렇게했지만 eventListener 가 작동하지않아서 onClick 으로 대문자를 고쳤더니 해결되었다.
        
        ~~🤣 대문자 구분 잘하기!~~
        
    - 강의를 보던중 텍스트 자동 포맷팅이 되는게 깔끔해보여서 나도 적용해보았다. ⬇️⬇️
        
        ![스크린샷 2023-03-06 오후 10.00.40.png](Nomad%20-%20ReactJS%20%E1%84%8B%E1%85%A7%E1%86%BC%E1%84%92%E1%85%AA%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%B5%E1%84%89%E1%85%B3%20a4bf1fe7952045f59012e64bc6383772/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-06_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_10.00.40.png)
        
        1. Prettier - Code formatter 이라는 Extension 설치 후 cmd + , 으로 설정에 들어간다.
        2. Search settings 에 Editor: default Formatter 를 검색 후 Prettier - Code formatter 로 설정한다.
            
            ![스크린샷 2023-03-06 오후 10.06.05.png](Nomad%20-%20ReactJS%20%E1%84%8B%E1%85%A7%E1%86%BC%E1%84%92%E1%85%AA%20%E1%84%8B%E1%85%B0%E1%86%B8%20%E1%84%89%E1%85%A5%E1%84%87%E1%85%B5%E1%84%89%E1%85%B3%20a4bf1fe7952045f59012e64bc6383772/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-03-06_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_10.06.05.png)
            
        3. 그리고 우측 위에 settings.json 에 들어가서 아래와 같이 설정한다.
            
            `"editor.formatOnSave": true`
            
        4. 그러면 cmd + s 로 저장 할 때 자동으로 코드가 정리된다!
