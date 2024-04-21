***1. Название:***

*Cling - The Interactive C++ Interpreter*

***2. Краткое описание проекта:***

Cling — это интерактивный интерпретатор C++, построенный на основе инфраструктуры компилятора Clang и LLVM.

***3. Количество файлов:*** 
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01find cling/ -type f | wc -l
578
```
***4. Объем всех файлов:*** 
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01 du -csh ./cling/ | tail -n 1
39M
```
***5. Объем исходного кода (с .git):***
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01find ./cling/ -iname ".cpp" -o -iname ".c" -o -iname ".h" -o -iname ".hpp" -o -iname ".cxx" -o -iname ".py" -o -iname ".pl" -o -iname ".php" -o -iname ".java" -o -iname ".cs" -o -iname ".rb" -o -iname ".rs" -o -iname "*.hs" -exec du -ch  + | tail -n 1
- .cpp 60200 
- .hpp 295776 
- .c 9524413 
- .h 1318666 (байт)
```
***6. Найти, если есть файл .clang-format:*** 
```
- .clang-format (находится в корневой папке репозитория)
egor@egor-virtual-machine:/Workspace/TAMOF/rk01 find ./cling -type f -name ".clang-format"
./cling/.clang-format
```
***7.Поиск каталога с именем src***
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01find ./cling -type d -name "src" -exec sh -c 'find "0" -type f | wc -l'  ;
0
Каталога src нет
```
***8. Выписать количество файлов, содержащих слово socket не зависимо от написания:*** 
``` 
egor@egor-virtual-machine:/Workspace/TAMOF/rk01grep -ril socket ./cling | wc -l
2
```
***9. Выписать количество файлов, содержащих слово select не зависимо от написания:***
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01 grep -ril select ./cling | wc -l
35
```
***10. Выписать количество раз, сколько встречается слово Microsoft, Google или Intel не зависимо от написания:***
```    
egor@egor-virtual-machine:/Workspace/TAMOF/rk01grep -rioE "Microsoft|Google|Intel" ./cling | wc -l
45
```
***11. Найти расположение файла LICENSE относительно начала репозитория:***
./LICENSE (находится в корневой папке репозитория)
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01 find ./cling/ -type f -name "LICENSE.TXT"
./cling/LICENSE.TXT 
```
***12. Вывести строку для файла LICENSE (если она есть), в которой есть аббревиатура BSD, GNU, MIT, APSL, Apache, GPL, AGPL, LGPL*** 
```
egor@egor-virtual-machine:/Workspace/TAMOF/rk01cat ./cling/LICENSE.TXT | grep -e "BSD" -e "GNU" -e "MIT" -e "APSL" -e "Apache" -e "GPL" -e "AGPL" -e "LGPL"
                  GNU LESSER GENERAL PUBLIC LICENSE
[This is the first released version of the Lesser GPL.  It also counts
 as the successor of the GNU Library Public License, version 2, hence
freedom to share and change it.  By contrast, the GNU General Public
  Most GNU software, including some libraries, is covered by the
ordinary GNU General Public License.  This license, the GNU Lesser
free software.  For example, permission to use the GNU C Library in
non-free programs enables many more people to use the whole GNU
operating system, as well as its variant, the GNU/Linux operating
                  GNU LESSER GENERL PUBLIC LICENSE
```
