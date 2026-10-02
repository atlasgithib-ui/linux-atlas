# 🐧 Linux Atlas — offline Linux catalog

**Linux Atlas** — автономный HTML-каталог для изучения, поиска и сравнения Linux-систем и связанных проектов.

Проект содержит **215 систем/проектов** и несколько вариантов одного каталога: от полного `index.html` до экстремально лёгкого `Atlas-micro-V6.html` для старого и слабого оборудования.

> 🇷🇺 Не ищи «лучший Linux». Найди Linux, который подходит именно тебе.

---

## 📦 Что находится в репозитории

В этой версии проекта есть четыре HTML-файла с разной степенью оптимизации:

| Файл | Размер файла* | Для чего предназначен |
|---|---:|---|
| `index.html` | ~20.8 MB | Полная версия каталога |
| `Atlas-lite-V6.html` | ~5.5 MB | Lite: меньше визуальной и технической нагрузки |
| `Atlas-ultra-lite-V6.html` | ~2.4 MB | Ultra Lite: максимально упрощённый интерфейс |
| `Atlas-micro-V6.html` | ~104 KB | Micro: экстремально маленькая версия для очень слабых машин |

\* Размеры указаны для файлов этой поставки.

Все четыре файла являются **самостоятельными HTML-файлами**. Отдельная сборка проекта, npm, Node.js, webpack или другой сборщик для обычного запуска не требуется.

---

# 🧭 Какую версию запускать

### `index.html` — полная версия

Используйте её, если компьютер достаточно современный и нужен исходный интерфейс с максимальным количеством исходных элементов.

В этой версии каталог содержит 215 записей, русский/английский интерфейс, поиск, фильтрацию, сравнение, подробные страницы, аналитику, локальные настройки и другие возможности. В исходном файле также присутствует встроенный аудиоматериал.

### `Atlas-lite-V6.html` — Lite

Более лёгкая версия полного каталога.

Она сохраняет каталог из 215 систем и основные интерактивные возможности, но интерфейс и техническая оболочка упрощены. В файле нет HTML-элемента `<audio>` и встроенного WAV-аудио.

### `Atlas-ultra-lite-V6.html` — Ultra Lite

Версия для старых ПК, старых ноутбуков и браузеров с более ограниченными возможностями.

Интерфейс сделан намеренно простым: обычный HTML/CSS/JavaScript без внешних библиотек, CDN, аудио, тяжёлых визуальных эффектов и лишней графики.

### `Atlas-micro-V6.html` — Micro

Самая компактная версия.

Размер файла — около **104 KB**. Данные каталога находятся во встроенном компактном представлении и распаковываются самим JavaScript при запуске. Поэтому наличие 215 систем в Micro не означает, что все 215 ID должны быть видны обычным поиском текста внутри файла.

Micro предназначен прежде всего для сценария:

- старый Linux;
- старый браузер;
- слабый ноутбук или нетбук;
- очень ограниченная RAM;
- локальный запуск без установки отдельного приложения.

> Важно: маленький размер HTML-файла не означает, что браузер после запуска будет использовать столько же RAM. Сам браузер и его движок всё равно требуют памяти.

---

# ✅ Что есть в каталоге

По содержанию поставленных файлов каталог рассчитан на работу с **215 системами/проектами**.

В зависимости от версии доступны такие основные возможности:

- 🔎 поиск по каталогу;
- 🧩 фильтры;
- ↕️ сортировка;
- 🗂️ карточки систем;
- 📋 табличное представление в полноразмерных версиях;
- ⚖️ сравнение систем;
- 📊 аналитические/сводные разделы;
- 🖥️ подробные страницы отдельных систем;
- 💻 сведения об оборудовании и системных требованиях;
- 🌐 русский и English;
- 📱 адаптация под небольшие экраны;
- 💾 локальное сохранение части настроек через `localStorage` там, где это поддерживает версия;
- #️⃣ переходы к отдельным страницам через hash-маршруты в версиях, где этот механизм включён.

Каталог является **справочным**. Он не устанавливает Linux и не изменяет разделы диска сам по себе.

---

# 🚀 Самый простой запуск

## Вариант A — открыть HTML-файл напрямую

Для автономного использования можно открыть нужный файл двойным щелчком из файлового менеджера.

Например:

```text
Atlas-micro-V6.html
```

или:

```text
Atlas-ultra-lite-V6.html
```

Если браузер нормально показывает каталог, ничего дополнительно устанавливать не нужно.

Если при открытии через `file://` возникают ошибки, пустая страница или часть функций не работает, используйте **локальный HTTP-сервер**. Это самый надёжный способ запуска.

---

# 🐧 Linux — запуск через терминал

Сначала перейдите в папку проекта.

Если проект находится в домашней папке:

```bash
cd ~/linux-atlas
```

Если папка находится, например, в `Downloads`:

```bash
cd ~/Downloads/linux-atlas
```

Проверить, где вы находитесь:

```bash
pwd
```

Показать файлы:

```bash
ls -lh
```

Вы должны увидеть примерно такие имена:

```text
index.html
Atlas-lite-V6.html
Atlas-ultra-lite-V6.html
Atlas-micro-V6.html
README.md
```

---

## 🐍 Способ 1 — Python 3

Проверка:

```bash
python3 --version
```

Запуск сервера:

```bash
python3 -m http.server 8000
```

