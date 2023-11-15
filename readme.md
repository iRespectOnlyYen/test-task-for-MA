# Тестовое задание для MillionAgents

### Задание:

Hard. Написать парсер для сайта Метро (https://online.metro-cc.ru/)

### Ход работы:

<p>
    Сначала решил асинхронно скачать страницы через aiohttp и запарсить через bs4 (можете глянуть папку draft), 
    но как оказалось, на скачанных страницах нет информации о цене(
</p>
<p>
    Селениум использовать очень не хотелось, 
    будет работать не так быстро + потреблять больше ресурсов 
<p>
    Полез во вкладку нетворк, в инструментах разработчика, 
    что бы глянуть как мы получаем данные о ценах, и встретил graphql. До этого с ним не работал, но общее представление имею.
    Быстренько накидал запрос, который тянет всю нужную информацию, а уже после - пару условий в питоне. 
    В итоге получился простой и быстрый скрипт.
</p>

![image](https://github.com/iRespectOnlyYen/test-task-for-MA/assets/90966720/7df8b497-9ca7-4d3b-8b1c-fa98721f3fd2)



### Запуск:

Установите зависимости из файла requirement.txt при помощи `pip install -r requirements.txt` или воспользуйтесь
poetry) <br>
После чего необходимо запустить файл `main_graphql.py`. В директории появится или обновится файл output.xlsx с
результатами парсинга.

**p.s.** запарсил раздел "Конфеты и подарочные наборы", результат можете глянуть в файле output.xlsx

![image](https://github.com/iRespectOnlyYen/test-task-for-MA/assets/90966720/cf902214-94c2-49cd-8981-32c7c6928066)


