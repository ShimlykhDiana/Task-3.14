## Что такое айл .gitignore?

### :exclamation: Файл .gitignore используется для того, чтобы определить, какие файлы и папки не нужно добавлять в git репозиторий.

 В рабочий каталог могут попадать файлы, которые вам бы не хотелось отправлять на сервер. Это и документы с вашими экспериментами или образцами, и автоматически генерируемые части проекта, актуальные только на вашем компьютере. Git может полностью игнорировать их, если создать в рабочем каталоге файл с названием *.gitignore* и внести в него все имена ненужных файлов и папок.


### **Где должен находиться этот файл?**

Файл может находиться в корне проекта или любом подкаталоге.

Либо можно задать глобальный файл gitignore, таким образом:

> $ git config --global core.excludesfile ~/.gitignore_global

Таким образом вы сможете записать в глобальный файл *~/.gitignore_global* настройки, общие для всех ваших проектов. В нем могут храниться например файлы для игнорирования, которые специфичны для вашей IDE, и по этому не логично добавлять их в репозиторий. Однако файлы, которые специфичны для конкретного проекта, обязательно нужно добавлять в *.gitignore* самого проекта.

### Примеры содержимого .gitignore файла


Рекомендуется создавать *.gitignore* **до первой отправки вашего проекта в удаленный репозиторий**, чтобы на сервер не попало никаких лишних файлов и каталогов. Разумеется, важно проверить, чтобы в .*gitignore* не были упомянуты критичные для проекта файлы, иначе у других участников команды возникнут проблемы после следующего обновления.



 Исключить все файлы с расширение .a| *.a
---|---
Но отслеживать файл lib.a даже если он подпадает под исключение выше |!lib.a
Исключить файл TODO в корневом каталоге, но не файл в subdir/TODO |/TODO
Игнорировать все файлы в каталоге build/|build/
Игнорировать файл doc/notes.txt, но не файл doc/server/arch.txt|doc/*.txt
 Игнорировать все .txt файлы в каталоге doc/|doc/**/*.txt 
 
 Читайте подробную документацию по этой ссылке: https://git-scm.com/docs/gitignore<p align = "right"> [![](/assets/pngwing.com-2.png)](./readme.md "домой") 