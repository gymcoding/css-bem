# HTML Class 이름 짓는 법 - BEM 명명 규칙

프로그래밍을 하다 보면 변수나 함수명을 어떻게 짓는지 정말 중요한데요. 이러한 이름을 지을 때 규칙이 없다면 지을 때마다 매번 고민을 해야 하고 많은 에너지를 소비할 수 있습니다. 그리고 이러한 불편함은 CSS 스타일을 위한클래스 이름 짓는 것에서도 느낄 수 있는데요 클래스 명을 지을 때 규칙이 없다면 우리는 역시 매번 고민을 해야하고 불필요한 에너지를 소비할거예요 하지만 올바른 규칙이 있다면 우리의 에너지를 알낄 수 있는 것 뿐만 아니라

- 코드의 가독성을 향상시켜 협업과 유지 보수를 용이하게 하고요
- 스타일의 충돌을 방지하여 예기치 않은 결과를 방지할 수 있습니다.
- 그리고 모듈화된 구조로 개발의 생산성을 높일 수 있어요.

그렇기 때문에 이번 시간에는 CSS 클래스 명명 규칙인 BEM에 대해 알아보도록 하겠습니다.

## BEM

CSS **BEM**은 "**B**lock, **E**lement, **M**odifier"의 약어로 웹 개발에서 CSS 클래스(Class) 이름을 지을 때 사용하는명명 규칙입니다. 이 규칙을 따르면 코드의 가독성과 유지보수성을 향상시킬 수 있습니다.

## 구성 요소

1. **Block (블록)**

   블록은 독립적으로 나타낼 수 있는 의미있는 개체로 웹 페이지 내에서 재사용될 수 있는 독립적인 단위로 구성됩니다.

   **예시**

   - `header`, `sidebar`, `article`, `button`

   블록 명에 공백이 포함되는 경우에는 공백을 대시로 대체하면 됩니다. 예: `my-header`, `my-button`

2. **Element (요소)**

   Element는 블록의 일부이며 독립적으로 의미는 없습니다. 모든 Element는 의미상 해당 블록에 종속되어 있고, 블록 내부에서만 의미가 있습니다.

   **예시**

   - `header` 블록 안에 있는 `header__logo`
   - `sidebar` 블록 안에 있는 `sidebar__title`
   - `article` 블록 안에 있는 `article__title`, `article__content`

   Element 명을 지을 때는 블록명과 두개의 밑줄 그리고 Element 이름으로 구성하시면 됩니다.

3. **Modifier (수정자)**:

   Modifier는 블록이나 요소의 상태나 모양을 변경하는 데 사용합니다. Modifier는 선택적으로 사용되며 필요한 경우에만 추가됩니다.

   **예시**

   - `button`의 상태를 나타낼 때는 `button—-primary`, `button-—disabled`
   - `button`의 모양을 나타낼 때는 `button--rounded`, `button--large`

   Modifier 명은 블록이나 요소의 이름과 두 개의 대시 그리고 Modifier명으로 구성됩니다.

### 사용 예시

```html
<!-- HTML -->
<nav class="navigation">
  <ul class="navigation__list">
    <li class="navigation__item">
      <a href="#" class="navigation__link">Home</a>
    </li>
    <li class="navigation__item">
      <a href="#" class="navigation__link">About</a>
    </li>
    <li class="navigation__item">
      <a href="#" class="navigation__link navigation__link--active">Services</a>
    </li>
    <li class="navigation__item">
      <a href="#" class="navigation__link">Contact</a>
    </li>
  </ul>
</nav>
```

```css
/* CSS */
.navigation {
  display: flex;
  justify-content: space-between;
}

.navigation__list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.navigation__item {
  margin-right: 10px;
}

.navigation__link {
  text-decoration: none;
  color: #333;
}

.navigation__link--active {
  font-weight: bold;
  color: #ff0000;
}
```

## 유튜브 영상

https://youtu.be/V8iLl2NyxgM

## 짐코딩 클럽 - 가장 쉬운 웹 개발 입문

https://gymcoding.co
