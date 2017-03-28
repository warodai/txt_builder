Утилита для генерации текстовых версий словарей 
===============================================

Утилиту следует запускать из командной строки (cmd.exe).

Использование: php.exe builder.php --dir --file [--ref --xedition]
	--dir                     Путь к директории с файлами карточек или,
                              если необходимо сгенерировать прошлую версию по тэгу репозитория,
                              - путь к директории .git (находится
                              внутри директории с карточками)
    --file                    Имя файла, в который необходимо положить результат.
	--ref                     Тэг или коммит, на момент которых нужно взять версию
							  (необязательный параметр, если отсутствует, будет взята последняя версия
    --xedition                Указание на то, что необходимо сгенерировать полную редакторскую версию 

Примеры:

php.exe builder.php --dir ../../warodai-source --file ewarodai.txt
Сгенерировать публичную версию WARODAI непосредственно из файлов карточек и сложить результат в ewarodai.txt

php.exe builder.php --dir ../../warodai-source/.git --file ewarodai.txt --ref 2011-11-17 --xedition
Сгенерировать редакторскую версию WARODAI из репозитория по состоянию на тэг 2011-11-17
