# Библиотека для платы AVR Game board
Плата **AVR Game board** это Arduino совместимое устройство на микроконтроллере ATmega328 в форм-факторе игровой консоли. Плата разработана для обучения программированию игровых сценариев. Программирование платы осуществляется при помощи Arduino IDE и специализированной библиотеки. Библиотека поддерживает все основные функции по работе с железом, при использовании библиотеки написание программного кода полностью сосредотачивается на логике игрового сценария, визуализации сцены.

Для формирования игрового сценария плата **AVR Game board** предоставляет следующие элементы:
- основной дисплей из светодиодной матрицы размером 8x16 точек;
- трехсимвольный семисегментный индикатор;
- 6 кнопок управления, включа четыре кнопки направления, кнопка FIRE, кнопка RETURN;
- зуммер для воспроизведения звуков.

Управление всеми перечисленными элементами отражено в библиотеке для Arduino IDE. 
Светодиодная матрица и семисегментный индикатор объединены в единую систему формирования изображения. Для формирования изображения используются два массива байтов. Формирование изображения сводится к заполнению этих массивов необходимыми данными с последующим вызовом функции **show**, которая отображает эти данные на дисплеях. Поддерживается 16 градаций яркости отдельно для светодиодной матрицы и семисегментного индикатора.
Библиотека постоянно опрашивает состояние кнопок и производит фильтрацию от дребезга контактов. В вашем сценарии вам достаточно выполнить запрос к библиотеке что бы определить состояние кнопок. Вы можете использовать один из двух режимов предоставления информации о нажатии кнопок: текущее состояние и события нажатия.

