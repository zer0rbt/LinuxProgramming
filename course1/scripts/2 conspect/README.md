# Оболочка

## Описание заданий
https://courses.igankevich.com/linux-programming/notes/shell/
### 1. Конвертация изображений (1 балл)
Напишите скрипт, который преобразует все переданные в него в качестве аргументов файлы в формат PNG. Для этого:
- Скачайте файлы JPG или аналогичные из интернета с помощью команды `wget`.
- В цикле вызовите команду `convert` (пакет ImageMagick) для преобразования формата файлов. Документацию можно найти в интернете или с помощью команды `man convert`.

### 2. Мониторинг (1 балл)
Напишите скрипт, который выводит показания всех датчиков температуры, поддерживаемых ядром операционной системы. Для этого:
- Воспользуйтесь командой `find`, чтобы найти файлы в директории `/sys`, которые начинаются на `temp` и заканчиваются на `input`.
- В цикле пройдитесь по найденным файлам и выведите их содержимое с помощью команды `cat`.

### 3. Параллельная обработка (1 балл)
Перепишите скрипт из первого задания так, чтобы конвертировались несколько изображений параллельно. Учтите:
- Не запускайте больше двух параллельных процессов на кластере.
- Запускайте конвертацию в фоновом режиме и используйте команду `wait`, чтобы дождаться завершения всех фоновых процессов.
- Для проверки параллельности выполнения можно использовать команду `top`, которая показывает загрузку ядер процессора в реальном времени (запускается в отдельном терминале).

### 4. Конвейер (2 балла)
Напишите скрипт, который ищет файлы с изображениями формата JPG и конвертирует их в формат PNG. Учтите:
- Поиск файлов и конвертация должны быть звеньями конвейера.
- Задумайтесь, будет ли этот скрипт работать быстрее скрипта из третьего задания при обработке большого количества файлов (например, тысячи).

## Инструкции по запуску

1. **Просто запуск скрипта**
   Для выполнения скриптов просто запустите их в командной строке. Например:
   ```sh
   ./script1.sh
   ```

2. **Файл monitoring.txt**
   Для задания мониторинга создайте файл `monitoring.txt`, куда будут выводиться результаты работы скрипта:
   ```sh
   ./script2.sh > monitoring.txt
   ```

3. **Запуск script3.1**
   Запуск скрипта `script3.1` приведет к запуску `script3.sh` несколько раз:
   ```sh
   ./script3.1.sh
   ```

4. **Просто запуск script4.sh**
   Для выполнения задания по конвейеру просто запустите скрипт:
   ```sh
   ./script4.sh
   ```