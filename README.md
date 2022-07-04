# Client-Server

HTTP и HTTPS
   ```
   HTTP (hypertext transfer protocol) -
   протокол передачи данных, изначально предназначенный для гипертекстовых документов 
   (которые могут содержать гиперссылки, для перехода к другим документам).
  
   1) Протокол прикладного уровня, но иногда используется как транспортный протокол для других протоколов прикладного уровня 
   (SOAP,XML-RPC,WebDAV)
   2) Передача данных через TCP/IP-соединение, обычно через  TCP-порт 80
   
   HTTP запрос состоит из:
    -стартовой строки (версия протокола, URL, метод запроса)
    -заголовков (Host, пр. инф-я о браузере, языке, авторизации)
    -тела сообщения (пр. комментарий к видео)
    
    Запрос отправляет Useragent (любой инстумент или устройство, выступающее от лица пользователя. 
    Чаще всего браузер, моб. приложения, иногда программа типа Postman)
  
   HTTPS - http + secure
    
    1) Шифрование обеспечивают механизмы SSL и TLS
    
    SSL (secure sokets layer) работает так:
    когда мы подключаемся к сайту, просим у него SSL сертификат, браузер проверяет его, если все ок, 
    то начинается обмен шифрованными данными
   
    TLS (transport layer security) - прокачанная версия SSL. 
    По сути, последняя версия SSL - это TLS 1.0, но сейчас применяются версии TLS 1.2 и 1.3
    
    2) Передача данных обычно осуществляется по TCP-порт 443
   ```


МЕТОДЫ HTTP ЗАПРОСА
   ```
   GET (запрашивает содержимое конкретного ресурса, получает данные и никак не должен изменять эти данные)
   POST (создает новый ресурс из переданных данных в запросе)
   PUT (изменяет содержимое запроса по-указанному URI)
   DELETE (удаляет конкретный ресурс по-указанному URI)
   OPTIONS (определяет возможности и используемые методы веб-сервера)
   HEAD (похож на GET, но не возвращает тело ответа, а только стартовую строку и заголовки)
   PUTCH (похож на PUT, но применяется только к фрагменту ресурса)
   TRACE (возвращает служебную отладочную информацию о том, какие данные добавляют или изменяют прокси-серверы в запросе)
   CONNECT (запускает двустороннюю связь с запрошенным ресурсом. Метод обычно используется для открытия прозрачного TCP/IP-туннеля)
   ```
   
HTTP СТАТУС КОДЫ 
   ```
   100 (Continue) - "Продолжить". Этот промежуточный ответ указывает, что запрос успешно принят и клиент может продолжать присылать запросы либо проигнорировать этот      ответ, если запрос был завершён.
   200 (OK) - "Успешно". Запрос успешно обработан.
   201 (Created) - "Создано". Запрос успешно выполнен и в результате был создан ресурс. Этот код обычно присылается в ответ на запрос PUT "ПОМЕСТИТЬ".
   300 (Multiple Choice) - "Множественный выбор". Этот код ответа присылается, когда запрос имеет более чем один из возможных ответов. 
   301 (Moved Permanently) - "Перемещён на постоянной основе". 
   302 (Found) - "Найдено". Этот код ответа значит, что запрошенный ресурс временно изменён. 
   400 (Bad Request) - "Плохой запрос". Этот ответ означает, что сервер не понимает запрос из-за неверного синтаксиса. 
   401 (Unauthorized) - "Неавторизованно". Для получения запрашиваемого ответа нужна аутентификация. Статус похож на статус 403, но в этом случае, аутентификация возможна. 
   402 (Payment Required) - "Необходима оплата".
   403 (Forbidden) - "Запрещено". У клиента нет прав доступа к содержимому, поэтому сервер отказывается дать надлежащий ответ. 
   404 (Not found) - "Не найден". Сервер не может найти запрашиваемый ресурс.
   405 (Method Not Allowed) - "Метод не разрешён". Сервер знает о запрашиваемом методе, но он был деактивирован и не может быть использован.
   500 (Internal Server Error) - "Внутренняя ошибка сервера". Сервер столкнулся с ситуацией, которую он не знает как обработать. 
   501 (Not Implemented) - "Не выполнено". Метод запроса не поддерживается сервером и не может быть обработан.
   502 (Bad Gateway) - "Плохой шлюз". Эта ошибка означает что сервер, во время работы в качестве шлюза для получения ответа, нужного для обработки запроса, получил     недействительный (недопустимый) ответ. 
   503 (Service Unavailable) - "Сервис недоступен". Сервер не готов обрабатывать запрос. Зачастую причинами являются отключение сервера или то, что он перегружен. 
   504 (Gateway Timeout) - Этот ответ об ошибке предоставляется, когда сервер действует как шлюз и не может получить ответ вовремя.
   ```
ЧТО ТАКОЕ ЯДРО БРАУЗЕРА
   ```
   ЯДРО (ДВИЖОК) БРАУЗЕРА -  программа, преобразующая содержимое веб-страниц (файлы HTML, XML, цифровые изображения и т.д.)
   и информацию о форматировании (в форматах CSS, XSL и т. д.) в интерактивное изображение форматированного содержимого
   на экране. Браузерный движок обычно используется в веб-браузерах (отсюда название), почтовых клиентах и других программах,
   нуждающихся в отображении и редактировании содержимого веб-страниц.
 
   ```
