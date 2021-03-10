1) Глобальный репозиторий я создала на сайте, а для создания локального я использовала следущие команды:
```
mkdir projects/hwlab02 && cd projects/hwlab02
git init
git config --global user.name ${GITHUB_USERNAME}
git config --global user.email ${GITHUB_EMAIL}
git remote add origin https://github.com/${GITHUB_USERNAME}/hwlab02.git
touch README.md
git add README.md
git commit -m"added README.md"
git push origin master
```

2) Коммит  случайно создала на предыдущем шаге
3) Создала файл
```
touch hello_world.cpp
edit hello_world.cpp
```

    # include <iostream>

    using namespace std

    int main(){
        cout << "Hello world";
    }
4) Отправила на сервер
```
git add hello_world.cpp
git commit -m"addede hello_world.cpp"
git push origin master
```
5) Сделала в пункте 4
6) Добавила чтение из консоли
```
edit hello_world.cpp
```
    # include <iostream>

    using namespace std

    int main(){
        string name;
        cin >> name;
        cout << "Hello world from " << name;
    }
7) Закомитила, но чтобы все прошло без ошибок, необходимо добавить опцию -а
```
git commit -m"added cin" -a
```
8) Отправила файлы на сервер
```
git push origin master
```
9) Проверила, скриншот лежит в папке с картинками

---

1) Добавила 
```
git branch patch1
```
2) Я переключилась на нужную ветку и внесла изменения
```
git checkout patch1
edit hello_world.cpp
```
    # include <iostream>

    int main(){
        std::string name;
        std::cin >> name;
        std::cout << "Hello world from " << name;
    }
3) Закоммитела и отправила
```
git commit -m"remove namespace" -a
git push origin patch1
```
4) Проверила, скриншот в папке.
5) Создала
6) Дописала комментарий
```
edit hello_world.cpp
```
    # include <iostream>

    int main(){
        std::string name;
        std::cin >> name; //Input your name plz
        std::cout << "Hello world from " << name;
    }

7) Отправила изменения
```
git commit -m"add comment" -a
git push origin patch1
```
8) Проверила
9) Нажала на нужную кнопочку
10) Сначала переключилась на ветку "мастер"
```
git checkout master
git pull origin master
```
11) Посмотрела логи
commit 0885777f8e43f34c1b0b6a4884c52f0a1d68f5fb (HEAD -> master, origin/master)
Merge: 29d3ee8 21f1ff6
Author: Yourmaidishere <79262298+Yourmaidishere@users.noreply.github.com>
Date:   Wed Mar 10 21:47:18 2021 +0300

    Merge pull request #1 from Yourmaidishere/patch1
    
    remove namespace

commit 21f1ff682956475281399e7a549086d18394b8dd (origin/patch1, patch1)
Author: Yourmaidishere <lislovekiss@mail.ru>
Date:   Wed Mar 10 21:45:14 2021 +0300
12) Удалила не нужную ветку
```
git branch -D patch1 
```


---

1) Создала ветку
```
git branch patch2
git checkout patch2
```
2) Скачала новую прогррамму и использовала ее
```
clang-format -style=Mozilla hello_world.cpp
```
3) Отправила на сервер
4) Немного поменяла комментарий
5) Да, конфликт есть
6) я не знаю как, но я это сделала!!!
```
git checkout master
git rebase master
git checkout patch2
git merge patch2
7) git push --force origin patch2
8) Убедилась
9) Вмержила
