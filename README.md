# Perl Golf

_Perl Golf --- это соревнование по поиску Perl кода наименьшего размера (меньше
всего символов), который решает заданную задачу._

## «Морской бой»

В этом выпуске я хочу предложить вам поиграть в «Морской бой». Всем с детства
известны
[правила](http://ru.wikipedia.org/wiki/%D0%9C%D0%BE%D1%80%D1%81%D0%BA%D0%BE%D0%B9_%D0%B1%D0%BE%D0%B9_%28%D0%B8%D0%B3%D1%80%D0%B0%29)
этой игры. На карте из 10x10 клеток размещаются десять кораблей: один
четырёхпалубный, два трёхпалубных, три двухпалубных и четыре однопалубных
корабля. Корабли могут располагаться как вертикально, так и горизонтально, но
при этом не должны соприкасаться углами. Ну и дальше игроки вслепую обмениваются
ударами, сообщая координаты удара и получая информацию о результате: мимо,
ранен, убит.

В ASCII-графике это может выглядеть примерно так:
           
     .-а-б-в-г-д-е-ж-з-и-к-.     .-а-б-в-г-д-е-ж-з-и-к-.
     1   0 0 0 0           |     1 *                   |
     2   *             0   |     2   *                 |
     3 0   0 0             |     3     *               |
     4 0                   |     4     * X X X         |
     5 0     *     0       |     5                     |
     6     *               |     6                     |
     7   X X *     *       |     7                     |
     8           0 0 0     |     8                     |
     9     0               |     9                     |
    10     0       0       |    10                     |
     `---------------------'     `---------------------'

Попробуйте реализовать такой код, который получив на `STDIN` данные в виде
ASCII-символьного поля 10x10, с изображёнными на нём результатом обстрела в виде
`*` --- промах, `X` --- палуба поражённого корабля и пробел --- неизвестная
территория, попытается выполнить расчёт и поразить одну палубу ещё не
обнаруженного четырёхпалубного корабля, выдав на `STDOUT` ту же самую карту, с
проставленными символами `@` в точках вероятного нахождения линкора.
Гарантируется, что на входном поле нет недобитых кораблей.

Тестовый код будет проверять не только то, что вам удалось поразить линкор, но
также просуммирует количество неуспешных попыток поражения (лишних `@`) в виде
штрафных баллов, которые будут увеличивать длину вашего скрипта на 10 байт за
каждый бал.

Репозиторий нового турнира доступен на github
[golf-09](https://github.com/PragmaticPerl/golf-09). Сделайте форк, создайте в
директории `script` файл `your_github_login.pl` с вашим вариантом решения.
Проверьте, что ваш вариант проходит тесты (с помощью команды `prove`) и сделайте
pull request в основной репозиторий. Помните, что чем раньше вы опубликуете свой
результат, тем больше шансов на победу.

Проверяться решения будут на последней стабильной версии Perl, т.е. 5.18.1.
Приём решений закончится 30 ноября 2013\ г. в 23:59:59.

Дерзайте, юнги! Победителя ждут слава и адмиральские погоны.

■ _Владимир Леттиев_
