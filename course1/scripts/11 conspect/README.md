# Память
https://courses.igankevich.com/linux-programming/notes/memory/
## Буферы (1 балл)
- Напишите класс `ByteBuffer`, который представляет собой массив байт, размер которого можно изменять динамически. 
- Для этого в конструкторе выделите память с помощью системного вызова `mmap`, в деструкторе освободите память с помощью `munmap`. 
- Не забудьте про проверку возвращаемого значения каждого системного вызова!

## Перемещение (1 балл)
- Добавьте в класс `ByteBuffer` конструкторы и операторы перемещения. 
- Проверьте, что память корректно освобождается с помощью санитайзеров.

## Изменение размера (1 балл)
- Добавьте в класс `ByteBuffer` метод для изменения размера выделенной области памяти `resize`, который использует вызов `mremap`.

## File + ByteBuffer (2 балла)
- Объедините класс `File` из заданий к предыдущему занятию с классом `ByteBuffer`. 
- Для этого сделайте `File` полем класса `ByteBuffer` и добавьте конструктор `ByteBuffer`, который позволяет создавать буфер из файла: вам понадобится вызов `stat`, чтобы узнать размер файла. 
- Также модифицируйте деструктор, так чтобы он записывал буфер в файл с помощью вызова `msync`.