# Russian
Русский язык для панели управления сервером aaPanel

**<h1>Установка</h1>**

## 1 - Боковая панель навигации
Создаем копию файла menu.json
###### `mv -v /www/server/panel/config/"menu.json" /www/server/panel/config/"menu.json_bak"`
Загружаем новый файл с переводом
###### `wget -P /www/server/panel/config https://raw.githubusercontent.com/aaPanel-russian/Russian/main/www/server/panel/config/menu.json`

## 2 - Изменение языка в конфиге панели
Вносим правку в конфиг панели
###### `sed -i 's/English/Russian/g' /www/server/panel/config/config.json`

## 3 - Загружаем и распаковываем архив с языковыми файлами
