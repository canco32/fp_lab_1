<p align="center"><b>МОНУ НТУУ КПІ ім. Ігоря Сікорського ФПМ СПіСКС</b></p>
<p align="center">
<b>Звіт з лабораторної роботи 1</b><br/>
"Обробка списків з використанням базових функцій"<br/>
дисципліни "Вступ до функціонального програмування"
</p>
<p align="right"><strong>Студент:</strong> <i>Сілін Ілля Денисович КВ-12</i><p>
<p align="right"><strong>Рік:</strong> <i>2024</i><p>

  ## Загальне завдання

  1. Створіть список з п'яти елементів, використовуючи функції LIST і CONS . Форма
створення списку має бути одна — використання SET чи SETQ (або інших
допоміжних форм) для збереження проміжних значень не допускається. Загальна
кількість елементів (включно з підсписками та їх елементами) не має перевищувати
10-12 шт. (дуже великий список робити не потрібно). Збережіть створений список у
якусь змінну з SET або SETQ . Список має містити (напряму або у підсписках):
   - хоча б один символ
   - хоча б одне число
   - хоча б один не пустий підсписок
   - хоча б один пустий підсписок
  ```
  (setq my-list (list 'a 42 (cons 'b '(c d)) '() 'e)) ; Результат: (A 42 (B C D) NIL E)
  
  ```
2. Отримайте голову списку
   
 ```
(car my-list) ; Результат: А
```
3. Отримайте хвіст списку  

```
(cdr my-list) ; Результат: (42 (B C D) NIL E)
```
4. Отримайте третій елемент списку.

```
(third my-list) ; Результат: (B C D)
```
5. Отримайте останній елемент списку.

```
(last my-list) ; Результат: (E)
```
6. Використайте предикати ATOM та LISTP на різних елементах списку (по 2-3 приклади для кожної функції).

```
(atom (car my-list)) ; Результат: T
(atom (cdr my-list)) ; Результат: NIL

(listp (car my-list)) ; Результат: NIL
(listp (third my-list)) ; Результат: T
```
7. Використайте на елементах списку 2-3 інших предикати з розглянутих у розділі 4 навчального посібника.

```
(numberp (second my-list)) ; Результат: T
(evenp (second my-list)) ; Результат: T
(equalp '(car my-list) '(third my-list)) ; Результат: NIL
```
8. Об'єднайте створений список з одним із його непустих підсписків. Для цьоговикористайте функцію APPEND.

```
setq append-list (append my-list (third my-list)) ; Результат: (A 42 (B C D) NIL E B C D)
```

## Варіант 4

<p align="center">
<img src="lab-1-variant.png">
</p>

```
(list
    1
    (list 'A 'NIL)
    (list 2 (list 'A 'NIL))
    (list 3 (list 'A 'NIL))
    (list 'C 'NIL))
```
Результат виконання роботи: 
```
(1 (A NIL) (2 (A NIL)) (3 (A NIL)) (C NIL))
```
