[Назад](./API.md)

## Описание интерфейса IClient

Интерфейс предназначен для работы с методами класса Client

### Реализация интерфейса

+ +Add(FIO:string, Sex:bool, Height:int, Weight:int, Health:int, Phone:int, DOB:DateTime, Comment:string) – функция добавления пользователя в БД;
    * FIO - ФИО клиента;
    * Sex - пол клиента;
    * Height - рост клиента;
    * Weight - вес клиента;
    * Health - комментарий о здоровье клинета;
    * Phone - номер телефона клиента;
    * DOB - Дата рождения клиента;
    * Comment - общий комментарий о клиенте;

+ +Save(FIO:string, Sex:bool, Height:int, Weight:int, Health:int, Phone:int, DOB:DateTime, Comment:string) – функция сохранения изменений;
    * FIO - ФИО клиента;
    * Sex - пол клиента;
    * Height - рост клиента;
    * Weight - вес клиента;
    * Health - комментарий о здоровье клинета;
    * Phone - номер телефона клиента;
    * DOB - Дата рождения клиента;
    * Comment - общий комментарий о клиенте;

+ +GetAll() - выводит список всех клиентов;

+ +FindClientByID(ID : int)  - поиск клиента по ID;
    * ID - номер клиента в БД.