После запуска в терминале обычно появится сообщение о сервере на порту `8000`.

Откройте браузер и перейдите на:

```text
http://127.0.0.1:8000/
```

или:

```text
http://localhost:8000/
```

### Сразу открыть Micro

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

### Сразу открыть Ultra Lite

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

### Сразу открыть Lite

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

### Сразу открыть полную версию

```text
http://127.0.0.1:8000/index.html
```

Остановить сервер:

```text
Ctrl+C
```

---

# 🐍 Если `python3` не найден

Попробуйте обычную команду `python`:

```bash
python --version
```

Если это Python 3:

```bash
python -m http.server 8000
```

Если на очень старой системе установлен **Python 2**, команда HTTP-сервера другая:

```bash
python -m SimpleHTTPServer 8000
```

После этого откройте:

```text
http://127.0.0.1:8000/
```

> Python 2 давно устарел. Здесь эта команда приведена именно как аварийный вариант для старой Linux-системы, где уже установлен старый Python.

---

# 🧰 Если Python вообще нет

Для старых систем часто полезен BusyBox.

Проверка:

```bash
busybox | head
```

Если есть `httpd`, можно попробовать:

```bash
busybox httpd -f -p 8000 -h .
```

После этого:

```text
http://127.0.0.1:8000/
```

Остановить сервер обычно можно через:

```text
Ctrl+C
```

Если ваша сборка BusyBox не позволяет использовать `httpd` таким образом, используйте другой способ из этого README.

---

# 🐘 Если есть PHP

Проверка:

```bash
php --version
```

Запуск:

```bash
php -S 127.0.0.1:8000
```

Затем:

```text
http://127.0.0.1:8000/
```

Остановить:

```text
Ctrl+C
```

---

# 🪟 Windows — CMD / PowerShell

Откройте `cmd.exe` или PowerShell.

Перейдите в папку проекта, например:

```bat
cd C:\Users\YOUR_NAME\Downloads\linux-atlas
```

Проверить Python:

```bat
py --version
```

Если команда работает:

```bat
py -m http.server 8000
```

Либо:

```bat
python -m http.server 8000
```

Откройте:

```text
http://127.0.0.1:8000/
```

Или конкретный файл:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

Остановить сервер:

```text
Ctrl+C
```

---

# 🍎 macOS

В Terminal:

```bash
cd ~/Downloads/linux-atlas
python3 -m http.server 8000
```

Откройте:

```text
http://127.0.0.1:8000/
```

Остановить:

```text
Ctrl+C
```

---

# 📱 Android / Termux

Если используется Termux и Python ещё не установлен:

```bash
pkg update
pkg install python
```

Перейдите в каталог проекта:

```bash
cd ~/linux-atlas
```

Запустите сервер:

```bash
python -m http.server 8000
```

Откройте браузер Android и введите:

```text
http://127.0.0.1:8000/
```

Micro можно открыть напрямую:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

---

# 🌐 Если порт 8000 занят

Ошибка вида:

```text
OSError: [Errno 98] Address already in use
```

означает, что порт уже используется другим процессом.

Попробуйте другой порт, например `8080`:

```bash
python3 -m http.server 8080
```

Затем:

```text
http://127.0.0.1:8080/
```

Ещё варианты:

```bash
python3 -m http.server 8888
```

или:

```bash
python3 -m http.server 3000
```

Порт можно выбрать практически любой свободный пользовательский порт выше 1024.

---

# 🔧 Если команда запущена не из той папки

Очень частая ошибка — сервер запускается из домашнего каталога или другой папки.

Проверка:

```bash
pwd
```

Linux/macOS:

```bash
ls
```

Windows CMD:

```bat
dir
```

В списке должен находиться нужный HTML-файл.

Например:

```text
Atlas-micro-V6.html
```

Если файла там нет, сначала выполните `cd` в правильный каталог.

---

# 📁 Пример с абсолютным путём

Linux:

```bash
cd /home/USER/linux-atlas
python3 -m http.server 8000
```

или, например:

```bash
cd /home/USER/Downloads/linux-atlas
python3 -m http.server 8000
```

macOS:

```bash
cd /Users/USER/Downloads/linux-atlas
python3 -m http.server 8000
```

Windows CMD:

```bat
cd /d C:\Users\USER\Downloads\linux-atlas
py -m http.server 8000
```

Замените `USER` на имя своей учётной записи.

---

# 🔽 Как скачать репозиторий через Git

Если Git установлен:

```bash
git clone https://github.com/atlasgithib-ui/linux-atlas.git
```

Перейдите в каталог:

```bash
cd linux-atlas
```

Посмотрите содержимое:

```bash
ls -lh
```

Запустите локальный сервер:

```bash
python3 -m http.server 8000
```

Откройте:

```text
http://127.0.0.1:8000/
```

Репозиторий проекта:

https://github.com/atlasgithib-ui/linux-atlas

---

# 🔄 Если Git уже использовался раньше

Перейдите в каталог проекта:

```bash
cd linux-atlas
```

Проверьте состояние:

```bash
git status
```

Получите изменения:

```bash
git pull
```

После обновления снова можно запустить:

```bash
python3 -m http.server 8000
```

---

# 🧪 Быстрая проверка перед запуском

Linux/macOS:

