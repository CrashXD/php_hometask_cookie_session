# Задача

## Cookie 1

1. Создайте файлы:
   - `introduce.php`
   - `hello.php`
2. В `introduce.php` добавьте форму с полем `name` и подписью **"Ваше имя"**:
   - при отправке формы сохраняйте введенное значение в cookie с названием `username`
   - если cookie `username` существует - выводите её значение в поле
3. В `hello.php` выведите текст **"Добро пожаловать, "** и значение сохраненное в cookie `username`:
   - если cookie `username` не существует - выведите "Мы еще не знакомы" и ссылку на `introduce.php`
4. Удалите через консоль разработчика cookie `username` и проверьте работу скриптов
5. Создайте через консоль разработчика cookie `username` с любым значением и проверьте работу скриптов
6. Измените через консоль разработчика cookie `username` и проверьте работу скриптов

## Cookie 2

1. Создайте файлы:
   - `cookie.php`
   - `cookie_update.php`
   - `cookie_clear.php`
2. В `cookie_update.php` создайте cookie с названием `update_at` и запишите в неё текущую метку времени, используя функцию `time()`:
   - добавьте проверку: если cookie `update_at` уже установлена - заменить её значение, а если cookie нет, то создавать её
3. В `cookie.php` выведите текст **"Последнее обновление:"** и время в секундах:
   - добавить проверку на существование cookie `update_at`
   - если cookie установлена - выведите рядом с текстом разницу между текущей меткой времени и значением cookie, с добавлением **"секунд назад"**
   - если cookie отсутствует, выведите текст **"больше часа назад"**
4. В `cookie_update.php` измените установку cookie `update_at` так, чтобы устанавливать её со сроком только на один час
5. В `cookie_update.php` добавьте редирект на `cookie.php` в конце скрипта
6. В `cookie_clear.php` удаляйте cookie `update_at`, если она установлена
7. В `cookie_clear.php` добавьте редирект на `cookie.php` в конце скрипта
8. В `cookie.php` добавьте ссылки на `cookie_update.php` и `cookie_clear.php`:
   - в зависимости от установленного cookie `update_at`, выводите ссылку на обновление или на сброс

## Сессии 1

1. Создайте файлы:
   - `order.php`
   - `check.php`
2. В начале каждого файла запустите сессию, чтобы иметь доступ к полям сессии
3. В `order.php` добавьте форму с полем `card` и подписью **"Номер карты"**:
   - при отправке формы сохраняйте введенное значение в сессии с названием `cardnumber`
   - если в сессии есть `cardnumber` - выводите его значение в поле
4. В `check.php` выведите текст **"Номер вашей карты "** и значение сохраненное в сессии в поле `cardnumber`:
   - если поля `cardnumber` не существует - выведите **"Вы еще не ввели номер карты"** и ссылку на `order.php`
5. Просмотрите через консоль разработчика и запишите куда-нибудь значение cookie `PHPSESSID`
6. Удалите через консоль разработчика cookie `PHPSESSID` и проверьте работу скриптов
7. Создайте через консоль разработчика cookie `PHPSESSID` или измените значение существующей на то значение, которое записали в пункте 5 и проверьте работу скриптов

## Сессии 2

1. Создайте файлы:
   - `session.php`
   - `session_login.php`
   - `session_logout.php`
2. В начале каждого файла запустите сессию, чтобы иметь доступ к полям сессии
3. В `session_login.php` создайте поле сессии с названием `login_at` и запишите в него текущую метку времени, используя функцию `time()`:
   - добавьте проверку: если в сессии поле `login_at` уже установлено - ничего не делать, а если поля нет, то создавать его
4. В `session.php` выведите текст **"Время входа:"** и время в секундах:
   - добавить проверку на существование поля `login_at` в сессии
   - если поле установлено - выведите рядом с текстом разницу между текущей меткой времени и значением поля сессии, с добавлением **"секунд назад"**
   - если поле отсутствует, выведите **"Вход не произведен"**
5. В `session_login.php` добавьте редирект на `session.php` в конце скрипта
6. В `session_logout.php` завершайте сессию
7. В `session_logout.php` добавьте редирект на `session.php` в конце скрипта
8. В `session.php` добавьте ссылки на `session_login.php` и `session_logout.php`:
   - в зависимости от установленного поля `login_at` в сессии, выводите ссылку на вход или на выход
