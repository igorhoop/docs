---
sort: 1
---



# A1

source: `{{ page.path }}`

# Элементы разметки Markdown - это заголовок (параграф?) с чертой снизу
Модель A1 производится в **двух** модификациях:
- Basic
- Explorer


###### Отличия модификаций (заголовок 6 решеток)

|   Параметр  | Basic    | Explorer  |
|------|:-------:|:--------:|
|   Максимальная скорость (м/с)   | 3.3 | 3.3 |
|   Максимальная грузоподъемность (кг) | 3 | 3 |
|   Максимальный угол подъема (°) | 30 | 30 |
|   Максимальная высота ступеней (мм) | 120 | 120 |
|   Бортовые компьютеры | Raspberry Pi 4 / Aaeon UP Developer Board | NVIDIA Jetson TX2 / Aaeon UP Developer Board |
|   Камера глубины | Intel RealSense D435 | Intel RealSense D435 |
|   Интерфейсы связи | Wi-Fi, Bluetooth, 2 x HDMI, 2 x Ethernet,2 x USB 3.0, 2 x USB 2.0, 2 отладочных порта
|   Датчик Lidar | **-** | **Установлен** |
|   Время работы | 1 час                  |




**жирный**
_итальянский текст_
~~зачеркнутый~~

А это [ссылка на гитхаб](http://github.com)



There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs.

There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs. There should be whitespace between paragraphs.

> Мы видим что основная разница между модификациями это различные модели бортовых компьютеров и наличие лидара.
>
> Из этого следует разное предназначение модификаций
>
>
> Basic для развлечения, Explorer для разработки и исследований
> ПРАВИЛО
> There should be no margin below this final sentence.
>
>

# Header 1

Это обычный параграф

## Header 2

> Так будет выглядеть блок цитирования

### Header 3

```
Так будет выглядеть код
```

#### Header 4


##### Header 5


###### Header 6

| What    | Follows  |
| ------- | -------- |
| A table | A header |
| A table | A header |
| A table | A header |

---

ПРАВИЛО???

---


Упорядоченный список

1. Michael Jackson
2. Michael Bolton
3. Michael Bublé

And an unordered task list:

- [x] Create a sample markdown document
- [x] Add task lists to it
- [ ] Take a vacation

And a "mixed" task list:

- [ ] Steal underpants
- ?
- [ ] Profit!

And a nested list:

- Jackson 5
  - Michael
  - Tito
  - Jackie
  - Marlon
  - Jermaine
- TMNT
  - Leonardo
  - Michelangelo
  - Donatello
  - Raphael

Definition lists can be used with HTML syntax. Definition terms are bold and italic.

<dl>
    <dt>Name</dt>
    <dd>Godzilla</dd>
    <dt>Born</dt>
    <dd>1952</dd>
    <dt>Birthplace</dt>
    <dd>Japan</dd>
    <dt>Color</dt>
    <dd>Green</dd>
</dl>

---

Tables should have bold headings and alternating shaded rows.

| Artist          | Album          | Year |
| --------------- | -------------- | ---- |
| Michael Jackson | Thriller       | 1982 |
| Prince          | Purple Rain    | 1984 |
| Beastie Boys    | License to Ill | 1986 |


жирная черта снизу (когда как)
---

asdf
---
---

Встраиваемый сниппет кода `var foo = "bar";` может быть встроен в строку

Also, `this should vertically align` ~~`with this`~~ ~~and this~~.

Code can also be shown in a block element.

```
var foo = "bar";
```

Code can also use syntax highlighting.

```javascript
var foo = "bar";
```

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```javascript
var foo =
  "The same thing is true for code with syntax highlighting. A single line of code should horizontally scroll if it is really long.";
```

Inline code inside table cells should still be distinguishable.

| Language   | Code               |
| ---------- | ------------------ |
| Javascript | `var foo = "bar";` |
| Ruby       | `foo = "bar"`      |

---

Small images should be shown at their actual size.

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

Large images should always scale down and fit in the content container.

![Branching](/assets/images/image-a1.png){: width="200px" style="text-align: center"}

```
This is the final element on the page and there should be no margin below this.
```
