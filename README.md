﻿# Отчёт о тестировании <KeyValidator>
## Краткое описание
<23.02.2020> - <23.02.2020> было проведено тестирование приложения <KeyValidator>.

На тестирование затрачено: <1 h>

**В результате тестирования выявлены следующие дефекты:**

1. Не все валидные ключи оказались валидными
1. На все невалидные ключи оказались невалидными

## шаги:
* скачать  KeyValidator.class
* распаковать файл
* открыть через GitBush
* запустить спомощью команды java KeyValidator 00000000-0000-0000-0000-000000000000 00000000-0000-0000-0000-000000000001
* проверить все валидные и невалидные ключи той же командой, указав номера ключей

1. Ожидаемый результат при введении валидных ключей 
 Result for 00000000-0000-0000-0000-000000000000: OK


 Фактический результат при введении четвертого из пяти валидных ключей (387eedc6-12e9-3b32-9881-63b6b5e85317) оказался невалидным:
 $ java KeyValidator 387eedc6-12e9-3b32-9881-63b6b5e85317
Result for 387eedc6-12e9-3b32-9881-63b6b5e85317: FAIL
1.  Ожидаемый результат при введении невалидных ключей 
 Result for 00000000-0000-0000-0000-000000000000: FAIL

 Фактический результат при введении пятого из пяти невалидных ключей (2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1) оказался валидным:
 $ java KeyValidator 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1
Result for 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1: OK

**СКРИН** 

(https://drive.google.com/file/d/1tzcmEDQnpPFMaVeVBut5f-yVn9DIqtn2/view?usp=sharing)

*Тестирование производилось в следующем окружении:*

<Windows 7>
<openjdk version "11.0.6" 2020-01-14>

