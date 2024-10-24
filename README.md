**Инструкции**

**Инструкция по установке:** 

1. Клонируем репозиторий
   
Устанавливаем backend:

2. Переходим в терминал и прописываем компанду для перехода в папку sboard-back ( cd 'sboard-back' ) или переходим через интерфейс
   
3. В терминале прописываем команду 'npm i'
   
4. Создаем .env файл и прописываем в нем:

PORT=3001

POSTGRESS_DB_URL=127.0.0.1

POSTGRESS_DB_PORT=5432

POSTGRESS_DB_USER=nest

POSTGRESS_DB_PASSWORD=nest

POSTGRESS_DB_NAME=nest

5. Запустите файл docker-compose.yml (Можно прописать в командной строке 'docker-compose up' или запустить через интерфейс). **Не забудьте перед этим запустить docker engine** 
6. В терминале прописываем команду 'nest start --watch'. Это же действие можно сделать через интерфейс, зайдя в файл package.json в папке 'sboard-back'

**Устанавливаем frontend:**

2. Переходим в терминал и прописываем компанду для перехода в папку sboard-front ( cd 'sboard-front' ) или переходим через интерфейс
   
3. В терминале прописываем команду 'npm i'

4. В терминале прописываем команду 'react-scripts start'. Это же действие можно сделать через интерфейс, зайдя в файл package.json в папке 'sboard-front'

Инструкция по тестированию: 
1. Переходим в браузере по адресу 127.0.0.1:3000 или localhost:3000

2. На экране кнопка "Создать". Нажимаете на неё
   
    2.1. Тест 1. Заполняете заголовок голосования. Нажимая на кнопку "Добавить вариант", добавляете необходимое количество вариантов для голосования. Для создания голосования все поля должны быть заполнены. Для создания запроса необходимо нажать на кнопку "Создать голосование". Если ошибок нет, то голосование создастся и появится в списки всех голосований.
   
    2.2. Тест 2. При создании теста заполните только заголовок, не создавая варианты ответов. Нажмите на кнопку "Создать голосование", система должна уведомить, что вариантов для голосования нет.

4. Нажимая на вариант ответа одного из голосований, прибавляется голос к этому ответу.

5. Если открыть несколько вкладок в браузере и проголосовать в одной из них либо в каждой за какой-то(какие-то) варианты ответов, во всех вкладках должны поменяться количество ответов в определенном голосовании и в определенном ответе (за который вы голосовали)
6. Нажимая на крестик в в правом верхнем углу каждого голосования, можно удалить это голосование.
7. Тестировать backend часть можно через swagger, перейдя по ссылке localhost:3001/swagger или 127.0.0.1:3001/swagger
