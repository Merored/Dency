DNC-драйвер - пример использования
==================================
###Что это?
* * *
HWSRV - это библиотека с закрытым исходным кодом, предназначеная для работы с российскими фискальными аппаратами или с принтерами чеков.  
Входит в пакет DNC, в который так-же включена кассовая программа с графической оболочкой (исходный код кассовой программы открыт).  
Сайт [разработчика](http://dnc-soft.ru/).

###Зачем это нужно?
* * *
В данном репозитории предствалены простейшие примеры использования библиотеки HWSRV из пакета DNC.  
Их можно искользовать для создания собственных проектов на основе библиотеки HWSRV, а так же для изучния принципов работы с ней.  
  
Документацию по HWSRV можно получить по запросу в поддержку DNC (Сайт DNC приведён выше).

####Подготовка к сборке
* * * 
  1. Установить Денси-Кассу (Тестировалось на версии "dnc_sources_1.2.9.patch4").
  2. Скопировать файл hwsrv.h из "/usr/share/dnc/dnc_sources_*Ваша версиря*/bin/include" в "/usr/local/include".
  3. Выполнить в терминале "sudo apt-get install pthread" если "pthread" не установлено.
  4. Установить g++. Для этого выполнить в терминале "sudo apt-get update" а затем "sudo apt-get install g++".


####Сборка
* * * 
В папке с проэктом выполнить "g++ ./**имя файла.cpp**   -o **Имя исполняемого файла** -lhwsrv -lpthread"  

####Файлы
* * *
*check.cpp* - Печатает чек по данным из файла log.txt.  
*otch.cpp* - Содержит в себе две функции для печати Z-отчёта и X-отчёта.  
*timeSynchronization.cpp* - Синхронизирует время ККМ с врменем компьютера (в том числе и дату).
