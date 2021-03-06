# Отчёт о тестировании приложения "Money Transfer" #
## Тестирование приложения, позволяющего пополнять баланс счета с помощью перевода ##

6.06.2020 было проведено тестирование работы приложения, которое позволяет отображать баланс счета клиента после перевода денежных средств. В результате тестов было выявлено, что данное приложение работает некорретно. Ошибка (скорее всего) кроется в максимально допустимых суммах, которые можно хранить на счете.

## Описание тестов ##
Проводились следующие виды тестирования:
1. Функциональное - чтобы понять, что выполняет программа, а именно: считает и выводит баланс клиента после пополнения.
1. Нефункциональное - чтобы определить на сколько корректно написана программа, работает ли ее главная функция (в данном случае сложение).

Также были проведены тесты эквивалентных значений:

1. В первую очередь проводилось позитивное тестирование с уже указанными данными (2 млрд., 500 млн.). В результате программа выдала неверную сумму.
1. Негативное тестирование с заменой числовых значений на буквенные и символы. Программа ответила ошибкой.
2. Позитиное тестирование с изменением текущего баланса на меньшее значение, чем было указано (меняли на: 500 млн., 1 млрд., 1 млрд. 500 млн.), а так же изменение суммы перевода с увеличением значения (меняли на: 1 млрд., 1 млрд. 500 млн.). Программа выдавала правильные результаты.
3. Тестирование граничных значений с увеличением суммы перевода в 2 раза (меняли на 1 млрд.) при текущем балансе 2 млрд.. В результате программа выдает неверную сумму.

## Результаты ##

80% - успешные тесты;

20% - не успешные тесты.

Выявлены следующие дефекты работы функционала:

1. https://github.com/Lebedeva-Kris/Money-Transfer/issues/1

1. https://github.com/Lebedeva-Kris/Money-Transfer/issues/2


## Общие рекомендации ##
В результате тестирования было выявлено, что проблема кроется в максимальной сумме, которую клиент может хранить на балансе. Поэтому рекомедуется увеличить это значение.