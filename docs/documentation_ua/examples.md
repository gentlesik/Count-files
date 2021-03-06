## Приклади практичного використання

- [Підрахунок файлів за розширенням: сортована таблиця](#Підрахунок-файлів-за-розширенням-сортована-таблиця)
- [Пошук файлів за розширенням: список шляхів до файлів](#Пошук-файлів-за-розширенням-список-шляхів-до-файлів)
   - [Пошук та отримання списку файлів з певним розширенням](#Пошук-та-отримання-списку-файлів-з-певним-розширенням)
   - [Пошук та отримання списку файлів без розширення](#Пошук-та-отримання-списку-файлів-без-розширення)
   - [Пошук та отримання списку всіх файлів](#Пошук-та-отримання-списку-всіх-файлів)
- [Загальна кількість файлів](#Загальна-кількість-файлів)
   - [Підрахунок файлів з певним розширенням](#Підрахунок-файлів-з-певним-розширенням)
   - [Підрахунок файлів без розширення](#Підрахунок-файлів-без-розширення)
   - [Підрахунок всіх файлів](#Підрахунок-всіх-файлів)

Більш детально про загальні аргументи 
`path`, `--all`, `--case-sensitive`, `--no-recursion` та `--no-feedback` 
у розділі [Як користуватися](https://github.com/victordomingos/Count-files/tree/master/docs/documentation_ua/howtouse.md)


### Підрахунок файлів за розширенням: сортована таблиця

Скорочена форма аргументів:
```
usage: count-files [-a] [-alpha] [-c]
                   [-nr] [-nf] [path]
```

Повна форма аргументів:

```
usage: count-files [--all] [--sort-alpha] [--case-sensitive]
                   [--no-recursion] [--no-feedback] [path]
```

Найпростішою формою використання CLI 
є ввід команди `count-files` без будь-яких аргументів.  
За замовчуванням програма здійснює пошук файлів рекурсивно 
в поточному робочому каталозі та в усіх його підкаталогах. 
Результатом цього буде таблиця, 
що показує частоту для кожного розширення файлу (наприклад: .txt, .py, .html, .css) 
та загальну кількість знайдених файлів.  
У цьому випадку всі розширення в таблиці 
будуть відображені у верхньому регістрі. 
Приховані файли та каталоги ігноруються.

Приклад:

```
count-files
```

![count_linux_mint](https://user-images.githubusercontent.com/23127253/45508149-c1dbf880-b79c-11e8-9814-ba04f4c00b90.png)

Якщо потрібно відсортувати розширення в таблиці за алфавітом 
додайте аргумент `-alpha` або `--sort-alpha`.

Приклад з одним із загальних аргументів:

```
count-files -c -alpha [path]
```

```
count-files --case-sensitive --sort-alpha [path]
```

![count_windows](https://user-images.githubusercontent.com/23127253/45508316-2b5c0700-b79d-11e8-9e4d-8675fd1e3c0a.png)

### Пошук файлів за розширенням: список шляхів до файлів

Скорочена форма аргументів:

```
usage: count-files [-a] [-c] [-nr]
                   [-fe FILE_EXTENSION] [-fs]
                   [-p] [-ps PREVIEW_SIZE] [path]
```

Повна форма аргументів:

```
usage: count-files [--all] [--case-sensitive] [--no-recursion]
                   [--file-extension FILE_EXTENSION] [--file-sizes]
                   [--preview] [--preview-size PREVIEW_SIZE] [path]
```

Ця утиліта також може використовуватися для пошуку файлів з певним розширенням (використовуючи аргумент `-fe` або `--file-extension`) та 
відображення короткого попереднього перегляду (аргумент `-p` або `--preview`) 
для текстових файлів. 
Розмір попереднього перегляду можна вказати з допомогою аргумента 
`-ps` або `--preview-size` та цілого числа (кількість символів для відображення).  
Переглянути список назв розширень, для яких доступний попередній перегляд, 
можна з допомогою аргументу `-st` або `--supported-types`.  
За замовчуванням результат пошуку за розширенням - список 
з повними шляхами всіх знайдених файлів. 
Якщо потрібна також інформація про розмір кожного окремого файлу 
додайте аргумент `-fs` або `--file-sizes`.

#### Пошук та отримання списку файлів з певним розширенням

Приклад:

```
count-files -fe txt
```

```
count-files --file-extension txt
```

![count_linux_mint_fe_txt](https://user-images.githubusercontent.com/23127253/45508325-36169c00-b79d-11e8-81e2-0d01b7e1ab70.png)

Приклад:

```
count-files -fe py -p -ps 100 -fs [path]
```

```
count-files --file-extension py --preview \
           --preview-size 100 --file-sizes [path]
```

![search_linux_mint_with_args](https://user-images.githubusercontent.com/23127253/45508392-60685980-b79d-11e8-95a6-95f068f14ce6.png)

#### Пошук та отримання списку файлів без розширення

Для отримання списку файлів без розширення, 
використовуйте одну крапку `.` як назву для розширення.  
Файли з такими іменами як `.gitignore`, `Procfile`, `_netrc` 
вважаються файлами без розширення.  
Приклад: `count-files --file-extension . ~/Documents`

#### Пошук та отримання списку всіх файлів

Якщо потрібно отримати список шляхів до всіх файлів незалежно від розширення, 
використовуйте дві крапки `..` як назву для розширення.  
Приклад: `count-files --file-extension .. ~/Documents`

### Загальна кількість файлів

Скорочена форма аргументів:

```
usage: count-files [-a] [-c] [-nr] [-nf] [-t EXTENSION] [path]
```

Повна форма аргументів:

```
usage: count-files [--all] [--case-sensitive] [--no-recursion]
                   [--no-feedback] [--total EXTENSION] [path]
```

Для підрахунку тільки загальної кількості файлів, без списку, 
використовуйте аргумент `-t` або `--total`.  
Для підрахунку загальної кількості всіх файлів, 
файлів з певним розширенням чи без розширення, 
потрібно також вказати назву розширення.

#### Підрахунок файлів з певним розширенням

Приклад:

```
count-files -t txt [path]
```

```
count-files --total txt [path]
```

![total_windows](https://user-images.githubusercontent.com/23127253/45508405-6fe7a280-b79d-11e8-9db9-c81b0116ed1d.png)

#### Підрахунок файлів без розширення

Для отримання інформації про файли без розширення, 
використовуйте одну крапку `.` як назву для розширення.  
Приклад: `count-files --total . ~/Documents`

#### Підрахунок всіх файлів

Якщо потрібно підрахувати загальну кількість незалежно від розширення, 
використовуйте дві крапки `..` як назву для розширення.  
Приклад: `count-files --total .. ~/Documents`
