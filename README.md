# Roadmap тестировщика

## Начало

- [x] Регистрация рабочей почты.
  
  *Она понадобится для регистрации на различных сайтах и программах + для резюме*
  
  > **Пример:**
  > 
  > Имя и Фамилия: Fedor Emelianenko
  > 
  > `femelianenko@gmail.com` (первая буква имени + фамилия) 
  > `fedor.emelianenko@gmail.com`

- [ ] Начать привыкать к английским словам и терминам и начать их использовать при объяснении чего-то
- [ ] Начать привыкать к поиску информации в интернете (**важно**)
- [ ] По тихоньку начинать запоминать сайты, на которых можно найти информацию (расскажу в голосовом)

## Темы

### Теория

- [ ] **Json** и **XML** форматы и их отличие
- [ ] **Клиент-серверная архитектура** приложений: принцип работы и где используется
  - [ ] Общие принципы работы **VCS**
  - [ ] Что такое **Git**
  - [ ] Что такое **репозиторий** (repository)
  - [ ] Что такое **комит** (commit)
  - [ ] Что такое **ветки** (в репозитории)
  - [ ] Что такое **Github** и какие есть еще сервисы
- [ ] Базы данных
  - [ ] Что такое **SQL** и **NoSQL** базы данных, а также чем они отличаются
  - [ ] Команды **SELECT**, **JOIN** и команды для сортировки
- [ ] Тест кейсы
  - [ ] Что это и как их писать (тест кейсы) 
  - [ ] Где можно их писать?
- [ ] Основные **HTTP** методы
  - [ ] Какие методы бывают и для чего они нужны
- [ ] Что такое логи и для чего они нужны
- [ ] Автоматизированные тестирование
  - [ ] Что это такое и как проводится
  - [ ] Найти программы, сервисы или системы для автоматизированного тестирования 
- [ ] Совместимость браузеров и сайтов

### Практика

- [ ] Chrome dev tool
- [ ] Git и GitHub
- [ ] Написание тест кейсов для приложения
- [ ] Тестирование API с помощью Postman

## Полезная информация

**HTTP методы**

[Небольшая статья](https://developer.mozilla.org/ru/docs/Glossary/Idempotent) - рекомендую прочитать, могут за это на собеседовании спросить. 

**Статьи**

https://www.uplab.ru/blog/automated-testing-of-website/ - по ручному и автомтизированному тестированию
https://www.youtube.com/watch?v=QPpaTBDDLS8 - можно посмотреть этот или поъожий стрим, там есть пример тестирования
https://habr.com/ru/post/505956/ - дополнительно можно изучить эту статью, что там написано
https://www.internet-technologies.ru/articles/rukovodstvo-po-testirovaniyu-saytov.html - статья по тестированию

**Json**

Вот API (если почитаешь что это такое, то будет круто), на примере которого можно посмотреть как работает клиент-серверное приложение, как отправляются запросы и как выглядит JSON.

https://developers.themoviedb.org/3 - это документация к API, но там можно протестировать любой запрос и ничего не нужно устанавливать. Позже попробуем с помощью Postman потестировать эти же запросы. (Это уже будет в практике)

Чтобы потестить запросы нужен ключ - `ee1307d98eff1fc83e1c926686859021` (это api_key)
На сайте выбираешь слева, например, `Movies` > `Get Details`, после чего откроется страница с запросом. Там описание, какие параметры и поля принимает запрос и пример Json ответа (Нужно нажать кнопку `Example`). 
Чтобы попробовать отправить запрос, нужно выбрать `Try it out`, ввести api_key и например movie_id = `245891`, должен прийти ответ с информацией о фильме Джон Уик.
По аналогии можешь попробовать другие запросы потестировать. 

**Git**

Для выполнения команд, нужно убедится что ты находишься в папке репозитория, в корне.

```shell
# Выведет информацию о параметрах и атрибутах
# --help можно применять практически для любой команды в консоли, чтобы получить информацию
$ git --help

# Добавит все содержимое репозитория в индекс (нужно чтобы зафиксировать их перед комитом) 
$ git add .

# Покажет список измененных/добавленных/удаленных файлов
# Если зеленый, значит добавлен в индекс, красный значит, что файл не находится в индексе и при комите не будет зафиксирован
$ git status

# Команда для фиксации изменений (создание комита)
# Если не указывать никакие параметры, то откроет редактор, в котором тебе нужно будет написать Название и Описание, сохранить и закрыть, после чего будет создан комит
$ git commit

# Быстрый способ создания комита без описания
$ git commit -m "Название комита "

# Получает обновления с удаленного репозитория, то есть с сервера (например с GitHub)
$ git pull origin

# Отправит обновления на сервер
$ git push origin
```

> Если интересно как писать правильно **комиты**, то вот [хорошая статья](https://habr.com/ru/post/416887/).

**Базы данных**

[Статья](https://mcs.mail.ru/blog/sravnenie-sql-i-nosql-kak-vybrat-sistemu-hraneniya-dannyh) про сравнение SQL и NoSQL.
Рекомендую поискать как выглядит NoSQL базы данных (можно на YouTube глянуть).
