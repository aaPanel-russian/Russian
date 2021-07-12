# Russian
Русский язык для панели управления сервером aaPanel

**<h1>Установка</h1>**

## 1 - Боковая панель навигации
Создаем копию файла menu.json
###### `mv -v /www/server/panel/config/"menu.json" /www/server/panel/config/"menu.json_bak"`
Загружаем новый файл с переводом
###### `wget -P /www/server/panel/config https://raw.githubusercontent.com/aaPanel-russian/Russian/main/www/server/panel/config/menu.json`

## 2 - Изменение языка в конфиге панели
Вносим правки в конфиг панели
###### `sed -i 's/English/Russian/g' /www/server/panel/config/config.json`
###### `sed -i '/{"name":"English","title":"English"}/a {"name":"Russian","title":"Russian"}' /www/server/panel/BTPanel/static/language/list.json`

## 3 - Загружаем и распаковываем архив с языковыми файлами
Загружаем
###### `wget -P /www/server/panel/BTPanel/static/language/ https://github.com/aaPanel-russian/Russian/releases/download/0-01/Russian.zip`
Распаковываем
###### `cd /www/server/panel/BTPanel/static/language`
###### `unzip Russian.zip`

## 4 - Делаем перезапуск aaPanel
Запускаем команду
###### `bt restart`
