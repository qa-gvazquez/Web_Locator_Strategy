# Robust Web Locator Strategy

A robust web automation locator strategy prioritizes stability, maintainability, and speed by favoring unique, immutable attributes over brittle DOM structures.

The best approach is to use dedicated test attributes (e.g., data-testid) or unique IDs, followed by CSS Selectors, and finally XPath.

This **minimizes** test failures (**flakiness**) during UI changes.

## 1. LECTURES

<details>
<summary> Full Course content </summary>

<details>
<summary> Sección 1: Introduction to the Course (2) </summary>

- [x] 1. Stop Fighting Locators: Course Overview (4m)
- [x] 2. How to Learn Locators Effectively (4m)

</details>

<details>
<summary> Sección 2: Locators in Test Automation (2) </summary>

- [x] 3. Introduction to Section – Locators in Test Automation (1)
- [x] 4. What Are Locators and Why They Matter (3)
- Why good locator matter?
  - Locators are the **link** between test code and webpage.
  - Must be unique and stable.
  - Weak locators break easily
  - Reliable locators make test consistent.
  - Goog locators make test reliable.
  - Bad locators make **flaky test**.
- [x] 5. Types of Locators in Test Automation.
- Commmon locator types in Automation Tools
  1. ID
  2. Name
  3. Class
  4. Tag
  5. Link Text
  6. Partial Link Test
  7. XPath
  8. CSS
  9. JavaScript Executor

  ```html
  <input type="text" name="username" id="username">  
  ```

- Wheb basic locators fail.
  - Dynamic or missing ID.
  - Non-unique class name.
  - Hidden or nested elements.
  - Changing atributes.

- [x] 6. Why We Use XPath and CSS Locators.
- Universal and framework-indepedent.
- Can locate elements with flexible patterns.
- Handle complex and dynamic DOM's.
  - XPath

  ```css
  //input[@name='username']
  ```

  - CSS

  ```css
  input[name='username']
  ```

  ```html
  <button id="submit" class="btn" style="">Submit</button>
  ```

  - XPath Text (without '@')

  ```css
  //button[text()='Submit']
  ```

  - CSS

  ```css
  button#submit.btn
  ```

- When to use each
  - Use XPath for text and relative elements location.
  - Use CSS for simplicity and performance
  - Mix both when needed in real frameworks

- [x] 7. Testing Locators in Chrome DevTools.

> SUT = https://practicetestautomation.com/practice-test-login/

- Usando el atajo de teclado:
  - Command + Shift + C = Quick select element and open inspector on DevTools.
- Podemos abrir rápidamente la consola y dar clic derecho sobre el elemento en el DOM para encontrar un localizador preliminar.
  - Xpath = Copy Xpath
  - CSS = Copy Selector
- Dentro del inspector de elementos, si vamos a la CONSOLA podemos validar estos localizadores

  - XPath = $x('LOCALIZADOR')

  ```css
    $x('//*[@id="username"]')
  ```

  - CSS = $$('LOCALIZADOR')

  ```css
    $$('#username')
  ```

- Finalmente, damos ENTER y desde la consola de los DevTools, podemos hacer todo.

</details>

</details>

## Append - Usefull Links

<details>
<summary> 1 - Course </summary>


1. Udemy Course at [XPath and CSS Locators for Test Automation](https://www.udemy.com/course/xpath-locators-for-selenium/)

</details>

<details>
<summary>  2 - Practice Pages for Automation </summary>


1.  [practicetestautomation.com](https://practicetestautomation.com/practice/) by Dmitry Shyshkin.

</details>

<details>
<summary> 3 -  Keyboard hacks </summary>

1. On MAC OS
   1. Command + Shift + C = Quick select element and open inspector on DevTools.
   2. Control + F = Open search bar in DevTools to validate our selectors.
   3. Option + Shift + UP = Copy code Line
   4. Option + UP/DOWN = Move code Line
   5. Control + Number = Switch to tab in Chrome Browser.

</details>
