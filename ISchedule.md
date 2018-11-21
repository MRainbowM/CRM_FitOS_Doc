[Назад](./API.md)

## Описание интерфейса ISchedule

Интерфейс предназначен для работы с методами класса Schedule

### Реализация интерфейса

+ +Add(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) - Добавитьзапись;
	* Trainer - экземпляр класса Trainer;
	* Card - экземпляр класса Trainer;
	* Service - экземпляр класса Service;
	* Room - экземпляр класса Room;
	* Date - дата занятия;

+ +Del(ID : int) – функция удаления запись (Присвоение статуса «удаленная»);
	* ID - номер записи в БД;

+ +Save(Trainer : Trainer, Card : Card, Service : Service, Room : Room, Date : DateTime) – функция сохранения изменений;
	* Trainer - экземпляр класса Trainer;
	* Card - экземпляр класса Trainer;
	* Service - экземпляр класса Service;
	* Room - экземпляр класса Room;
	* Date - дата занятия;

+ +AddFrost( StartDate : DateTime, EndDate : DateTime, IDCard:int) - заморозить карту;
	* ID - номер карты в БД;
	* StartDate - дата начала заморозки;
	* EndDate - дата разморозки;

+ +GetAll() - вывести список всех записей.

[Назад](./API.md)