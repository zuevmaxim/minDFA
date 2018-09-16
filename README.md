Консольное приложение, минимизирующее DFA.

Сборка приложения: sudo bash compile.sh. Скрипт компилирует файлы main.cpp(алгоритм минимизации) и graph.cpp(создет файл с описание DFA в формате утилиты dot(graphviz)) в исполняемые файлы main и graph в той дириктории, где находился скрипт при запуске. Так же скрипт устанавливает пакет graphviz.

Запуск приложения:
Скрипт run.sh принимает в качестве параметра путь в файлу, в котором находится описание DFA.
Запуск скрипта:
bash run.sh <путь к файлу>
Если в конце добавить флаг -o, скрипт так же нарисует исходный DFA.

Формат входных данных:

На первой строке находится число n -- количество состояний DFA.
На второй строке находится число s -- размер алфавита.
На третьей строке находится s символов через пробел -- символы алфавита.
На четвертой строке находится число q0(1 <= q0 <= n) -- начальное состояние DFA.
На пятой строке находится число t(0 <= t <= n)-- количество терминальных состояний DFA и через пробел t чисел t_j(1 <= t_j <= n) -- терминальные состояния DFA.
На следующих n строках описана таблица переходов DFA. Если в строке i(1 <= i <= n) в столбце j(1 <= j <= s) стоит число k(1 <= k <= n), это значит, что из состояния i есть переход в состояние k по символу j.

Формат выходных данных:
Минимальный автомат выводится в файл out.txt в том же формате, что и входной DFA.

В результате работы скрипта в дириктории появляются файлы out.txt с описанием DFA и изображение minDFA.png. С флагом -o так же еще появится изображение DFA.png -- исходный автомат.
