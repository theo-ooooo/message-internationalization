# 🌍 메세지, 국제화

## 메시지 파일 설정

- 기본 메시지 파일: `messages.properties`
- 언어별 메시지 파일:
  - `messages_ko.properties`
  - `messages_en.properties`

```properties
# messages.properties
hello=안녕하세요
required.item=상품 이름은 필수입니다.
```

---

## 타임리프에서 메시지 출력

```html
<p th:text="#{hello}">Hello</p>
```

---

## 자바 코드에서 메시지 사용

```java
@Autowired
MessageSource messageSource;

String message = messageSource.getMessage("hello", null, locale);
```

- `locale`은 `LocaleContextHolder.getLocale()`로 가져올 수 있음
