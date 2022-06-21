Настройка `CSS` 
---

**Подключение стилей страницы** в данном проекте раздельное. 

Это значит то, что для каждого шаблона `HTML` прописывается адрес к `css` индивидуально в своем шаблоне. Указывается слой `{layout:set}` и строка с адресом `<link rel="stylesheet" href="{site_url}template/file-name-css" type="text/css" />` и далее закрываем слой `{/layout:set}`.

```js
{layout="aprakos/_wrapper"}
// --------------------------------
{layout:set}
<link rel="stylesheet" href="{site_url}template/file-name-css" type="text/css" />
{/layout:set}
```

Далее в фантике-шаблоне `_wrapper.html` подключаем слой стилей данного шаблона так:

```js
<head>
	{layout:css}
</head>
```

Таким образом мы используем один фантик с `head` и `footer`, и подключаем в него остальные шаблоны с собственными `css`.