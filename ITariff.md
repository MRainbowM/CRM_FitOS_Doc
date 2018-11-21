[Назад](./API.md)

## Описание интерфейса ITariff

Интерфейс предназначен для работы с методами класса Tariff

### Реализация интерфейса

+ +Add(Name:string, Duration:int, TotalCost:float, StartDate:DateTime, DateRemoved:DateTime) - Добавить новый тариф;
	* Name - наименование тарифа;
	* Duration - длительность тарифа;
	* TotalCost - стоимость тарифа;
	* StartDate - дата начала продаж тарифа;
	* DateRemoved - дата окончания продаж тарифа;

+ +GetServices(ID : int) - показать услуги по тарифу;
	* ID - номер тарифа в БД;

+ +Del(ID : int) – функция удаления тарифа (Присвоение статуса «удаленный»);
	* ID - номер тарифа в БД;

+ +Save(Name:string, Duration:int, TotalCost:float, StartDate:DateTime, DateRemoved:DateTime) – функция сохранения изменений;
	* Name - наименование тарифа;
	* Duration - длительность тарифа;
	* TotalCost - стоимость тарифа;
	* StartDate - дата начала продаж тарифа;
	* DateRemoved - дата окончания продаж тарифа.

+ +GetAll() - вывести список всех тарифов;

+ +FindTarrifsByID(ID : int) - найти тариф по ID;
	* ID - номер тарифа в БД.

[Назад](./API.md)