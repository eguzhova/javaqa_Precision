### Отчёт о тестировании Precision

#### Краткое описание
1 апреля 2021 было проведено функциональное тестирование модуля расчета размера бонуса для новых клиентов  Precision

На тестирование затрачено: 2 часа

В результате тестирования выявлены следующие дефекты:
* [Ошибка вычисления суммарного бонуса для новых клиентов](https://github.com/eguzhova/javaqa_Precision/issues/1)

#### Описание процесса тестирования
В процессе тестирования использовался тестовый сценарий:

1. Создать проект в IntelliJ IDEA с кодом
```java
public class Main {

    public static void main(String[] args) {
        int currentBalance = 2_000_000_000;
        int transferAmount =  500_000_000;
        int balanceAfterTransfer = currentBalance + transferAmount;
        System.out.println("Баланс после перевода:"+balanceAfterTransfer);
    }
}
```
2. Запустить код на исполнение
2. Оценить правильность результата

**Тестовые данные:**
1. Обычный размер бонуса: 0.3
1. Бонус для новых клиентов: 0.6

#### Тестирование производилось в следующем окружении:
* MacOS 11.2.3 (20D91)
* openjdk version "11.0.10" 2021-01-19
* IntelliJ IDEA Community Edition "2020.3.3"