#google #osint


Все операторы поиска (2023): https://cargosecurity.gitbook.io/instrumenty-sb/operatory-poiska-google-yandex

"Thinking like a document"

[Online Course Explaining how Search Engines work](https://tryhackme.com/room/googledorking)
[So You Think You Can Google? - Workshop With Henk van Ess](https://www.youtube.com/watch?v=uyqXS5lL-mc)
[Power Searching with Google - edX course](https://www.edx.org/course/power-searching-with-google)

Использование разных операторов (например `filetype:pdf`)  может только увеличить поисковую выдачу. Чем точнее запрос - тем лучше работает поиск. Это особенно важно, учитывая что сообщения гугла типа "Найдено около 659,000,000 страниц" - это фейк и больше 300-400 посмотреть не получится.

В гугл картинках есть фильтр по цвету изображений и он очень сильно влияет на контекст выдачи. Пример: запрос `tesla coil` и `tesla coil` в чб цвете.

Очередность слов и кейс тоже очень важны.
##### Search hints:
- Кавычки: `"kali linux"`
- Оператор `intext:`, чтобы термин появился именно в том тексте, который вы видите на странице.
- Фильтр по времени через Tools/All filters
- Диапазон значений через троеточие: `best pizza "rating 4...5"`
- Для исключения нерелевантных результатов знак минус: `-site:vk.com`
- Оператор `OR`, `filetype:txt OR filetype:csv`
- Используйте `define` в поисковой строке для определения значения слов.
- `AROUND(n)` помогает искать слова рядом друг с другом. `n` - количество слов между искомыми словами. `AROUND(5)` будет выдавать результаты со словами на расстоянии 1,2,3,4 или 5 слов между ними.
- Поиск цитат в google books.
  
| Term | Action |
| -------- | -------- |
| site: | The specified phrase MUST appear on the specified site |
| filetype: | Search for a file by its extension (e.g. PDF) |
| cache: | View Google's Cached version of a specified URL |
| intitle: | The specified phrase MUST appear in the title of the page |


##### Examples:
`"document fraud" AROUND(7) France`
![[Pasted image 20230721234314.png]]
На конкретном сайте: `site:vk.com filetype:pdf`