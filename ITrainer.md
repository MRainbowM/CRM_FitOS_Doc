[Назад](./API.md)

## Описание интерфейса ITrainer

Интерфейс предназначен для работы с методами класса Trainer

### Реализация интерфейса

+ +GetAll() - выводит список всех тренеров;

+ +FindTrainerByID(ID : int) - поиск тренера по ID;
    * ID -номер пользователя в БД;

+ +Add(FIO:string, Sex:bool,  Qualification:string, Phone:int, DOB:DateTime, Comment:string) - функция добавления тренера в БД;
     * FIO - ФИО тренера;
     * Sex - пол тренера;
     * Qualification - квалификация тренера;
     * Phone - номер телефона тренера;
     * DOB - дата рождения;
     * Comment - комментарий о тренере.

[Назад](./API.md)