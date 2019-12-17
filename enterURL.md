# Ввод URL
**Акторы:** пользователь, браузер, сервер.

**Цель:** пользователь хочет увидеть содержимое веб-страницы по URL.

**Предусловия:** у пользователя открыт браузер.

**Сценарий:**
1. Пользватель вводит google.com в адресную строку своего браузера.
2. Браузер проверяет кэш DNS-записи, чтобы найти соответствующий IP-адрес google.com.  

{[Запрос DNS](#Запрос_DNS)}  

3. Браузер инициирует TCP-соединение с сервером.
4. Браузер отправляет HTTP-запрос на веб-сервер.
5. Сервер обрабатывает запрос и отправляет ответ.
6. Сервер отправляет ответ HTTP.
7. Браузер отображает HTML-контент (для HTML-ответов, который является наиболее распространенным).  

**Результат:**
* Пользователь успешно перешел по URL и увидел содержимое веб-страницы.

**Исключения:**
1. Отсутствует интернет-соединение.
2. Неверно введен URL.

**Альтернативный сценарий:**  
2а. <a name="Запрос_DNS"></a> *Запрос DNS.*  
2а1. Если запрошенный URL отсутствует в кэше, DNS-сервер интернет-провайдера инициирует запрос DNS, чтобы найти IP-адрес сервера, на котором размещен maps.google.com.  
Возврат на шаг 3.


# Диаграмма activity
![activity](http://polinanov.mati.su/svg/ativitydz2.png "Диаграмма activity")

# Диаграмма sequence
![sequence]
(http://www.plantuml.com/plantuml/png/ZP4nRy8m48Lt_ueJB7Je7s2eK4gb3bM5QfWjrpw4HR3ftOMAVzypIY5X8bkUxttl_BnWyIJTeJK-I27OC9B1B4dEC6ce_Eh_13n3OxvBbwCdrItIgPUjCTK2po_GpE4j2vBRV7tCdYeldRoWEatJduSTXhrRVbf760f55xnAes6OBZtjhMyF9Pk8Gufl1GX_EcJ129e2YI4NWPH1TWWN61Y0IvoTWmQ1ZjDPjIl8Wi6MTGvpDEP_L1b9afwpMx-kN2WvepfAhilThDEWttPh8Wx46uKnHtRlw_NAzOi-P3Vswg_5kYELWCp8ivxoEAIvMuAF9VDTmyEAOTpnaDbVgpxl76BYO-lFN9iHpFLU8-D2Gxj3-mS0 "Диаграмма sequence")
