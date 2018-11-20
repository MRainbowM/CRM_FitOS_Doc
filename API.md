**Лабораторная работа № 6**

**Задание:** Определить интерфейсы классов, разработать диаграммы компонентов и размещения UML по проекту АИС.

 

Рисунок 1 Диаграмма размещения

 
На диаграмме размещения изображены узлы выполнения программных компонентов, а также объектов. Показано, что клиентское приложение, установленное на компьютере пользователя, взаимодействует с сервером, который содержит в себе базу данных.

Рисунок 2 Диаграмма компонентов

На данной диаграмме изображены все компоненты: клиентское приложение, работники, клиенты, услуги, расписание, помещения, карты, тарифы, платежи, пользователи. Эти компоненты взаимодействуют друг с другом с помощью интерфейсов.

 
Рисунок 3 Диаграмма интерфейсов

**IUser**

+ Del(ID : int) - функция удаления пользователя;

+ Validation(Login:string, Password:string) - функция проверки логина и пароля, вводимых пользователем.

**IClient**

Данный класс наследует все операции классаUser, содержит в себе атрибуты: FIO, Sex, Haight, Weight, Health (состояние здоровья), Phone, DOB (дата рождения), Comment (комментарий), State (статус: удаленный или нет).

+ Add(FIO:string, Sex:bool, Height:int, Weight:int, Health:int, Phone:int, DOB:DateTime, Comment:string) – функциядобавленияпользователявБД;

+ Save(FIO:string, Sex:bool, Height:int, Weight:int, Health:int, Phone:int, DOB:DateTime, Comment:string) – функциясохраненияизменений;

+ GetAll() - выводит список всех клиентов;

+ FindClientByID(ID : int)  - поиск клиента по ID;

**ITrainer**

+ GetAll() - выводит список всех тренеров;

+ FindTrainerByID(ID : int) - поиск тренера по ID;

+ Add(FIO:string, Sex:bool,  Qualification:string, Phone:int, DOB:DateTime, Comment:string) - функциядобавлениятренеравБД.

**IPhotos**

Данный класс работает с фотографиями. Он содержит в себе атрибуты: ID, URL, State (статус: удаленный или нет).

+ Add() – функция добавления фото в БД;

+Del(ID : int) – функция удаления фото (Присвоение статуса «удаленный»).

**IService**

Данный класс позволяет работать со списком услуг. Класс содержит в себе атрибуты: ID, Name, Cost, Room, Comment, State (статус: удаленная услуга или нет).

+ Add(Name:string, Cost:int, Comment:string)– функциядобавленияуслугивБД;

+ Del(ID : int) – функция удаления услуги (Присвоение статуса «удаленная»);

+ Save(Name:string, Cost:int, Comment:string) – функциясохраненияизменений;

+ GetAll() - вывести список всех услуг;

+ GetTrainers(ID\_Servise : int) - вывести всех тренеров услуги;

+ FindServiceByID(ID : int) - поискуслугипо ID;

+ GetBalanceService(IDCard : int) - показать баланс карты, то есть количество услуги на карте;

+ GetBalanceFrost(IDCard : int) - показать количество дней заморозки.

**ITariff**

+ Add(Name:string, Duration:int, TotalCost:float, StartDate:DateTime, DateRemoved:DateTime) - Добавитьновыйтариф;

+ GetServices() - показать услуги по тарифу;

+ Del(ID : int) – функция удаления тарифа (Присвоение статуса «удаленный»);

+ Save(Name:string, Duration:int, TotalCost:float, StartDate:DateTime, DateRemoved:DateTime) – функциясохраненияизменений;

+ GetAll() - вывести список всех тарифов;

+ FindTarrifsByID(ID : int) - найти тариф по ID;

**IRoom**

+ Add(Name:string, Equipment:string,

Capasity:int,Comment:string) - Добавитьпомещение;

+ Del(ID : int) – функция удаления помещение (Присвоение статуса «удаленное»);

+ Save(Name:string, Equipment:string,

Capasity:int,Comment:string) – функция сохранения изменений;

+ GetAll() - вывести список всех помещений;

+ FindRoomByID(ID : int) - поискпо ID;

+ GetScheduleRoomByTime(ID:int) - показать расписание помещения

**ICard**

+ Add(IDTariff: int) - Добавить карту;

+ Del(ID : int) – функция удаления карты (Присвоение статуса «удаленная»);

+ Save(IDTariff: int) – функция сохранения изменений;

+ GetAll() - вывести список всех карт;

+ FindCardByID(ID : int) - поискпо ID;

+ ShowBalance(Card : FindCardByID(ID : int)) - показатьостатокуслугпокарте;

+ AddVisit(ID\_Card : int, ID\_Service : int) - добавитьпосещение;

+ DelVisit(ID\_Card : int, ID\_Service : int) - удалитьпосещение;

+ FrostCard(IDCard : int, StartDate : DateTime, EndDate : DateTime) - заморозкакарты

**ISchedule**

+ Add(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) - Добавитьзапись;

+ Del(ID : int) – функция удаления запись (Присвоение статуса «удаленная»);

+ Save(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) – функциясохраненияизменений;

+ AddFrost( StartDate : DateTime, EndDate : DateTime, IDCard:int) - заморозитькарту;

+ GetAll() - вывести список всех записей;

**IPayment**

+ Add(IDCard:int, Date:DateTime, Amount:int) - Добавитьплатеж;

+ Del(ID : int) – функция удаления платежа из БД;

+ GetAll() - вывести список всех платежей.



