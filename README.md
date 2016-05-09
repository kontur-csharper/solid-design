# Блок "Проектирование"

## Задача 1. Polymorphism over Conditionals

Отрефакторите код проекта Conditionals так, чтобы он соответствовал принципам OCP и DIP.

## Задача 2. DI-сontainer

Откройте проект DIContainer

Минимум:
1. Внедрите Ninject container для создания Program. (см. метод Program.Main)

Основная программа:

2. Добавьте команду HelpCommand, печатающую список всех доступных команд (в том числе себя). Для этого придется побороть циклическую зависимость.
3. Сделайте явной зависимость от TextWriter и используйте его, вместо консоли и в командах, и в Program.

Дополнительно:

4. Попробуйте подход Convention over configuration в Ninject. Для этого изучите extension-метод Bind(c => ...) из пространства имен Ninject.Conventions.
5. Биндить что-то на TextWriter — не очень хорошая идея. TextWriter — это слишком общая штука.
Примените идею именованных зависимостей в Ninject (атрибут Named), чтобы избавиться от этой проблемы.

## Задача 3. Mock Framework.

Создайте тест с использованием FakeItEasy на класс Program.
Напишите тесты, проверяющие поведение Program в случаях, когда команда не указана или указана неверно.
Все зависимости Program, в том числе команды подмените на Mock-классы.