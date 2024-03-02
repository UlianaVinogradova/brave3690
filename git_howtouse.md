# Подсказка по GIT
____

## Создание репозитория 
Чтобы создать пустой репозиторий Git или повторно инициализировать существующий используем команду:
```sh
git init
```

> *При инициализации Git создаст скрытую папку,в которой будут содержаться ссылки и объекты, которые он использует в истории работы над проектом*

Чтобы получить информацию от git о его текущем состоянии, используем команду:
```sh
git status
```

>_Git дает подсказку, какие действия не были добавлены, выделяя их красным, и какой командой мне нужно воспользоваться: **use git add "file_name"**_

## Создание коммитов и сохранение

Чтобы добавить файл или файлы к следующему коммиту, ипользуем команду add:
```sh
git add "file_name"
```

Чтобы сохранить текущие изменения, чтобы потом была возможность переключаться между ними, используем коммиты: 
```sh
git commit -m "message"
```
 Чтобы вывести на экран истории всех коммитов с их хеш-кодами, используем команду *Log*
 ```sh
git log
```
>*Он отображает список последних коммитов в порядке выполнения. Каждому коммиту присваевается свой номер - **хеш код** (куча цифр и букв после commit). В дальнейшем с помощью данного номера можно переключаться к нужному коммиту*

*Команда **Git log --oneline** также выведет на экран созданные по порядку коммиты, но в более сжатом варианте*

>>Чтобы выйти из режима log в Git-e, нажми <kbd>Q</kbd>

Чтобы переключиться с одного коммита на другой, используем комманду: 
```sh
git checkout
```
>Команда *git checkout main* позволяет вернуться к главной ветке и продолжить работу

Чтобы увидеть различия между текущим файлом и закоммиченным файлом, используем комманду:

```sh
git diff
```

## Добавление изображений 

Чтобы добавить изображение, нужно поставить восклицательный знак, квадратные скобки (внутри них напишем текст подсказку), и далее в круглых скобках название файла изображения. Но сначала этот файл должен быть в этом репозитории. 
![Это кот](cat.jpg)

## Работа с ветками

Чтобы вывести весь список веток в репозитории, используем команду:
```sh
git branch
```
Чтобы создать новую ветку, используем ту же команду + ее имя: 
```sh
git branch NAME 
```
*Звездочкой будет выделяться та ветка, на которой ты находишься*

Чтобы переключиться на другую ветку, используй команду: 
```sh
git checkout имя ветки
```

Чтобы удалить ненужную ветку после слияния, используй команду: 
```sh
git branch -d имя ветки
```
**ВАЖНО!** Удалить ветку нужно после слияния. Чтобы внести содержание ветки в main, используй команду: 
```sh
git merge имя ветки
```
*Эту команду мы вызываем там, куда должны быть внесены изменения. То есть, если надо внести из ветки N изменения в main, то ты должна быть в main и там вызывать эту команду. Для этого сначала используем команду __git checkout main__ и __git branch__, чтобы убедиться, что ты в main, и потом используй __git merge__ (слияние)*

Чтобы вывести дерево коммитов, используй комманду: 
```sh
git log --graph
```

## Работа с удаленными репозиториями

Чтобы скопировать себе репозиторий из Интернета используем команду:

```sh
git clone
```

Чтобы скачать все из удаленного репозитория и автоматически слиять с нашей версией, используй команду 

```sh
git pull
```

Чтобы отправить то, что есть на моем репозитории, на удаленный репозиторий, используй команду: 
```sh
git push
```

### Open
1. Делаем Fork интересующего нас репозитория на GitHub
2. Делаем git clone для нашей версии этого репозитория 
3. Создаем новую ветку с предлагаемыми изменениями 
4. Производим все изменения только в этой ветке 
5. Отправляем эти изменения на свой аккаунт git push
6. В окне на GitHub появляется возможность отправить pull request 

## Дополнительные ссылки
[Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637)

[Регистрация на GitHub](https://gb.ru/manualgithub)

[Скачать Git](https://git-scm.com/download/win)

[Обучение Git oneline](https://learngitbranching.js.org/?locale=ru_RU)