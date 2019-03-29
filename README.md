# RubyRush
Open source курс по основам настоящего программирования для всех и каждого. Основной язык — Ruby. Здесь хранятся все уроки и задания курса. 

🎓  
Лично Вы, дорогой читатель можете внести свой вклад в этот курс (об этом ниже).

## Как устроено

На данный момент из содержимого этой репы middleman-ом генерится статический сайт на https://rubyrush.ru со временем переедем 
на свой движок, сохранив общую структуру и место хранения курса.

В папке `steps/` лежит линейный список «шагов».

Каждый шаг это урок с вложенными в него видосами и/или текстом, или ДЗ, 
или какой угодно mardkdown+html материал. 

Последовательность шагов на сайте в конечном итоге определяем мы, деплоеры курса (@aristofun, @installero).

### Структура папок

`steps/<step_slug>/` — уникальное имя (идентификатор) шага. 

Шаги-ДЗ принято привязывать к соотв. уроку и нумеровать. 

Например после урока `steps/classes-inheritance` есть 2 ДЗ: `steps/classes-inheritance-01` и `steps/classes-inheritance-02`.


| Файл | Его смысл |
|----------------------|-----------------------------|
| `/<step_slug>/content.md` | основное тело шага |
| `/<step_slug>/links.json` | ссылки и материалы к шагу |
| `/<step_slug>/files/*` | файлы для материалов к уроку |
| `/<step_slug>/solution/*` | код с ответом на ДЗ |


### links.json

Отрывок из `steps/argv-test/links.json` — шаг-урок [про аргументы командной строки](https://github.com/aristofun/rubyrush/tree/master/steps/argv-test)

```json
{
  "help": [
    {
      "title": "Тест на логическое мышление",
      "url": "http://syntone.ru/psytesty/test-logicheskogo-myshleniya/"
    },
    {
      "title": "Тонкости работы с командной строкой Windows",
      "url": "http://habrahabr.ru/post/218759/"
    }
  ],
  "materials": [
    {
      "title": "Работа с аргументами запуска",
      "url": "arguments.rb"
    },
    {
      "title": "Тест на ревнивость",
      "url": "jealous_test.rb"
    }
  ]
}
```

**"help"** — абсолютные ссылки на актуальные материалы к теме урока (мануалы, полезные статьи, читшиты...)

**"materials"** — имена файлов относительно вложенной в этот же шаг папки `steps/argv-test/files/`. Ссылка сгенерится напрямую на репозиторий с этим файлом.

Этот файл внутри любого шага (ДЗ, урок) актуален и используется, если есть.

### content.md

Содержит хорошо структурированный текст шага (урок или ДЗ). Может содержать вложенные по определенному формату видео и спец. блоки с ДЗ/подсказкой.

Просто сравните внимательно:

https://github.com/aristofun/rubyrush/edit/master/steps/argv-test/content.md

и

https://github.com/aristofun/rubyrush/blob/master/steps/argv-test-01/content.md (шаг-ДЗ)

### Решения ДЗ

Решения ДЗ, код, файлы и пр. надо складывать в подпапку соотв. шага ([пример №1](https://github.com/aristofun/rubyrush/tree/master/steps/errors-exceptions-03/solution), [пример №2](https://github.com/aristofun/rubyrush/tree/master/steps/gets-butovo-03/solution)).

В виде подпапки с набором файлов проекта, а не архивом.

## Как вносить вклад

🎁

### Исправления
1. Увидели на сайте https://rubyrush.ru какой-то косяк или слабое место
2. Нашли по слагу соотв. папку тут
3. Сделали пулл-реквест с улучшениями
4. PROFIT! 

### Новые уроки
1. Увидели что какая-то тема рассказана плохо или не рассказана вообще
2. Или вспомнили интересную задачку для начинающих
3. Свяжитесь с [@aristofun](tg://resolve?domain=aristofun), [@installero](tg://resolve?domain=installero) чтобы согласовать тему
4. Пулл-реквест
5. PROFIT!!

### PROFIT

1. Cсылки на самых активных контрибьюторов разместим тут, на самом сайте и вообще при любом случае поддержим и упомянем. 
2. К карме +150 каждый пулл-реквест

Время разбрасывать камни и умножать добро 🎈

И через это еще больше прокачиваться. Кто на себе хоть раз проверял, знают о чем я.


# License & copyright

Воровать и использовать без нашего ведома никакие материалы нельзя, навсегда испортите карму. Все вопросы решим, пишите.
