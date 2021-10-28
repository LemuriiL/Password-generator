Честно утащил для лабораторной работы с сайта https://code-live.ru/post/password-generator-cpp/#comments

Clang-Tidy: Inclusion of deprecated C++ header 'time.h'; consider using 'ctime' instead 3

Clang-Tidy: Inclusion of deprecated C++ header 'stdlib.h'; consider using 'cstdlib' instead 4

Clang-Tidy: Rand() has limited randomness; use C++11 random library instead 49, 52, 55

Clang-Tidy: 'std::random_shuffle' has been removed in C++17; use 'std::shuffle' instead 57

Clang-Tidy: Rand() has limited randomness; use C++11 random library instead 62, 64

Clang-Tidy: Random number generator seeded with a disallowed source of seed value will generate a predictable sequence of values 77

Clang-Tidy: Use nullptr 77

Clang-Tidy: Use auto when initializing with new to avoid duplicating the type name 78


Обработка ошибок отсутствует полностью.
Память из кучи выделяется, но не освобождается. 
под имя файла из кучи выделяется место под 1 (один) символ, а от пользователя по этому адресу принимается строка символов, явно большая, чем один завершающий ноль.

char * filename = new char;
...
cin >> filename;
то есть имя файла должно быть пустое,
чтобы не выйти за границы.
