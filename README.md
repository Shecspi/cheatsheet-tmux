# Шпаргалка по tmux

## Установка
1. Установить tmux  
```bash
sudo pacman -S tmux
```  
2. Установить Tmux Plagin Manager  
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

3. Создать конфигурационный файл `~/.tmux.conf` и в него скопировать содержимое [этого файла](https://github.com/Shecspi/cheatsheet-tmux/blob/master/.tmux.conf)  
4. Войти в tmux и выполнить команду  для установки плагинов, прописанных в конфигурационном файле  
```
<prefix> + I
```

## Запуск tmux
Команда | Описание  
--- | ---
`tmux` | Создать новую сессию
`tmux ls`|Показать список сессий  
`tmux a`|Подключиться к последней активной сессии  
`tmux a -t <name>`|Подключиться к указанной сессии  
`tmux kill-session <name>`|Завершить сессию  
`tmux kill-server`|Полностью завершить tmux


## Сочетания клавиш  
**Layout**  
Команда | Описание  
--- | ---
`<prefix>, \|` | Разделить окно вертикально  
`<prefix>, -` | Разделить окно горизонтально  
`<prefix>, o` | Переключение между терминалами по часовой стрелке  
`<prefix>, <стрелочка>` | Переключение между терминалами в сторону, куда указывает <стрелочка>  
`<prefix>, h/j/k/l` | Изменение размеров активного терминала  
`<prefix>, z` | Развернуть активный терминал на всё окно  
`<prefix>, <space>` | Автоматическое изменение лэйаута  

**Window**  
Команда | Описание  
--- | ---
`<prefix>, c` | Создать новое окно  
`<prefix>, ,` | Переименовать активное окно  
`<prefix>, n` | Переключиться на следующее окно  
`<prefix>, p` | Переключиться на предыдущее окно  
`<prefix>, 1...0` | Переключиться на окно с указанным номером  
`<prefix>, w` | Показать экран навигации между окнами  
`<prefix>, f` | Поиск окна по названию  
`<prefix>, &` | Закрыть активное окно  

**Session**  
Команда | Описание  
--- | ---
`<prefix>, $` | Переименовать активную сессию  
`<prefix>, s` | Показать список сессий  
`<prefix>, d` | Отсоединиться от tmux обратно в консоль

**Копирование через внутренний буфер**  
Команда | Описание  
--- | ---
`<prefix>, [` | Перейти в режим копирования  
`h/j/k/l` | Выделение текста  
`y` | Копирование текста во внутренний бубфер  
`<prefix>, ]` | Вставить текст из внутреннго буфера  
