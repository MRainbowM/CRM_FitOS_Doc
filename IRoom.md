[Назад](./API.md)

## Описание интерфейса IRoom

Интерфейс предназначен для работы с методами класса Room

### Реализация интерфейса

+ +Add(Name:string, Equipment:string, Capacity:int,Comment:string) - Добавить помещение;
	* Name - название помещения;
	* Equipment - оборудование помещения;
	* Capacity - вместимость помещения;
	* Comment - комментарий о помещении;
+ +Del(ID : int) – функция удаления помещение (Присвоение статуса «удаленное»);
	* ID - номер помещения в БД;

+ +Save(Name:string, Equipment:string, Capasity:int,Comment:string) – функция сохранения изменений;
	* Name - название помещения;
	* Equipment - оборудование помещения;
	* Capacity - вместимость помещения;
	* Comment - комментарий о помещении;

+ +GetAll() - вывести список всех помещений;

+ +FindRoomByID(ID : int) - поискпо ID;
	* ID - номер помещения в БД;

+ +GetScheduleRoomByTime(ID:int) - показать расписание помещения;
	* ID - номер помещения в БД.

[Назад](./API.md)