# Задача «Артемий слишком занят»

Перед выполнением задания внимательно прочитайте:

- [О всех этапах проверки задания](https://github.com/urfu-2017/guides/blob/master/workflow/overall.md)
- [Как отправить пулл](https://github.com/urfu-2017/guides/blob/master/workflow/pull.md)
- [Как пройти тесты](https://github.com/urfu-2017/guides/blob/master/workflow/test.md)
- Правила оформления [javascript](https://github.com/urfu-2017/guides/blob/master/codestyle/js.md), [HTML](https://github.com/urfu-2017/guides/blob/master/codestyle/html.md) и [CSS](https://github.com/urfu-2017/guides/blob/master/codestyle/css.md) кода

## Основное задание
Билли отправляется в путешествие и ему хочется составить список мест,
которые он желает посетить. Но память постоянно подводит Билли,
и он забывает, в каких местах ему уже довелось побывать. Чтобы путешествие Билли было
увлекательным, и он посетил запланированные достопримечательности, ему нужен сервис для сохранения и просмотра отметок о посещенных местах.

Билли прочитал хорошую книгу по фронтенду и сделает его сам,
а своего друга, опытного путешественника Артемия, попросил реализовать REST-интерфейс (API), используя Express.
Но Артемий укатил в очередную экспедицию, и просит помощи у вас.

### Билли просил
- Возможность добавления нового места (страны, города, достопримечательности) [ POST /spots { description: '' } ]
    - Место состоит из описания и отметки о посещении
    - Место создается непосещённым
- Возможность получения списка мест [ GET /spots?sort=lex|date&page=0&pageSize=50 ]
    - Можно сортировать по дате создания
    - Можно сортировать по алфавиту
    - Можно выводить список мест постранично
- Возможность поиска места по его описанию [ GET /spots/search?desc=desc ]
- Возможность редактирования описания конкретного места [ PATCH /spots/:id { visited: false, description: '' } ]
- Возможность отметить место посещённым или непосещённым [ PATCH /spots/:id { visited: false, description: '' } ]
- Возможность удаления места [ DELETE /spots/:id ]
- Возможность менять порядок мест в списке [ POST /spots/shuffle ]
- Возможность менять порядок мест в списке #2 [ POST /spots/:id/swap-with?id= ]
- Возможность очистки всего списка мест [ DELETE /spots/all ]

![artemii](https://user-images.githubusercontent.com/8963033/37154087-b5f1ed76-2300-11e8-81b7-0a8700bc5f57.png)
