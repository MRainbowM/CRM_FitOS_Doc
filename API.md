**Лабораторная работа № 7**

*Задание*: Разработать документацию на API проектируемой программы в документе(-ах) формата MarkDown или его расширении GitHub-Flavored Markdown. Создать проект для программы на GitHub и выложить документацию в папку docs проекта. 

## Диаграмма размещения

![](./images/1.png "img1")
 
*Рисунок 1 Диаграмма размещения*

 
На диаграмме размещения изображены узлы выполнения программных компонентов, а также объектов. Показано, что клиентское приложение, установленное на компьютере пользователя, взаимодействует с сервером, который содержит в себе базу данных.

## Диаграмма компонентов

![](./images/2.png "img2")

*Рисунок 2 Диаграмма компонентов*

На данной диаграмме изображены все компоненты: клиентское приложение, работники, клиенты, услуги, расписание, помещения, карты, тарифы, платежи, пользователи. Эти компоненты взаимодействуют друг с другом с помощью интерфейсов.

## Диаграмма интерфейсов

![](./images/3.png "img3")

*Рисунок 3 Диаграмма интерфейсов*

*Список интерфейсов:*

+ [IUser](#IUser);
+ [IClient](#IClient);
+ [ITrainer](#ITrainer);
+ [IPhoto](#IPhoto);
+ [IService](#IService);
+ [ITariff](#ITariff);
+ [IRoom](#IRoom);
+ [ICard](#ICard);
+ [ISchedule](#ISchedule);
+ [IPayment](#IPayment);

<a name="IUser">[**IUser**](./IUser.md)</a>
-----

+ +Del(ID : int) : bool - функция удаления пользователя;

+ +Validation(Login:string, Password:string) : bool - функция проверки логина и пароля, вводимых пользователем.

<a name="IClient">[**IClient**](./IClient.md)</a>
-----

+ +Add(FIO:string, Sex:bool, Height:int, Weight:int, Health:int, Phone:int, DOB:DateTime, Comment:string): int – функция добавления пользователя в БД;

+ +Save(FIO:string, Sex:bool, Height:int, Weight:int, Health:int, Phone:int, DOB:DateTime, Comment:string) : bool – функция сохранения изменений;

+ +GetAll() : List<Client> - выводит список всех клиентов;

+ +FindClientByID(ID : int) : Client - поиск клиента по ID;

<a name="ITrainer">[**ITrainer**](./ITrainer.md)</a>
-----

+ +GetAll() : List<Trainer> - выводит список всех тренеров;

+ +FindTrainerByID(ID : int) : Trainer - поиск тренера по ID;

+ +Add(FIO:string, Sex:bool,  Qualification:string, Phone:int, DOB:DateTime, Comment:string) : int - функция добавления тренера в БД.

<a name="IPhoto">[**IPhoto**](./IPhoto.md)</a>
-----

+ +Add(URL : string) : int – функция добавления фото в БД;

+ +Del(ID : int) : bool – функция удаления фото (Присвоение статуса «удаленный»).

<a name="IService">[**IService**](./IService.md)</a>
-----

+ +Add(Name:string, Cost:int, Comment:string) : int – функция добавления услуги в БД;

+ +Del(ID : int) : bool – функция удаления услуги (Присвоение статуса «удаленная»);

+ +Save(Name:string, Cost:int, Comment:string) : bool – функциясохраненияизменений;

+ +GetAll() : List<Service> - вывести список всех услуг;

+ +GetTrainers(IDServise : int) : List<Trainer> - вывести всех тренеров услуги;

+ +FindServiceByID(ID : int) : Service - поискуслугипо ID;

+ +GetBalanceService(IDCard : int) : Dictionary<string, int> - показать баланс карты, то есть количество услуги на карте;

+ +GetBalanceFrost(IDCard : int) :  Dictionary<string, int> - показать количество дней заморозки.

<a name="ITariff">[**ITariff**](./ITariff.md)</a>
-----

+ +Add(Name:string, Duration:int, TotalCost:float, StartDate:DateTime, DateRemoved:DateTime) : int - Добавить новый тариф;

+ +GetServices(ID : int) : List<Service> - показать услуги по тарифу;

+ +Del(ID : int) : bool – функция удаления тарифа (Присвоение статуса «удаленный»);

+ +Save(Name:string, Duration:int, TotalCost:float, StartDate:DateTime, DateRemoved:DateTime) : bool – функция сохранения изменений;

+ +GetAll(ID : int) : List<Tariff> - вывести список всех тарифов;

+ +FindTarrifsByID(ID : int) - найти тариф по ID;

+ +AddServiceInTariff(IDService : int, IDTariff : int, Periodicity : int, Amount : int) : bool - добавить услугу в тариф.

<a name="IRoom">[**IRoom**](./IRoom.md)</a>
-----

+ +Add(Name:string, Equipment:string, Capacity:int,Comment:string) : int - Добавить помещение;

+ +Del(ID : int) : bool – функция удаления помещение (Присвоение статуса «удаленное»);

+ +Save(Name:string, Equipment:string, Capasity:int,Comment:string) : bool – функция сохранения изменений;

+ +GetAll() : List<Room> - вывести список всех помещений;

+ +FindRoomByID(ID : int) : Room - поискпо ID;

+ +GetScheduleRoomByTime(ID:int) : Dictionary<DateTIme,string> - показать расписание помещения

<a name="ICard">[**ICard**](./ICard.md)</a>
-----
+ +Add(IDTariff: int, IDClient: int) : int - Добавить карту;

+ +Del(ID : int) : bool – функция удаления карты (Присвоение статуса «удаленная»);

+ +Save(IDTariff: int) : bool – функция сохранения изменений;

+ +GetAll() : List<Card> - вывести список всех карт;

+ +FindCardByID(ID : int) : Card - поискпо ID;

+ +AddVisit(IDCard : int, IDService : int) : int - добавить посещение;

+ +DelVisit(IDCard : int, IDService : int) : bool - удалить посещение;

+ +FrostCard(IDCard : int, StartDate : DateTime, EndDate : DateTime) : bool - заморозка карты

<a name="ISchedule">[**ISchedule**](./ISchedule.md)</a>
-----

+ +Add(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) : int - Добавитьзапись;

+ +Del(ID : int) : bool – функция удаления запись (Присвоение статуса «удаленная»);

+ +Save(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) : bool – функция сохранения изменений;

+ +AddFrost( StartDate : DateTime, EndDate : DateTime, IDCard:int) : bool - заморозить карту;

+ +GetAll() : List<Schedule> - вывести список всех записей;

<a name="IPayment">[**IPayment**](./IPayment.md)</a>
-----

+ +Add(IDClient:int, Date:DateTime, Amount:int) : int - Добавить платеж;

+ +Del(ID : int) : bool – функция удаления платежа из БД;

+ +GetAll() : List<Payments> - вывести список всех платежей.



