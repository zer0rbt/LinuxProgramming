# Системы сборки кода
https://courses.igankevich.com/linux-programming/notes/build-systems/
## 1. Make (1 балл)
Напишите Makefile с правилами для сборки программы, состоящей из файлов `main.cc` и `main.hh`: первый файл включает второй с помощью `#include`. Программа должна пересобираться при изменении `main.hh`.

#### Пример содержания файлов:
```cpp
// Файл main.cc
#include "main.hh"
int main() { return 0; }
```
```cpp
// Файл main.hh
```

## 2. Make + pkg-config (1 балл)
Соберите код из первого задания с библиотекой zlib. Библиотеку подключите с помощью `pkg-config`.

## 3. Meson (1 балл)
Соберите код из первого задания с библиотекой zlib с помощью Meson.

## 4. Git + Meson (2 балла)
Скачайте проект unistdx с помощью команды git. Соберите его с помощью Meson с флагами компилятора `-march=native -O3` и флагом линковщика `-flto`.
