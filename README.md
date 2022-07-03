# lesson_9_server_log
Анализ лога веб сервера

1) Скрипт принимает в себя 2 аргумета. Первый это путь к файлу или дирректории, а второй это расширение лог-файла.
2) Функция check_params проверяет параметры.
    а) Передано ли расширение для файла. Если нет до берёт дефолтное значение "log".
    б) Проверяет путь до файла или дирректрии на коректность.
    в) Возвращает flag в зависимости от того, что будет парсится, конкретный файл или файл/файлы в дирректории.
        Возвращает путь.
        Возвращает расширение файла.

3) Функция parse_log парсит файл и возвращает список строк из файла.
4) Функция http_requests принимает в себя спсок и выполняет сбор количества запросов по методам HTTP и сложение их общего количества. Возвращает json.
5) Функция often_request принимает в себя спсок и выполняет поиск трёх самый частых IP адресов, которые обращаются к хосту. Возвращает строку.
6) Функция create_json_from_string принимает в себя строку вида "key-231,name-r45,...", разделитель между разными значениями ",", разделитель между ключом и значением "-" и флаг, который указывает на то, какая сторона булет ключём, а какая значением.