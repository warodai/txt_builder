Утилита для генерации текстовых версий словарей 
===============================================

Утилиту следует запускать из командной строки (cmd.exe).

Использование: php.exe builder.php --dir --file [--ref --xedition]


**--dir**       Путь к директории с файлами карточек или, если необходимо сгенерировать прошлую версию по тэгу репозитория, - путь к директории .git (находится внутри директории с карточками)

**--file**      Имя файла, в который необходимо положить результат.

**--ref**       Тэг или коммит, на момент которых нужно взять версию (необязательный параметр, если отсутствует, будет взята последняя версия

**--sort**      Способ сортировки карточек в результирующем файле. Возможные значения: code - по коду, 
kana - по написанию каной, kiriji - по порядку букв в русском алфавите, header - по всему заголовку целиком. По умолчанию - code.

**--xedition**  Указание на то, что необходимо сгенерировать полную редакторскую версию 


Примеры:
--------

Сгенерировать публичную версию WARODAI непосредственно из файлов карточек и сложить результат в warodai.txt
```
php.exe builder.php --dir ../warodai-source --sort kana --file warodai.txt
```

Сгенерировать публичную версию БЯРС непосредственно из файлов карточек и сложить результат в bjrd.txt
```
php.exe builder.php --dir ../bjrd-source --sort code --file bjrd.txt
```

Сгенерировать редакторскую версию БЯРС непосредственно из файлов карточек и сложить результат в xbjrd.txt
```
php.exe builder.php --dir ../bjrd-source --sort code --file xbjrd.txt --xedition
```

Сгенерировать редакторскую версию БЯРС из репозитория по состоянию на тэг 2011-11-17
```
php.exe builder.php --dir ../bjrd-source/.git --sort code --file xbjrd.txt --ref 2011-11-17 --xedition
```