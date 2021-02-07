## Проект "Filmoteka". Команда_1 Группа_24 GOIT

<img align="left" alt="JavaScript" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/js.png" />
<img align="left" alt="Node.js" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/node.png" />
<img align="left" alt="HTML5" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/html.png" />
<img align="left" alt="CSS3" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/css.png" />
<img align="left" alt="Sass" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/sass.png" />
<img align="left" alt="webpack" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/webpack.png" />
<img alt="babel" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/babel.png" />
<img align="left" alt="Git" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/git.png" />
<img align="left" alt="GitHub" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/github.png" />
<img align="left" alt="Terminal" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/consol.png" />
<img align="left" alt="Visual Studio Code" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/vsc.png" />
<img align="left" alt="Firebase" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/firebase.png" />
<img align="left" alt="Handlebars" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/handlebars.png" />
<img alt="jQuery" width="64px" src="https://raw.githubusercontent.com/marvall/filmoteka/main/src/images/stack/jquery.png" />

## Проект выполнен согласно тех.задания.

  Для выполнения работы командой был составлен <a href="https://raw.githubusercontent.com/marvall/filmoteka/main/src/documentation/BackLogFilmoteka.pdf">Backlog.</a>
  
  Для контроля качества, все баги вносились в <a href="https://raw.githubusercontent.com/marvall/filmoteka/main/src/documentation/Check-List.pdf">testCheckList</a>  


## Авторизация FireBase через email и пароль (Ярослав Безуглый)

Реализована авторизация пользователей через комбинацию email и password. Функцилнал работает таким образом что при первом вводе комбинации создается новый аккаунт для firebase, и сразу проходит аунтификация. При следующей попытке войти, будет проходить авторизация проверяя данные в firebase и отслеживает корректность введенных данных. В случае ошибки, ошибки выводяться в соответствующее поле модального окна авторизации.

## Авторизация FireBase через логин-провайдера Google (Антон ткаченко)

Реализовал авторизацию через социального логин-провайдера Google с помощью платформы разработки мобильных и веб-приложений Firebase, а именно службу Firebase Auth.
	Firebase Auth – это служба, которая может аутентифицировать пользователей, используя только код на стороне клиента. Кроме этого, она включает в себя систему управления пользователями, с ее помощью разработчики могут включить аутентификацию пользователя при помощи входа с электронной почты и пароля, которые хранятся в Firebase.
	Используя HTML, CSS и JS реализована разметка, стилизация и логика доступа к модальному окну для ввода данных о пользователе и отображение смены статуса “Sign in” & “Sign out”.
  
 ## Работа с базей Firebase (Ярослав Безуглый)
 
 Для работы с базой Rialtime Database использовалась библиоткка firebase. в качестве ключа в BD используется uid пользователя. При авторизации пользователся идет запрос в базу по UID и если такая таблица существует, то возвращет очереди из базы. Сохранение очереди происходит при клике по соотвествующтм кномкам в карточках фильмов, сначала данные сохраняются в localStorage и срузе же дублируется в RealTime Database. 
  
 ## Динамическое изменение стилей и разметки при навигации страницы. (Антон ткаченко)
 Выполнение переключения между страницами “Home” & “My library” в Header (SPA), кнопок переключения “Watched” & “Queue” в “My library” выполнено с помощью HTML, CSS, JS, а также использовался шаблонизатор “Handlebars Webpack Plugin”.
  
 Handlebars - это простой язык шаблонов. Он использует шаблон и входной объект для создания HTML или других текстовых форматов. Шаблоны Handlebars выглядят как обычный текст со встроенными выражениями Handlebars.
  
Handlebars выражение - это {{, некоторое содержимое, за которым следует}}. Когда шаблон выполняется, эти выражения заменяются значениями из входного объекта.

## Строка поиска и рендер хедера (Ihor Prokopets)

На проекте я писал стили хеддера с использованием препроцессора SASS и логику строки поиска, при написании  логики строки поиска использовалась библиотека lodash

## Навигация сайта и хранение текущей страницы. (Безуглый Ярослав)

Был создан класс стайт, который хранит в себе текущую страницу. Данное значение дублируется в localStorage и проверяется при загрузке страницы. Потому если пользователь откроет страничку повторно, то попадет в ту вкладку в которой был в прошлый раз.