```bash
test -f index.html && echo "OK: index.html"
test -f Atlas-lite-V6.html && echo "OK: Atlas-lite-V6.html"
test -f Atlas-ultra-lite-V6.html && echo "OK: Atlas-ultra-lite-V6.html"
test -f Atlas-micro-V6.html && echo "OK: Atlas-micro-V6.html"
```

Если хотите проверить размеры:

```bash
ls -lh index.html Atlas-lite-V6.html Atlas-ultra-lite-V6.html Atlas-micro-V6.html
```

Проверить, что HTML-файлы существуют и читаются:

```bash
wc -c index.html Atlas-lite-V6.html Atlas-ultra-lite-V6.html Atlas-micro-V6.html
```

---

# 🧩 Как понять, что сервер действительно работает

После запуска:

```bash
python3 -m http.server 8000
```

в другом окне терминала можно проверить HTTP:

```bash
curl -I http://127.0.0.1:8000/
```

Нормальный ответ должен начинаться примерно так:

```text
HTTP/1.0 200 OK
```

или другим вариантом `200 OK` в зависимости от версии Python/сервера.

Для конкретного Micro-файла:

```bash
curl -I http://127.0.0.1:8000/Atlas-micro-V6.html
```

> `curl` проверяет доступность файла по HTTP. Он не заменяет браузер и не выполняет полноценный JavaScript-каталог.

---

# 🪶 Что делать на очень старом ПК

Если компьютер очень слабый, не начинайте с полной версии `index.html`.

Рекомендуемый порядок проверки такой:

```text
1. Atlas-micro-V6.html
2. Atlas-ultra-lite-V6.html
3. Atlas-lite-V6.html
4. index.html
```

Сначала откройте Micro. Если браузер работает с ним нормально, можно попробовать Ultra Lite.

Если компьютер уверенно работает с Ultra Lite, попробуйте Lite.

Полную версию запускайте последней.

Это не является строгим требованием: это просто практический порядок от самого маленького файла к самому тяжёлому.

---

# 🧠 Важно про RAM и браузер

Размер HTML нельзя напрямую переводить в требуемую оперативную память.

Например, `Atlas-micro-V6.html` занимает около 104 KB на диске, но при запуске браузер должен:

1. прочитать HTML;
2. выполнить JavaScript;
3. распаковать/создать структуру данных каталога;
4. построить DOM-интерфейс;
5. хранить состояние страницы в памяти;
6. выполнять поиск, фильтрацию и другие операции.

Поэтому **104 KB файла не означает 104 KB RAM**.

Для крайне старого компьютера решающим ограничением может оказаться именно браузер, а не размер HTML.

---

# 🧑‍💻 Какие браузеры пробовать на старых системах

Конкретная совместимость зависит от операционной системы, версии браузера и JavaScript-движка.

Для старого компьютера логика тестирования простая:

```text
1. Запустить Micro.
2. Проверить загрузку страницы.
3. Проверить поиск.
4. Проверить открытие карточки/подробностей.
5. Проверить переключение языка.
6. Проверить сравнение, если оно используется в данной версии.
```

Если браузер показывает пустую страницу или `JavaScript is required`, попробуйте более современный браузер, который ещё можно установить на вашу систему, либо другую версию Linux/браузера.

**README не заявляет абсолютную совместимость со всеми историческими браузерами.** Реальная совместимость всегда зависит от конкретного браузера.

---

# 🛠️ Если открывается белая страница

Делайте по порядку.

### Шаг 1 — запустите через HTTP

```bash
python3 -m http.server 8000
```

И откройте:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

### Шаг 2 — проверьте сам файл

```bash
ls -lh Atlas-micro-V6.html
```

Если файла нет, вы находитесь не в каталоге проекта.

### Шаг 3 — проверьте браузер

Попробуйте другую установленную версию браузера.

### Шаг 4 — посмотрите консоль браузера

Если браузер умеет Developer Tools / Console, откройте консоль и посмотрите текст ошибки JavaScript.

### Шаг 5 — попробуйте Ultra Lite

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

Если Ultra Lite работает, но полная версия нет, проблема может быть связана с нагрузкой полной версии, а не с локальным сервером.

---

# 🛠️ Если `python3` тоже не найден

Проверьте доступные варианты:

```bash
which python3
which python
which php
which busybox
which ruby
```

Также:

```bash
command -v python3
command -v python
command -v php
command -v busybox
```

Используйте тот сервер, который реально установлен в системе.

---

# 🔌 Локальный сервер и Интернет

Сам каталог является локальным HTML-проектом: HTML, CSS и JavaScript находятся внутри файлов.

Локальный запуск через:

```text
http://127.0.0.1:8000/
```

не требует публикации сайта в Интернет и не требует внешнего веб-сервера.

При этом **ссылки на документацию и другие внешние материалы**, которые содержатся в каталоге, могут вести в Интернет. Сам переход по такой ссылке уже требует соответствующего сетевого доступа.

---

# ⚠️ Важное отличие между «локально работает» и «полностью офлайн»

Сам интерфейс каталога может запускаться без Интернета.

Но если вы нажмёте внешнюю ссылку на официальный сайт дистрибутива, GitHub, документацию или другой ресурс, для открытия этого ресурса понадобится Интернет.

Это нормально: внешний источник не является частью локального HTML-каталога.

---

# 🔒 Безопасность

Linux Atlas — справочный HTML-каталог.

Он **не предназначен для установки Linux автоматически** и сам по себе не должен изменять разделы диска, загрузчик или системные файлы.

