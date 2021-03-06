# my-latex-template

Мои шаблоны LaTeX для курсовых и лабораторных работ.

# Что нужно установить?

Чтобы собрать документ, вам нужен дистрибутив LaTeX-а, в который входит `xelatex`.
Неплохим вариантом будет [MiKTeX](https://miktex.org/download).

Опционально понадобятся make, git, и Python с пакетом `pygments` для подсветки
синтаксиса в вставляемых исходниках.

Git для Windows можно взять [здесь](https://git-scm.com/download/win).
Make поставляется в комплекте
[MinGW](https://osdn.net/projects/mingw/releases/).

Текст курсовой работы с использованием LaTeX-разметки можно набирать в любом редакторе. Рекомендую Sublime Text
с плагином для проверки грамматики. С основами LaTeX можно
познакомиться [тут](howto-latex.md).

# Как мне написать курсач или сделать лабу?

Выполните команду `make cw` или `make lab`
для подготовки шаблона курсовой или лабораторной работы.

Отредактируйте файлы `main.tex` и `title.tex` под свои нужды. Текст можно разбить и на
несколько файлов (подробнее [здесь](howto-latex.md)).

Для сборки PDF выполните:

```
make all
```

Перед этим в настройках MiKTeX Console лучше указать "Автоматически устанавливать пакеты", поскольку их достаточно много.
Если во время сборки не идет никакого вывода - скорее всего, это подкачиваются пакеты.

Результатом будет файл `main.pdf` в корне проекта.
Проверьте, чтобы он и `main.example.pdf` выглядели одинаково.

Также рекомендуется удалить каталог `.git` и пересоздать его через `git init`.

### Линуксоидам

Из-за бага в MiKTeX, возможно, придется прогнать [эти три команды](https://github.com/MiKTeX/miktex/issues/136#issuecomment-392561637),
чтобы заставить пакет polyglossia работать.

Возможно, даже по два раза ¯\\(°_o)/¯. Еще можно попробовать поставить hyph-utf8 пакет в MiKTeX Console.

Также не забудьте поставить шрифты Times, Courier, Courier New и Arial - regular, bold, italic и bolditalic версии.
