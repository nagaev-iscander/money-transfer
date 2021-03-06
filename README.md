## Установка
mvn clean install

## Задание
1. Запустить программу командой java -jar <путь до скомпилированной shaded jar'ки>
2. Запустить скрипт run_tests.py
3. С помощью jvisualvm подключиться к работающей программе и проанализировать метрики.

На каждом этапе выполнения задания, собирайте следующую информацию:
- на сколько загружен CPU
- сколько в среднем потребляется памяти, заметен ли в программе memory leak
- как часто происходит сборка мусора  
- сколько в среднем выполняется запуск сценария 1, как быстро увеличивается это время
- какие операции из значимых (т.е. без учета работы системных функций, в т.ч. веб сервера) занимают больше всего процессорного времени
- на основе этой информации решите, что в коде можно оптимизировать, и кратко обоснуйте свое решение
- проведите оптимизацию и повторите сбор информации

Также можете провести свои оптизации в коде, даже если не видите для этого формацльных метрик в jvisualvm.
 
Для финальной версии программы сделайте Pull Request на github'е, в названии пулл реквеста напишите ваше имя, а в комментариях к пулл реквесту напишите ваш анализ

После того как вы исправите все найденные баги, проведите дополнительные эксперименты:
- попробуйте использовать разные GC и сравните как они себя ведут в плане потребления ресурсов, опишите найденные вами различия и выберите по вашему мнению подходящий GC для этого приложения
- полностью перепишите AccountDAOImpl и UserDAOImpl избавившись от базы данных, и реализовав все функции на основе HashMap и других структур, которые будут работать наиболее эффективно для тестового сценария 1. Получилось ли увеличить производительность программы?    