Тем не менее всегда соблюдайте обычную осторожность:

- не запускайте неизвестные команды из случайных источников;
- проверяйте команды перед копированием в терминал;
- перед установкой настоящей ОС делайте резервную копию важных данных;
- внимательно проверяйте, какой диск выбран установщиком Linux.

Особенно важно: команды из этого README запускают **локальный HTTP-сервер каталога**. Они не являются командами установки Linux.

---

# 🧹 Как остановить локальный сервер

В том же окне терминала:

```text
Ctrl+C
```

После этого `http://127.0.0.1:8000/` перестанет открываться, пока вы снова не запустите сервер.

---

# 🗑️ Как удалить локальный серверный процесс, если окно терминала закрыли неправильно

Обычно достаточно просто найти процесс, использующий порт.

Linux:

```bash
ss -ltnp | grep ':8000'
```

Если `ss` нет:

```bash
netstat -ltnp 2>/dev/null | grep ':8000'
```

После этого сначала используйте нормальное завершение процесса. Не убивайте случайный процесс только потому, что он использует порт: убедитесь, что это именно запущенный вами Python/PHP/BusyBox-сервер.

---

# 📂 Структура проекта

Минимально ожидаемая структура:

```text
linux-atlas/
├── index.html
├── Atlas-lite-V6.html
├── Atlas-ultra-lite-V6.html
├── Atlas-micro-V6.html
└── README.md
```

Все HTML-файлы можно хранить рядом в одной папке.

---

# 🔗 Прямые ссылки на файлы после запуска сервера

Если сервер запущен так:

```bash
python3 -m http.server 8000
```

то:

**Полная версия**

```text
http://127.0.0.1:8000/index.html
```

**Lite**

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

**Ultra Lite**

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

**Micro**

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

---

# 📝 Если браузер сам открывает не тот файл

Это нормально: сервер просто показывает содержимое каталога.

Не нужно переименовывать все файлы.

Введите адрес нужного файла вручную, например:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

---

# 📱 Доступ с другого устройства в одной локальной сети

Если нужно открыть каталог, например, с телефона, а сервер работает на компьютере, можно привязать сервер ко всем локальным интерфейсам:

```bash
python3 -m http.server 8000 --bind 0.0.0.0
```

Затем на компьютере узнайте локальный IP.

Linux:

```bash
ip addr
```

или:

```bash
hostname -I
```

После этого на другом устройстве в той же сети используйте:

```text
http://IP_КОМПЬЮТЕРА:8000/
```

Например:

```text
http://192.168.1.50:8000/
```

> Делайте это только в доверенной локальной сети и помните, что сервер, привязанный к `0.0.0.0`, может быть доступен другим устройствам в этой сети. Для обычного запуска на одном компьютере используйте `127.0.0.1`.

---

# 🐧 Старый Linux / слабый ПК: практический сценарий

Для старого компьютера можно работать так:

```bash
cd ~/linux-atlas
python3 -m http.server 8000
```

Затем открыть:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

Если Micro запустился — проверить Ultra Lite:

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

Если Ultra Lite запустился нормально — попробовать Lite:

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

И только затем:

```text
http://127.0.0.1:8000/index.html
```

Так проще понять реальные пределы старого компьютера и браузера.

---

# 🧾 Что проверить после запуска

Минимальный чек-лист:

- [ ] Страница открылась.
- [ ] Видны системы каталога.
- [ ] Работает поиск.
- [ ] Работают фильтры.
- [ ] Открывается подробная информация.
- [ ] Можно переключить русский/English.
- [ ] Страница не зависает надолго при открытии.
- [ ] Нужная версия не потребляет слишком много памяти для конкретного ПК.

---

# 💾 Резервная копия

Если вы меняете HTML вручную, сначала сделайте копию:

```bash
cp Atlas-micro-V6.html Atlas-micro-V6.backup.html
```

Для полной версии:

```bash
cp index.html index.backup.html
```

Для Lite:

```bash
cp Atlas-lite-V6.html Atlas-lite-V6.backup.html
```

Для Ultra Lite:

```bash
cp Atlas-ultra-lite-V6.html Atlas-ultra-lite-V6.backup.html
```

---

# 🧑‍🔧 Если HTML был случайно повреждён

Если проект клонирован из GitHub и изменения не нужны, можно скачать чистую копию заново:

```bash
git status
```

Если нужно проверить, какие файлы изменились:

```bash
git diff --stat
```

Для конкретного файла:

```bash
git diff -- index.html
```

**Не используйте `git reset --hard` без понимания последствий**: эта команда может удалить локальные изменения.

Если вы не хотите терять свои изменения, сначала сделайте копию файла.

---

# 📚 О проекте

Linux Atlas предназначен для самостоятельного изучения Linux-систем.

Каталог помогает:

- находить системы по названию и параметрам;
- изучать требования к оборудованию;
- сравнивать проекты;
- рассматривать лёгкие системы для старого оборудования;
- читать подробные пользовательские пояснения;
- использовать русский и английский интерфейс.

Проект не утверждает, что существует одна универсальная Linux-система для всех пользователей.

---

# ⚖️ Данные и официальная документация

Linux Atlas — независимый справочный проект.

Названия Linux-систем, логотипы, товарные знаки и материалы отдельных проектов принадлежат соответствующим правообладателям.

Перед установкой конкретной ОС рекомендуется сверяться с официальной документацией соответствующего проекта, особенно для:

