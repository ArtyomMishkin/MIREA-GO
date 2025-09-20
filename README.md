# Практическое задание 1

## ЭФМО-02-25 Мишкин Артём Дмитриевич
---
# Информация о проекте

Helloapi - Минимальный HTTP-сервис на Go. Сервис предоставляет три эндпоинта и возвращает текстовые и JSON-ответы.

# Цели и задания практической работы
Цель : Развернуть рабочее окружение Go на Windows, создать минимальный HTTP-сервис на net/http, подключить и использовать внешнюю зависимость, собрать и проверить приложение

Задания :
-    Установить Go и Git, проверить версии.
-    Инициализировать модуль Go в новом проекте.
-    Релизовать HTTP-сервер с маршрутами /hello (текст) и /user (JSON).
-	Подключить внешнюю библиотеку (генерация UUID) и использовать её в /user.
-	Запустить и проверить ответы curl/браузером.
-	Собрать бинарник .exe и подготовить README и отчёт.

# Команды запуска/сборки
Для запуска Helloapi нужно выполнить 4 шага:
## 1) Клонировать данный репозиторий в удобную для вас папку:
```Powershell
git clone https://github.com/ArtyomMishkin/MIREA-GO
```
## 2) Перейти в папку helloapi:
```Powershell
cd helloapi
```
## 3) Загрузка зависимостей:
```Powershell
go mod tidy
```
## 4) Команда запуска
```Powershell
go run ./cmd/server
```

Порт по умолчанию будет 8080, его можно сменить. (см. Примечания по конфигурации)

## Команда сборки
Для сборки бинарника и запуска .exe файла используются данные программы
<img width="611" height="44" alt="image" src="https://github.com/user-attachments/assets/5954bcda-fbe5-47a7-8e9c-6091f59d4cff" />

# Примечания по конфигурации и требования

Для запуска требуется:

Go: версия 1.25.1

Git: версия 2.38.1

<img width="758" height="152" alt="image" src="https://github.com/user-attachments/assets/1c3a1438-4760-4dab-9f36-43aabf1c940e" />


Порт сервера можно изменить через переменную окружения APP_PORT(если её не использовать, то будет использоваться порт 8080)

Команда для PowerShell:
```Powershell
$env:APP_PORT="8081"
```

Результат после изменения:

<img width="481" height="70" alt="image" src="https://github.com/user-attachments/assets/8ce75a78-acf1-425c-96b8-05d9c2a0d4ef" />

# Отчётные материалы

## Скриншот go version

<img width="758" height="152" alt="image" src="https://github.com/user-attachments/assets/ec19e5bf-1031-499b-a28d-a8f170db8dfe" />

## Скриншоты эндпоинтов на порте 

### Эндпоинт /hello

```Powershell
curl http://localhost:8081/hello
```

<img width="901" height="328" alt="image" src="https://github.com/user-attachments/assets/d368ad46-76a5-424d-ba5f-14b31b13363f" />

### Эндпоинт /user

```Powershell
curl http://localhost:8081/user
```

<img width="901" height="377" alt="image" src="https://github.com/user-attachments/assets/8fde7b1f-221d-4d16-a97b-b12381a72732" />

### Эндпоинт /health(дополнительный пункт)

```Powershell
curl http://localhost:8081/health
```

<img width="901" height="366" alt="image" src="https://github.com/user-attachments/assets/ac482412-9e5b-42aa-be16-1fdaa5002949" />






