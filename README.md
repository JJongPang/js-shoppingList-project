# 쇼핑 목록앱 만들기

## 구현할 기능 목록
+ +버튼 클릭시 쇼핑 리스트 추가
+ 'Enter' key-press event 발생시 쇼핑 리스트 추가
+ 삭제 버튼 클릭시 쇼핑 리스트 삭제

## 결과물
![shoppinglist](https://user-images.githubusercontent.com/68219486/91831287-d9a93180-ec7e-11ea-9665-6f2a7784dbd2.JPG)
![shoppingDelete](https://user-images.githubusercontent.com/68219486/91831291-db72f500-ec7e-11ea-87f7-355d48cf9c99.JPG)

#### Project URL: https://jjongpang.github.io/js-shoppingList-project/

## Note
#### 이벤트 위임
```html
//예제 코드
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      .selected {
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <ul>
      <li>1</li>
      <li>2</li>
      <li>3</li>
      <li>4</li>
      <li>5</li>
      <li>6</li>
      <li>7</li>
      <li>8</li>
      <li>9</li>
      <li>10</li>
    </ul>
    <script>
      // Bad
      // const lis = document.querySelectorAll('li');
      // lis.forEach(li => {
      //   li.addEventListener('click', () => {
      //     li.classList.add('selected');
      //   });
      // });

      // Coooooooool 🙌
      const ul = document.querySelector('ul');
      ul.addEventListener('click', event => {
        if (event.target.tagName == 'LI') {
          event.target.classList.add('selected');
        }
      });
    </script>
  </body>
</html>
```