- архитектуры CPU;
- совместимости оборудования;
- загрузки с USB/DVD;
- UEFI/Legacy Boot;
- разметки диска;
- драйверов;
- Wi‑Fi/Bluetooth;
- установки и восстановления системы.

---

# 🌐 Репозиторий

GitHub:

https://github.com/atlasgithib-ui/linux-atlas

---

# 🛠️ Технологии

Каталог построен как автономный веб-проект и использует:

- HTML
- CSS
- JavaScript

Для обычного запуска отдельная установка приложения не требуется.

---

# 📌 Краткая памятка для терминала

### Скачать

```bash
git clone https://github.com/atlasgithib-ui/linux-atlas.git
cd linux-atlas
```

### Посмотреть файлы

```bash
ls -lh
```

### Самый простой запуск

```bash
python3 -m http.server 8000
```

### Открыть

```text
http://127.0.0.1:8000/
```

### Micro

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

### Ultra Lite

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

### Lite

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

### Полная версия

```text
http://127.0.0.1:8000/index.html
```

### Остановить

```text
Ctrl+C
```

---

# ✅ Если ничего не получается

Используйте этот порядок без пропуска шагов:

```bash
cd /путь/к/linux-atlas
pwd
ls -lh
python3 --version
python3 -m http.server 8000
```

Если `python3` отсутствует:

```bash
python --version
python -m http.server 8000
```

Если это старый Python 2:

```bash
python -m SimpleHTTPServer 8000
```

Если Python отсутствует, проверьте:

```bash
php --version
busybox | head
```

После успешного запуска откройте:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

Если Micro работает, переходите к Ultra Lite, затем Lite и только потом к полной версии.

---

## ❤️ Спасибо за использование Linux Atlas

**Explore. Compare. Find the Linux that fits you.**

🇷🇺 Изучай. Сравнивай. Находи систему под себя.

---

# 🇬🇧 ENGLISH VERSION

## 🐧 Linux Atlas — offline Linux catalog

**Linux Atlas** is a self-contained HTML catalog for exploring, searching and comparing Linux systems and related projects.

This repository contains **215 systems/projects** and four versions of the catalog, from the full `index.html` to the extremely small `Atlas-micro-V6.html` for older and weaker hardware.

> 🇬🇧 Don't look for the “best Linux”. Find the Linux that fits your hardware, tasks and preferences.

---

## 📦 Files in the repository

| File | Approx. size* | Purpose |
|---|---:|---|
| `index.html` | ~20.8 MB | Full catalog |
| `Atlas-lite-V6.html` | ~5.5 MB | Lite version with reduced visual/technical load |
| `Atlas-ultra-lite-V6.html` | ~2.4 MB | Ultra Lite for older PCs and browsers |
| `Atlas-micro-V6.html` | ~104 KB | Extreme Micro version for very limited machines |

\* Approximate sizes for this release.

All four files are standalone HTML files. You do **not** need npm, Node.js, webpack, a build system, a package manager, or an external library just to run the catalog.

---

# 🧭 Which version should you run?

### `index.html` — Full version

Use this version when the computer is reasonably modern and you want the original, feature-rich interface.

It contains the 215 catalog entries, Russian/English interface, search, filters, comparison, detailed pages, analytics and other original functionality. The source file also contains embedded audio material.

### `Atlas-lite-V6.html` — Lite

A lighter version of the full catalog.

It keeps the 215 systems and the main interactive functionality while reducing visual and technical overhead. The Lite file does not contain the original embedded audio element/WAV data.

### `Atlas-ultra-lite-V6.html` — Ultra Lite

Designed for older PCs, older laptops and browsers with more limited capabilities.

The interface is intentionally simple and avoids external libraries, CDNs, audio and unnecessary heavy visual effects.

### `Atlas-micro-V6.html` — Micro

The smallest version in the repository.

The file is approximately **104 KB**. The catalog data is stored in a compact embedded representation and reconstructed by JavaScript when the page starts.

Therefore, a 104 KB HTML file does **not** mean that the browser only needs 104 KB of RAM. The browser engine and the decoded catalog still require memory.

Micro is intended for scenarios such as:

- old Linux systems;
- old web browsers;
- weak laptops and netbooks;
- very limited RAM;
- local/offline use;
- simple machines where the full interface is unnecessarily heavy.

---

# ✅ What the catalog contains

The supplied files contain information for **215 systems/projects**.

Depending on the selected version, the main functionality includes:

- 🔎 catalog search;
- 🧩 filters;
- ↕️ sorting;
- 🗂️ system cards;
- 📋 table view in the larger versions;
- ⚖️ system comparison;
- 📊 analytical/summary sections;
- 🖥️ detailed pages for individual systems;
- 💻 hardware and system requirements;
- 🌐 Russian and English interface support;
- 📱 responsive use on smaller screens;
- 💾 local browser storage/fallback functionality where supported by the version.

The catalog is a reference tool. It does not install Linux and does not automatically modify your operating system.

---

# 🚀 Quickest way to start

## Option A — open an HTML file directly

The simplest method is to open one of the HTML files in a browser.

For example:

```text
Atlas-micro-V6.html
```

Double-click the file in a graphical file manager, or use the browser's **Open File** command.

For modern browsers this may be enough.

For older browsers or when local JavaScript behaves differently, use a small local HTTP server instead. The terminal method below is usually more reliable.

