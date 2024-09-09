Домашнє завдання №11

Створи репозиторій goit-js-hw-11. Збери проєкт за допомогою Vite. Ми підготували
для тебе готову збірку з усіма додатковими налаштуваннями проєкту та
рекомендуємо використовувати саме її. Прочитай завдання і виконай його в
редакторі коду. Переконайся, що код відформатований за допомогою Prettier, а в
консолі відсутні помилки й попередження під час відкриття живої сторінки
завдання. Здай домашнє завдання на перевірку.

Формат здачі: Домашня робота містить два посилання: на вихідні файли і робочу
сторінку на GitHub Pages.

Зверни увагу! Імена файлів та папок, а також їх структура вкладеності, мають
відповідати вказаній схемі. В іншому разі робота не буде прийнята.

Для організації коду використовуй модульність та синтаксис export/import:

У файлі pixabay-api.js зберігай функції для HTTP-запитів. У файлі
render-functions.js створи функції для відображення елементів інтерфейсу. У
файлі main.js напиши всю логіку роботи додатка.

Завдання — Пошук зображень

Створи застосунок пошуку зображень за ключовим словом і їх перегляду в галереї.
Додай оформлення елементів інтерфейсу згідно з макетом.

Для стилізації розмітки твоїх завдань використовуй цей макет.

Форма пошуку

Форма пошуку міститься в HTML-документі. Користувач буде вводити рядок для
пошуку в текстове поле, а за сабмітом форми необхідно виконувати HTTP-запит із
цим пошуковим рядком.

При натисканні на кнопку відправки форми, додайте перевірку вмісту текстового
поля на наявність порожнього рядка, щоб користувач не міг відправити запит, якщо
поле пошуку порожнє.

HTTP-запити

Для бекенду використовуй публічний API сервіс Pixabay. Зареєструйся, отримай
свій унікальний ключ доступу і ознайомся з документацією.

Список параметрів рядка запиту, які тобі обов'язково необхідно вказати:

key — твій унікальний ключ доступу до API. q — слово для пошуку. Те, що буде
вводити користувач. image_type — тип зображення. Потрібні тільки фотографії,
тому постав значення photo. orientation — орієнтація фотографії. Постав значення
horizontal. safesearch — фільтр за віком. Постав значення true. У відповіді буде
об’єкт із декількома властивостями, в одному з яких буде масив зображень, що
задовольнили критерії параметрів запиту.

Якщо бекенд повертає порожній масив, значить, нічого підходящого не було
знайдено. У такому разі показуй повідомлення з текстом "Sorry, there are no
images matching your search query. Please try again!". Для повідомлень
використовуй бібліотеку iziToast.

Для того щоб підключити CSS код бібліотеки в проєкт, необхідно додати ще один
імпорт, крім того, що описаний у документації.

// Описаний у документації import iziToast from "izitoast"; // Додатковий імпорт
стилів import "izitoast/dist/css/iziToast.min.css";

Подивись демовідео роботи застосунку на цьому етапі.

Галерея і картки зображень

Елемент галереї (список однотипних елементів) міститься в HTML-документі, і в
нього необхідно додавати розмітку карток зображень після HTTP-запитів.

Кожне зображення описується об'єктом, з якого тобі цікаві тільки такі
властивості:

webformatURL — посилання на маленьке зображення для списку карток у галереї
largeImageURL — посилання на велике зображення для модального вікна tags — рядок
з описом зображення. Підійде для атрибута alt likes — кількість вподобайок views
— кількість переглядів comments — кількість коментарів downloads — кількість
завантажень Перед пошуком за новим ключовим словом необхідно повністю очищати
вміст галереї, щоб не змішувати результати запитів.

Подивись демовідео роботи застосунку на цьому етапі.

Бібліотека SimpleLightbox

Додай відображення великої версії зображення з бібліотекою SimpleLightbox для
повноцінної галереї.

Для того щоб підключити CSS код бібліотеки в проєкт, необхідно додати ще один
імпорт, крім того, що описаний у документації.

// Описаний у документації import SimpleLightbox from "simplelightbox"; //
Додатковий імпорт стилів import "simplelightbox/dist/simple-lightbox.min.css";

У розмітці необхідно буде обгорнути кожну картку зображення в посилання, як
зазначено в документації в секції «Markup». Бібліотека містить метод
[refresh()](https://github.com/andreknieriem/simplelightbox#public-methods),
який обов'язково потрібно викликати щоразу після додавання нових елементів до
галереї.

Подивись демовідео роботи застосунку на цьому етапі.

Індикатор завантаження

Додай елемент, що сповіщає користувача про те, що йде процес завантаження
зображень з бекенду. Завантажувач має з’являтися прямо перед початком HTTP
запиту та зникати після того, як запит завершився.

Подивись демовідео роботи застосунку на цьому етапі.

Замість банального тексту, як це реалізовано в демовідео, можна використовувати
бібліотеку з гарними індикаторами завантаження, наприклад, css-loader.
Відеоінструкція з використання цієї бібліотеки є в README.md їхнього
репозиторію.

На що буде звертати увагу ментор при перевірці:

Домашня робота містить два посилання: на вихідні файли і живу сторінку на GitHub
Pages Проєкт зібраний за допомогою Vite Консоль в інструментах розробника не
містить помилок, попереджень і консоль логів До проєкту підключені бібліотеки
iziToast, SimpleLightbox та css-loader Елементи на сторінці стилізовані згідно з
макетом (або власні стилі) На сторінці присутня форма пошуку зображень за
пошуковим словом При сабміті форми перед відправкою запиту на бекенд з’являється
індикатор завантаження з css-loader та очищаються попередні результати пошуку на
сторінці При сабміті форми відправляється запит на бекенд по ключовому слову для
пошуку зображень з усіма параметрами, що вказані в ТЗ Після отримання відповіді
від бекенда зникає індикатор завантаження та на сторінці відмальовуються
зображення на основі отриманих даних від бекенду, або з’являється повідомлення
про те, що підходящих результатів не було знайдено Нові зображення додаються в
DOM за одну операцію Після додавання нових елементів до списку зображень на
екземплярі SimpleLightbox викликається метод refresh() При кліку на маленьке
зображення в галереї відкривається його збільшена версія у модальному вікні з
використанням бібліотеки SimpleLightbox Під час виконання HTTP-запитів
використовуються обробники then() та catch(), щоб опрацьовувати можливі помилки
та запобігти “падінню” сторінки
