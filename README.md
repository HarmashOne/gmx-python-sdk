# gmx-python-sdk (Customized)

**gmx-python-sdk (Customized)** — это кастомизированная версия библиотеки для работы с протоколом GMX на сети Arbitrum и Ethereum. Эта версия включает в себя специфические изменения и исправления, предназначенные для личного использования или по заказу. Основные улучшения включают исправления и улучшения для работы с депозитами и выводами в GMX v2 пулах, что обеспечивает более надежную и точную работу с этими функциями.

## Основные функции

- **Исправленные депозиты**: Обновленный функционал для работы с депозитами в GMX v2 пулах.
**Исправлено**
- Правильная передача кортеджа данных в контракт. Был изменен get_estimated_deposit_amount_out в файле gmx_utils.py
  
- **Исправленные выводы**: Улучшенная обработка операций вывода из GMX v2 пула.
**Исправлено**
- Правильное формирование и отправка данных в контракт, есть проблема с передаваемым swapPricingType(uint8) в контракте https://arbiscan.io/address/0xa19fa3f0d8e7b7a8963420de504b624167e709b2 ф-ции _executeWithdrawal (0x08cfdf3d), передаваемое значение имеется в файле gmx_utils.py в функции get_estimated_withdrawal_amount_out.
- Поправлена функция determine_swap_paths(self) в файлe withdraw.py. В удачных транзакциях на вывод Swap path оставался незаполненным.

## Установка