---

# 🐧 Linux — terminal launch

First open a terminal and move to the directory containing the four HTML files.

### Check your current directory

```bash
pwd
```

### List the files

```bash
ls -lh
```

You should see files similar to:

```text
index.html
Atlas-lite-V6.html
Atlas-ultra-lite-V6.html
Atlas-micro-V6.html
README.md
```

If you do not see them, you are probably in the wrong directory. Use `cd` to enter the correct directory.

Example:

```bash
cd ~/linux-atlas
```

Then check again:

```bash
ls -lh
```

---

# 🐍 Method 1 — Python 3

This is the preferred terminal method when Python 3 is available.

Run:

```bash
python3 -m http.server 8000
```

You should see a message similar to:

```text
Serving HTTP on 0.0.0.0 port 8000 ...
```

Then open:

```text
http://127.0.0.1:8000/
```

or:

```text
http://localhost:8000/
```

### Open Micro

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

### Open Ultra Lite

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

### Open Lite

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

### Open the full version

```text
http://127.0.0.1:8000/index.html
```

Keep the terminal window open while the server is running.

To stop the server, press:

```text
Ctrl+C
```

---

# 🐍 If `python3` is not found

Try:

```bash
python -m http.server 8000
```

If that also fails, check whether Python exists:

```bash
which python3
```

and:

```bash
which python
```

You can also check the version:

```bash
python3 --version
```

or:

```bash
python --version
```

If there is no Python installation, use one of the alternatives below.

---

# 🧰 If Python is not installed

## BusyBox

Some small Linux systems include BusyBox.

Check:

```bash
busybox
```

If the `httpd` applet is available, start a server from the project directory:

```bash
busybox httpd -f -p 8000
```

Then open:

```text
http://127.0.0.1:8000/
```

Stop it with `Ctrl+C` if running in the foreground.

## PHP

If PHP is installed:

```bash
php -S 127.0.0.1:8000
```

Then open:

```text
http://127.0.0.1:8000/
```

Check PHP first with:

```bash
php --version
```

---

# 🪟 Windows — CMD / PowerShell

Open **Command Prompt** or **PowerShell** and move into the directory containing the project.

Example:

```bat
cd C:\linux-atlas
```

Check the files:

```bat
dir
```

If Python 3 is installed:

```bat
py -m http.server 8000
```

If `py` is not available, try:

```bat
python -m http.server 8000
```

Then open:

```text
http://127.0.0.1:8000/
```

To stop the server:

```text
Ctrl+C
```

---

# 🍎 macOS

Open Terminal and enter the project directory:

```bash
cd ~/linux-atlas
```

Then:

```bash
python3 -m http.server 8000
```

Open:

```text
http://127.0.0.1:8000/
```

---

# 📱 Android / Termux

If you are using Termux and Python is installed, go to the directory containing the files and run:

```bash
python3 -m http.server 8000
```

Then open the browser on the same device and visit:

```text
http://127.0.0.1:8000/
```

If Python is not installed in Termux, install it using the package manager available in your Termux installation, then repeat the command above.

For very weak Android hardware, start with `Atlas-micro-V6.html` rather than the full version.

---

# 🌐 If port 8000 is already in use

Try another port, for example `8080`:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://127.0.0.1:8080/
```

You can also try `8888`:

```bash
python3 -m http.server 8888
```

The important rule is simple: the port number in the command and the URL must match.

For example:

```text
python3 -m http.server 8080
```

means:

```text
http://127.0.0.1:8080/
```

---

# 🔧 If the command was started in the wrong directory

If the browser shows a directory that does not contain Linux Atlas, stop the server:

```text
Ctrl+C
```

Find the project directory:

```bash
pwd
ls -lh
```

Then use `cd`:

```bash
cd /path/to/linux-atlas
```

Check:

```bash
ls -lh
```

Finally start the server again:

```bash
python3 -m http.server 8000
```

---

# 📁 Example using an absolute path

If your files are stored in:

```text
/home/user/linux-atlas
```

run:

```bash
cd /home/user/linux-atlas
python3 -m http.server 8000
```

Do not literally copy `/home/user/linux-atlas` unless that is your actual path. Replace it with the real directory.

To find your home directory:

```bash
echo "$HOME"
```

---

# 🔽 Clone the repository with Git

Official repository:

```text
https://github.com/atlasgithib-ui/linux-atlas
```

Clone it with:

```bash
git clone https://github.com/atlasgithib-ui/linux-atlas.git
```

Enter the directory:

```bash
cd linux-atlas
```

Check the files:

```bash
ls -lh
```

Start the local server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://127.0.0.1:8000/
```

If Git is not installed, you can download the repository as a ZIP archive from GitHub and extract it instead.

---

# 🔄 If Git was used before

If the repository already exists locally, do not clone it again into the same directory.

Enter it:

```bash
cd linux-atlas
```

Check its status:

```bash
git status
```

If you simply want the latest remote changes and you have not made local changes that must be preserved:

```bash
git pull
```

If you are unsure whether you have local modifications, read the output of `git status` before changing anything.

---

# 🧪 Quick check before launching

From the project directory run:

```bash
pwd
ls -lh
```

Then verify that the four HTML files exist:

```bash
ls -lh index.html Atlas-lite-V6.html Atlas-ultra-lite-V6.html Atlas-micro-V6.html
```

