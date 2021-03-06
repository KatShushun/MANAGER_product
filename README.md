# Задача №1 - "Менеджер Товаров"
На основании проекта из лекции необходимо реализовать менеджер товаров, который умеет:

Добавлять товары в репозиторий
Искать товары
Что нужно сделать:

Разработайте базовый класс Product, содержащий id, название, стоимость
Разработать два унаследованных от Product класса: Book (с полями название* и автор) и Smartphone (с полями название* и производитель)
Разработайте репозиторий, позволяющий сохранять Product'ы, получать все сохранённые Product'ы и удалять по id
Разработайте менеджера, который умеет добавлять Product'ы в репозиторий и осуществлять поиск по ним
Как осуществлять поиск
У менеджера должен быть метод searchBy(String text), который возвращает массив найденных товаров

Менеджер при переборе всех продуктов, хранящихся в массиве (или в репозитории, если вы в предыдущих ДЗ сделали репозиторий)*, должен для каждого продукта вызывать собственный метод matches, который проверяет, соответствует ли продукт поисковому запросу.

Примечание*: если вы сделали репозиторий, то пусть менеджер забирает из репозитория все товары и сам уже по ним ищет.

Проверку соответствия проводится с помощью instanceof - для книги по полям название и автор, для смартфона по полям название и производитель.

Требования к проекту:

Создайте ветку (не делайте ДЗ в master!)
Подключите плагин Surefire так, чтобы сборка падала в случае отсутсвия тестов
Подключите плагин JaCoCo в режиме генерации отчётов (обрушать сборку по покрытию не нужно)
Реализуйте нужные классы и методы
Напишите автотесты на метод поиска (только на метод поиска в менеджере), добившись 100% покрытия по branch'ам* (вспомните, что мы говорили про тестирование методов, возвращающих набор значений)
Подключите CI на базе Github Actions и выложите всё на Github
Итого: у вас должен быть репозиторий на GitHub, в котором расположен ваш Java-код в ветке (в master должен быть только pom.xml).
