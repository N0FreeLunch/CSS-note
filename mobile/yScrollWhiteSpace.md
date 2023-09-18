## 모바일 스크롤

### 왼쪽 y축의 미세한 여백

- 스마트폰 디자인에서 y축 스크롤 부분에 미세하게 공간이 생기고 이를 불편하게 여길 때가 있다.

```
html,body {
  @media only screen and (max-width: 768px) {
    overflow-x: clip;
  }
}
```

- html 태그와 body 태그 모두에 `overflow-x: clip`을 넣어 주어야 한다. 두 곳 중 한 곳에만 속성을 주면 안 되고 두 곳 모두에 적용 해 주어야 한다.
- `overflow-x: hidden;`을 넣어도 왼쪽 스크롤 공간의 여백이 생기는 것을 제거할 수 있지만, 세로 스크롤이 툭툭 끊기는 문제가 발생하므로 `clip`을 사용해 준다.
- 현재 `clip` 속성 값은 [브라우저 호환성](https://developer.mozilla.org/ko/docs/Web/CSS/overflow#%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80_%ED%98%B8%ED%99%98%EC%84%B1)으로 모든 브라우저에서 지원하므로 사용해도 무방하다.
- 원리는 가로축의 스크롤을 차단하여 화면 사이즈 보다 바깥쪽 영역으로 갈 수 없게 하는데 원리가 있다.
