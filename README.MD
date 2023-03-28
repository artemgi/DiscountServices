# **Сервис по работе с товарами**

**Описание:**
Реализация тестового задания по [постановке](Task.md). Данное приложение представляет собой сервис для работы с клиентами, товарами и фактами 
продажи, также в нем есть случайная генерация скидок. Сервис имеет два интерфейса: SOAP и RESTful.

**Используемые технологии:**
* Java 11
* Spring boot 2.7.1
* PostgresSQL
* JUnit 5`
* Docker
* Apache CXF
* Liquibase

**Запуск**

`docker-compose up -d --build`

**Как использовать**

1. список клиентов (все атрибуты). [rest](http://localhost:8080/clients) / [wsdl](http://localhost:8080/Service/Client?wsdl)(getClients)
2. изменение индивидуальных скидок клиента (входные параметры: идентификатор, скидка 1, скидка 2).
 [rest](http://localhost:8080/clients/1?discount1=8&discount2=9)
3. список товаров (идентификатор, наименование, цена). [rest](http://localhost:8080/products)
4. получение дополнительной информации о товаре. [rest](http://localhost:8080/products/2)
5. Запрос итоговой стоимости [rest](http://localhost:8080/products/totalCost?1=3&2=2)
6. Регистрация продажи [rest](http://localhost:8080/sales/registration?1=3&2=2&totalCost=94000)
7. Оценка товара
8. Получение статистики