If a file is reported as missing, do not continue with a filename that does not exist. Check the directory with:

```bash
ls -lah
```

---

# 🧩 How to know that the server is actually running

After:

```bash
python3 -m http.server 8000
```

open another terminal and run:

```bash
curl -I http://127.0.0.1:8000/
```

A working server should return an HTTP response such as:

```text
HTTP/1.0 200 OK
```

You can also test Micro directly:

```bash
curl -I http://127.0.0.1:8000/Atlas-micro-V6.html
```

If the server is running but the browser cannot connect, check whether you used the correct port and address.

---

# 🪶 Very old PC / weak Linux

For an old computer, start with:

```text
Atlas-micro-V6.html
```

If it works correctly but you want more convenience, try:

```text
Atlas-ultra-lite-V6.html
```

Then:

```text
Atlas-lite-V6.html
```

Use:

```text
index.html
```

when the machine and browser can comfortably handle the full interface.

The exact browser requirements cannot be guaranteed for every historical Linux distribution/browser combination without testing that particular machine.

---

# 🧠 Important: RAM is not the same as HTML file size

`Atlas-micro-V6.html` is extremely small on disk, but the browser must still:

1. load the HTML;
2. execute JavaScript;
3. reconstruct the catalog data;
4. create the interface;
5. render the selected records.

Therefore, the file size is only one part of the resource requirement.

On very old hardware, the browser itself may be the largest consumer of RAM.

---

# 🧑‍💻 Browsers on old systems

There is no single browser that can be guaranteed to work on every historical Linux distribution.

If a modern browser is available, test the catalog there first.

If you are working with a very old Linux installation, choose a browser appropriate for that operating system and CPU architecture. Start with `Atlas-micro-V6.html` because it has the smallest interface and data representation.

Do not assume that every browser claiming HTML support also supports every JavaScript feature used by every version of Linux Atlas.

---

# 🛠️ If the browser shows a blank/white page

Follow these steps in order.

### Step 1 — use the HTTP server

Instead of opening the HTML directly, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

### Step 2 — verify the file

```bash
ls -lh Atlas-micro-V6.html
```

### Step 3 — try another browser

If possible, test the same file in another browser available on the machine.

### Step 4 — check the browser console

If the browser has a developer console, look for a JavaScript error. Record the exact error text before changing files.

### Step 5 — try an older version of the interface

If Micro fails, try:

```text
Atlas-ultra-lite-V6.html
```

If that also fails, test the Lite version and finally the full version.

Do not immediately delete or rewrite the HTML. First identify whether the problem is the browser, the server, the path, or the file itself.

---

# 🛠️ If `python3` is also missing

Run:

```bash
which python3
which python
which php
which busybox
```

The commands that print a path indicate which runtime is available.

Examples:

```text
/usr/bin/python3
```

or:

```text
/usr/bin/php
```

If none of these commands returns a usable program, you can still open the HTML file directly in a browser if that browser supports the file correctly.

---

# 🔌 Local server and Internet access

Running:

```bash
python3 -m http.server 8000
```

does **not** publish the catalog to the Internet by itself.

By default, the server is intended for local access on the machine. If you explicitly bind it to a network interface or expose the machine to other devices, other devices on the local network may be able to access it.

For a local-only server, prefer:

```bash
python3 -m http.server --bind 127.0.0.1 8000
```

Then use:

```text
http://127.0.0.1:8000/
```

---

# ⚠️ Local operation vs. completely offline operation

The HTML catalog itself is designed as a self-contained local project.

However, a link inside the catalog can still point to an external website. Opening such a link obviously requires network access to that external site.

The catalog does not need an Internet connection merely to display its embedded catalog data when using a standalone version that contains the required data.

---

# 🔒 Safety

Linux Atlas is a catalog/reference website. It does not install an operating system for you.

The local HTTP server only serves files from the directory in which you start it.

Before running commands copied from another source, make sure you understand what they do.

In particular, be extremely careful with commands involving:

- `sudo`;
- disk devices such as `/dev/sda` or `/dev/nvme0n1`;
- `rm`;
- formatting tools;
- partitioning tools;
- bootloader changes.

Linux Atlas itself does not require any of those commands merely to open the catalog.

---

# 🧹 Stop the local server

If the server is running in the foreground, press:

```text
Ctrl+C
```

You should then return to the normal shell prompt.

---

# 🗑️ If the terminal was closed incorrectly

Normally the Python server exits when its terminal process is closed.

If you suspect a server is still listening on port 8000, check it with a tool available on your system, for example:

```bash
ss -ltnp | grep 8000
```

or, on older systems where `ss` is unavailable:

```bash
netstat -ltnp 2>/dev/null | grep 8000
```

Do not kill a process blindly. First identify the process and confirm that it is the server you started.

---

# 📂 Project structure

A typical directory can look like this:

```text
linux-atlas/
├── index.html
├── Atlas-lite-V6.html
├── Atlas-ultra-lite-V6.html
├── Atlas-micro-V6.html
└── README.md
```

The HTML files can be used independently. You do not need to compile them before normal use.

---

# 🔗 Direct file URLs after starting the server

With:

```bash
python3 -m http.server 8000
```

the files are available at:

```text
http://127.0.0.1:8000/index.html
http://127.0.0.1:8000/Atlas-lite-V6.html
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
http://127.0.0.1:8000/Atlas-micro-V6.html
```

---

