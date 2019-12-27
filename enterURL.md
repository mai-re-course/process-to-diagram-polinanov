# Ввод URL
**Акторы:** пользователь, браузер(клиент), сервер.

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
![sequence](http://www.plantuml.com/plantuml/png/LP9HQoen48NVvrSCtfVrmVi3v7AHhOKMIf56dqEwEs1mJUpChCL_tud4whuUpldcp2GhqS0w7WS8dMR6dH33PnvJ7_Y2ivRpjoap388jKDAefZhYSnKTG8dWuZ-sItnEIknt7s_D70emdeCIjlXd7VZWmd3C2L8sALk-1BezTGU_VdUUgSlS-owOrCp_0W8OOb1a-Xf9b7eqBaP10s1Cg7l2gzkSY6rfu9POKERdYpL0_AtW411TRSaafvo4_ElcwkhfqKU3699I3t23shYeCIY9tpvjV9TJ8alaPF5xrEp_5kZk_4Pvf3bCyJUcs0JnBzljnjSDfx27EvK6SZsvFt7kI8IagI6x541TRCgi7QRpwqxboPROHpaDuI9b8QMaKsyBAyELd_43 "Диаграмма sequence")

# Диаграмма component 
![component](http://polinanov.mati.su/svg/компонентная.png "Диаграмма component")
