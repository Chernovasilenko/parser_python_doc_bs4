# Парсер документации Python и PEP
# Описание
Парсер документации Python и PEP с помощью библиотеки BeautifulSoup4
# Технологии
# Технологии
- Python 3.12
- BeautifulSoup4
# Установка
Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:Chernovasilenko/parser_python_doc_bs4.git
cd parser_python_doc_bs4
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv venv
source env/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
pip install -r requirements.txt
```

# Инстукция по использованию
Для использования команд необходимо находится в директории parser, содержащей файл main.py и должно быть активировано виртуальное окружение.

Команда для вывода справки по командам:
```
python main.py -h
```
Команда для запуска парсера:
```
python main.py [парсер] [аргументы]
```
## Парсеры
- `whats-new` - выводит список изменений в python
- `latest_versions` - выводит список версий python и ссылки на их документацию
- `download` - скачивает архив с документацией python
- `pep` - выводит список статусов документов pep
и количество документов в каждом статусе.
## Аргументы

- `-c`, `--clear-cache` - очистка кеша перед выполнением парсинга.
```
python main.py [пасер] -c
```
- `-o {pretty,file}`, `--output {pretty,file}`   - дополнительные способы вывода данных   
`pretty` - выводит данные в командной строке в таблице
`file` - сохраняет информацию в формате csv в папке **results**
```
python main.py [парсер] -o file
```