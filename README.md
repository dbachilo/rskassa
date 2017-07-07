# rskassa
Кассовая программа компании Роза-Сантана под Linux для работы с кассовыми аппаратами АТОЛ. Для лёгкости модификации под другую компанию силами системного администратора, не очень сильного в программировании - написана на Gambas3 (почти Visual Basic 6 только под Linux, разобраться в программе не труднее чем в bash-скрипте, вся визуальная составляющая так же как в VB просто рисуется мышкой).

Для корректной работы требуется положить драйвер касс АТОЛ - библиотеку libfptr.so соотвествующий версии платформы в /usr/lib или другую директорию пользовательских разделяемых библиотек в зависимости от версии ОС. А так же создать файл ~/kkk.conf с настройками драйвера в зависимости от модели кассы и потребностей. Пример для работы по UDP:

<?xml version="1.0" encoding="UTF-8"?>
<settings version="5">
    <value name="AccessPassword">0</value>
    <value name="AutoDisableBluetooth">0</value>
    <value name="AutoEnableBluetooth">1</value>
    <value name="BaudRate">1200</value>
    <value name="Bits">8</value>
    <value name="ConnectionType">1</value>
    <value name="DeviceName">Device #1</value>
    <value name="IPAddress">192.168.54.99</value>
    <value name="IPPort">5555</value>
    <value name="MACAddress"></value>
    <value name="Model">63</value>
    <value name="OfdPort">NONE</value>
    <value name="Parity">0</value>
    <value name="Port">UDPIP</value>
    <value name="Protocol">0</value>
    <value name="SearchDir">/home/bocha/Dist/ATOL/linux-x64/</value>
    <value name="StopBits">0</value>
    <value name="TTYSuffix">ttyACM0</value>
    <value name="UserPassword">30</value>
</settings>

Для запуска потребуется пакет gambas3 и его зависимости.