## Функции по работе с API (Артем Сергеев)
В данном проекте используется API по фильмам The Movie Database (TMDb) API (https://www.themoviedb.org/)
Чтобы начать работу, необходимо зарегистрироваться и получить ключ доступа api_key. Делается это один раз, потом этот ключ постоянно используется для получения данных из API. Для этого решения было решено использовать аxios (https://www.npmjs.com/package/axios), который упрощает функционал запросов, в частности позволяет сохранять дефолтные значения (axios.defaults.baseURL = 'https://api.themoviedb.org/3')
Для получения необходимых данных были использованы такие основные запросы на API:
- запрос на список самых популярных фильмов  для создания коллекции на главной странице
(function fetchGetTrending);
- запрос кинофильма по ключевому слову (function fetchGetSearchMovie);
- запрос о полной информации о кинофильме для страницы кинофильма (function fetchGetMovieById);
- запрос о всех жанрах фильмотеки (function fetchGetMovieGenres).
В дальнейшем данные этих запросов использовались в функциях, которые импортировались во весь проект и использовались для работы с интерфейсом сайта( getFilmInfo, getRenres, getFilmsPagination, getFilmInfoToStorage):
-function getFilmInfo - принимает id фильма из галереи, и возвращает данные с полной информацией фильма;
-function getRenres -  возвращает данные о всех жанрах фильмотеки;
-function getFilmsPagination  - принимает слово поиска и номер страницы, и возвращает данные в зависимости от переданных параметров (фильмы по рейтингу или по ключевому слову с сответствующей страницы)
-function getFilmInfoToStorage  - принимает id фильма из LocalStorage, и возвращает данные с полной информацией фильма.
В вышеперечисленных функциях использовались вспомогательные функции, такие как reMapFilmsArray, reMapFilm, reMapFilmToStorage, которые видоизменяли полученные данные, согласно требованиям.

## Додавання фільмів до localStorage (Andrii-Stanislav)
Це завдання виконує функція addToStorage. Фільм повинен додаванися до одного із двох масивів: "watched", або "queue" і може знаходитися тільки в одному і з них, або в жодному із масивів.
Також фільм можна повторно вилучити бази localStorage.
На початку виконання дана функція отримує поточне значення двох масивів, перевіряє наявність ID фільму
в цих масивах, та залежно від результату записує фільм до масиву або видаляє із нього. 


## Шаблон карточки фильма (Viktoriia Ksenofontova)

Створення шаблонів(картка фільму тощо).Саме шаблонізатори дозволяють отримувати дані з мови програмування та виводити їх разом з  розміткою. Тому при вирішенні будь-якої задачі, в якій необхідно створити декілька типових елементів на сторінці веб-додатку з використанням масиву об’єктів, першим, що приходить на думку є використання бібліотеки Handlebars. Handlebars надає нам засоби, необхідні дляефективногоствореннясемантичних шаблонів.Стилі.Для написання таблиці стилів в проекті використовувався препроцесор Sass та розповсюджений синтаксис SCSS(Sassy CSS).Sass допоміг структурувати таблиці стилів та надав можливість використовувати змінні, вкладені правила, міксіни тощо, повністю сумісні з CSS синтаксисом. Опис функцій.

## Шаблон и функция открытия модального окна (Yevheniia Petrychenko)

Модальное окно открывается при клике на элемент галереи. Содержит в себе краткую
информацию о фильме. Для модального окна исспользовался плагин Micromodal.js.
Разметка модального окна была создана в шаблоне HBS. Он фильтрует объект
приходящий с бэкэнда и выбирает необходимые значения. Для открытия модального
окна исспользуется js функция. Она рендерит разметку для модального окна при
нажатии на елемент галлереи, принимает id фильма, возвращает информацию
необходимую для разметки из API. Применяет стили, если необходимо.Подставляет
статус на кнопки, если необходимо и удаляет атрибуты с єлемента галереи при
закрытии окна. Стили реализованы в препроцессоре SASS. Написанны для четырех
брейкпоинтов @media 320, @media 768, @media 1024,@media 1400. Модальное окно
закрывается при клике на оверлей и нажатии на клавишу esc.

## Пагинация (Olena Tsemko)

Pagination – для ее реализации в проекте применяется плагин (https://pagination.js.org/index.html). В проекте используется 2 пагинации:- Первая (для вкладки HOME) использует функцию запроса на API и функцию рендера страницы с полученных данных.  При переключении страниц происходит запрос на API и строится страничка. Количество карточек фильмов на странице – согласно макету, для разных устройств разное. Это реализовано с помощью медиа запросов через JS. Так как API возвращает по дефолту массив с 20-ью результатами, и этот параметр (в данном API) изменить нельзя, то над пагинацией расположена кнопка, которая догружает остальные результаты, которые не попадают в видимость страницы по макету, чтоб не терялся контент. - Вторая пагинация (для вкладки MY LIBRARY) берет данные с функции, которая возвращает массив обьектов с  Local Storage и так же с помощью функции рендера страниц прорисовывает карточки согласно макету.Также при переключении страниц в пагинации происходит скролл к началу страницы для удобства пользования. Если же результат поиска выдает меньше результатов, чем должно быть элементов на странице – пагинация не появляется, аналогично с кнопкой.

## Футер (Myroslava Nikolaenko)

При клике на ссылку GoIT Students открывается модальное окно. Оно реализовано с помощью библиотеки модального окна MicroModal.
Для отображения данных был написан шаблон modalFooter.hbs, который перебирает данные участников проекта и отображает их в модальном окне. Данные участников проекта хранятся в файле footerGalleryItem.js: имя, фотография, информация о том, чем занимался на проекте и ссылки на соцсети. Иконки для ссылок реализованы с помощью шрифта Font Awesome.
Для стилизации модального окна был использован препроцессор SASS.

## Спинер (Olena Tsemko)

Spinner – функция, которая используется для отображения процесса загрузки на странице. Spinner построен с использованием HTML, SCSS и JS (для вставки HTML-разметки при запуске, и удалении при остановке). Вызывается - в зависимости от получаемого параметра start или stop – соответствено запустить или остановить. Цвет и дизайн подобраны так, чтоб подчеркнуть общую стилистику сайта.

## Стрелочка возрата (Артем Сергеев)

Для удобства пользователя на странице сайта была добавлена стрелка для возврата на начало страницы (function arrowTop). Как только пользователь покидал первую часть видимой страницы, то появляется стрелка, при нажатии на которую происходит автоматический скролл на начало страницы. 

## Модальное окно Трейлера (Viktoriia Ksenofontova)

ФункціяgetVideoUrl() призначена для отримання з TMDb посилання на офіційний трейлер кінострічки в Youtube. Інструментом для HTTP-запитів  є Axios, який надає більш зручний API порівняно зfetch(), зокрема автоматичний синтаксичний аналіз JSON.Функція showVideo(), яка викликається під час кліку на кнопку розташовану на обкладинці фільму, в свою чергу викликає getVideoUrl(), генерує розмітку модального вікна та вбудовує фрейм для перегляду відео-трейлера кінострічки.Модальні вікна.Для створення модальних вікон наша команда використовувала зручну бібліотеку Micromodal.js

## Всплывающая подсказка в поисковой строке (Артем Сергеев)

Для удобства пользователя на странице сайта был добавлен выпадающий список подсказок фильмов в поисковой строке (function renderListSearch).
При вводе информации, если что-то соответствует введенным данным, выпадает список из 5 подсказок отсортированных по рейтингу от наибольшего (за это отвечает вспомогательнае функция function sortByRating.

## Деплой сайту на хостинг Netlify (Andrii-Stanislav)
В нашому командному проекті було прийнято рішення додатково використати платформу для хостінгу
веб-додатків Netlify. 
Із переваг хостингу через Netlify можна визначити:
1. Єдиний вигляд url в порівнянні із GitHub.
2. Кожен учасник команди зможе зробити собі копію репозиторію без необхідості повторно налаштовувати деплой на хостінг.
3. За умови машатабування проекту та додавання динамічної маршрутиизації це буде можливо зробити.

### Деплой сайту на хостинг Netlify (Andrii-Stanislav)

## Deploying/Publishing

В нашому командному проекті було прийнято рішення використати динамічну маршрутизацію.
Для корректної роздачі подібного сайту нам потрібно налаштувати хостінг, щоб на кожен
запит за файлом html хостінг віддавав index.html, не зважаючи на url запиту.
GitHub Pages не має такої можливості. Тому ми використали платформу для хостінгу
веб-додатків Netlify.  

<!-- Пользователям **Windows**, в режиме администратора.
[Как запусттить Powershell](https://youtu.be/p2tFnxcymwk) в режиме
администратора. -->


### Register on Netlify
 
Спочатку потрібно зарееструватися на Netlify. Бажано зробити це за допомогою акаунту GitHub,
оскільки це дасть більше цікавих можливостей в роботі.  

### Add netlify.toml

Далі додаємо в корінь проекту файл netlify.toml.
В даниий документ додаємо необхідні налаштування.

```json
[build]
    publish = "build"

[[redirects]]
    from = "/*"
    to = "/index.html"
    status = 200
```

### Netlify CLI і netlify-скрипти

Для деплою через npm-скрипти портрібно один раз глобально встановити Netlify CLI.
В терміналі виконуємо команду 

```shell
npx install netlify-cli -g
```

Далі отримуємо право доступу до свого netlify акаунту через термінал.
Виконуємо команду

```shell
netlify login
```
В браузері відкриється вкладка де необхідно підтвердити авторизацію.

Наступним кроком в нашому проекті в файлі package.json додаємо npm-скрипти для автоматичного деплою

```json
"predeploy": "npm run build",
"deploy": "netlify deploy -p" 
```

Також в файлі package.json необхідно видалити властивість "homepage".

### Deploy
 
Виконуємо команду:
```shell
npm run deploy
```
Спочатку атоматично запускається скрипт "predeploy" і робить свіжий білд додатку.

При перешому деплою на netlify необхідно створити та налаштувати проект.
Кнопками "вверх", "вниз" обираємо команду "+ Create & configure a new site".

Команду розробників обираємо за замовчуванням натиснувши Enter.

Далі обираємо назву сайту. Це має бути унікальний рядок. Рекомендується на початку або в кінці назви
дописати ваш логін на netlify, але це не обов'язково. Головне, щоб це було унікальне значення.

Через деякий час бачимо результат. Всі детальнашого проекту відображені в терміналі.
Також керування сайтом можна здійснити через браузер в акаунті netlify.

Для кожного наступного деплою вашого додатку виконуємо команду
```shell
npm run deploy
```
