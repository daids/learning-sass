# learning-sass

## 变量
  ```scss
  $primary-color: #272727;
  $font-weight: (
    "regular": 400,
    "medium": 600,
    "bold": 800
  );
  
  body {
    background: $primary-color;
    font-weight: map-get($font-weight, bold);
  }
  ```
  
## 嵌套
  ```scss
  .main {
    width: 80%;
    #{&}__paragraph {
     font-weight: map-get($font-weight, bold);
     &:hover {
      color: #666;
     }
    }
  ```
 
## 导入
  ```scss
  // file ./_resets.scss
  @import './resets';
  ```
## 函数
  ```scss
  @function weight($weight-name) {
    @return map-get($font-weights, $weight-name);
  }
  ```
## Mixin
  ```scss
  @mixin flexCenter($direction) {
    display: flex;
    flex-direction: $direction;
  }
  @mixin theme($light-theme: true) {
    @if $light-theme {
      color: #fff;
    }
  }
  .main {
    @include flexCenter(row);
  }
  .light {
    @include theme($light-theme: true);
  ```
## Extend
  ```scss
  .p1 {
  
  }
  .p2 {
    @extend .p1
  }
  ```
## Math
  ```scss
  p {
    width: 80% -40%;
  }
  ```
## More
 