# 📝 If the browser opens the wrong file

Do not rely only on the directory index.

Enter the exact file name in the address bar:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

or:

```text
http://127.0.0.1:8000/index.html
```

This makes it clear which version you are testing.

---

# 📱 Access from another device on the same LAN

If you intentionally want another device on the local network to access the catalog, bind the server to the machine's network interface, for example:

```bash
python3 -m http.server 8000 --bind 0.0.0.0
```

Find the computer's local IP address with a command appropriate for your system, for example:

```bash
ip addr
```

Then another device can try:

```text
http://YOUR_LOCAL_IP:8000/
```

Replace `YOUR_LOCAL_IP` with the actual LAN address.

Example format:

```text
http://192.168.1.50:8000/
```

This is different from the local-only `127.0.0.1` configuration. Do not expose the server to networks you do not trust.

---

# 🐧 Practical scenario: old Linux / weak PC

A simple workflow is:

```bash
cd /path/to/linux-atlas
ls -lh
python3 -m http.server --bind 127.0.0.1 8000
```

Then open:

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

If Micro works comfortably, you can try Ultra Lite:

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

If that is also comfortable, try Lite:

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

Only move to the full version when the machine handles it comfortably.

---

# 🧾 What to check after launch

After opening the catalog, verify:

- the page loads without a blank screen;
- the catalog entries appear;
- search responds;
- filters respond;
- language switching works where available;
- detailed pages open;
- comparison works where available;
- the browser does not freeze for an unreasonable amount of time.

On very weak hardware, give the browser some time after the initial page load before deciding that the file has failed.

---

# 💾 Backup

Before editing any HTML file, make a backup.

For example:

```bash
cp Atlas-micro-V6.html Atlas-micro-V6.backup.html
```

Or back up the complete directory:

```bash
cp -a linux-atlas linux-atlas-backup
```

Make sure the destination does not already contain a backup you intend to preserve before using commands that overwrite files.

---

# 🧑‍🔧 If an HTML file was accidentally damaged

First stop editing it.

If the project is under Git, check:

```bash
git status
```

If you have uncommitted changes that you need, do not blindly reset the file.

If you simply downloaded a fresh copy and have no local changes to preserve, you can compare the files or restore the clean repository version using the normal Git workflow.

If there is no Git history, restore your own backup instead:

```text
Atlas-micro-V6.backup.html
```

Do not try to repair a large embedded catalog by manually deleting random parts of the HTML.

---

# 📚 About the project

Linux Atlas is an independent reference/catalog project for exploring the Linux ecosystem.

It is intended to help users:

- explore Linux systems;
- search the catalog;
- compare systems;
- understand hardware requirements;
- look for lightweight options;
- examine desktop and interface characteristics;
- use the catalog offline.

The catalog contains **215 systems/projects** in the supplied release.

---

# ⚖️ Data and official documentation

Linux Atlas is a reference catalog and is not the official documentation for most projects listed in it.

Names, logos, trademarks and other project-specific materials belong to their respective rights holders.

Before installing an operating system, always consult the official documentation of the corresponding project, especially for:

- supported CPU architectures;
- supported devices;
- installation procedure;
- boot requirements;
- storage requirements;
- graphics and Wi-Fi support;
- release-specific instructions.

---

# 🌐 Repository

GitHub:

```text
https://github.com/atlasgithib-ui/linux-atlas
```

Clone command:

```bash
git clone https://github.com/atlasgithib-ui/linux-atlas.git
```

---

# 🛠️ Technologies

The project is based on:

- HTML;
- CSS;
- JavaScript.

The standalone HTML files do not require a separate application installation for normal use.

---

# 📌 Terminal cheat sheet

### Download

```bash
git clone https://github.com/atlasgithib-ui/linux-atlas.git
cd linux-atlas
```

### List files

```bash
ls -lh
```

### Start the local server

```bash
python3 -m http.server 8000
```

### Open

```text
http://127.0.0.1:8000/
```

### Micro

```text
http://127.0.0.1:8000/Atlas-micro-V6.html
```

### Ultra Lite

```text
http://127.0.0.1:8000/Atlas-ultra-lite-V6.html
```

### Lite

```text
http://127.0.0.1:8000/Atlas-lite-V6.html
```

### Full

```text
http://127.0.0.1:8000/index.html
```

### Stop

```text
Ctrl+C
```

---

# ✅ If nothing works

Use this exact diagnostic sequence:

```bash
pwd
ls -lah
ls -lh index.html Atlas-lite-V6.html Atlas-ultra-lite-V6.html Atlas-micro-V6.html
python3 --version
python3 -m http.server 8000
```

Then, from another terminal:

```bash
curl -I http://127.0.0.1:8000/Atlas-micro-V6.html
```

If `python3` is unavailable, check alternatives:

```bash
which python3
which python
which php
which busybox
```

If the server works but the browser shows a blank page, try the Micro file first and then check the browser's JavaScript console if one is available.

When asking for help, provide:

1. operating system;
2. CPU architecture;
3. RAM amount;
4. browser name/version;
5. exact file being opened;
6. exact terminal command used;
7. exact error message, if any.

This makes troubleshooting much faster and avoids guessing.

---

## ❤️ Thank you for using Linux Atlas

Explore Linux, compare systems, and choose the system that fits your own hardware and workflow.

> 🇬🇧 Linux Atlas — explore. Compare. Find the system that fits you.
