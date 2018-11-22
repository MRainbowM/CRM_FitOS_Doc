[Назад](./API.md)

## Описание интерфейса ISchedule

Интерфейс предназначен для работы с методами класса Schedule

### Реализация интерфейса

+ **+Add**(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) - Добавитьзапись;
	* Trainer - экземпляр класса Trainer;
	* Card - экземпляр класса Trainer;
	* Service - экземпляр класса Service;
	* Room - экземпляр класса Room;
	* Date - дата занятия;

+ **+Del**(ID : int) – функция удаления запись (Присвоение статуса «удаленная»);
	* ID - номер записи в БД;

+ **+Save**(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) – функция сохранения изменений;
	* Trainer - экземпляр класса Trainer;
	* Card - экземпляр класса Trainer;
	* Service - экземпляр класса Service;
	* Room - экземпляр класса Room;
	* Date - дата занятия;

+ **+AddFrost**( StartDate : DateTime, EndDate : DateTime, IDCard:int) - заморозить карту;
	* ID - номер карты в БД;
	* StartDate - дата начала заморозки;
	* EndDate - дата разморозки;

+ **+GetAll()** - вывести список всех записей.

## Описание класса Schedule

Класс позволяет работать с информацией о помещениях.

### Атрибуты класса Schedule

* **ID** : Bool - номер помещения в БД;
* **Trainer** : Trainer - экземпляр класса Trainer;
* **Card** : Card - экземпляр класса Trainer;
* **Service** : Service - экземпляр класса Service;
* **Room** : Room - экземпляр класса Room;
* **Date** : DateTime - дата занятия;
* **StartDate** : DateTime - дата начала заморозки (только для услуги заморозки карты);
* **EndDate** : DateTime - дата окончания заморозки (только для услуги заморозки карты).

[Назад](./API.md)