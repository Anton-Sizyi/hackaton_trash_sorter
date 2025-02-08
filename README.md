# hackaton_trash_sorter
Создание программы для оптимизации сортировки и переработки отходов по фотографиям на основе машинного обучения через взаимодействие с чат ботом

## Команда

- Игнатьева Елена
- Максимов Алексей
- Сизый Антон
- Поцелуев Богдан
- Мельник Илья
- Михасик Руслан

## Описание

В последние десятилетия проблема мусора и его утилизации стала одной из самых острых экологических проблем. Миллиарды тонн отходов ежегодно загрязняют планету, загрязняют водоемы и почву, создавая угрозу для экосистем и здоровья человека. Одним из наиболее эффективных решений этой проблемы является сортировка мусора и его правильная переработка.

Но, несмотря на важность правильной сортировки, многие люди сталкиваются с трудностями в определении, как именно следует утилизировать тот или иной вид отходов. Это приводит к неправильному обращению с мусором и ухудшению состояния окружающей среды.

Данный проект решает проблему с помощью Telegram-бота, который может распознавать мусор на фотографиях и давать рекомендации по его сортировке. Бот будет использовать алгоритмы машинного обучения и компьютерного зрения для классификации различных типов отходов и поможет пользователю узнать, как правильно утилизировать их.

## Функции

1. **Распознавание мусора**: Пользователь отправляет фото мусора, а бот использует алгоритмы машинного обучения для его распознавания и классификации.
   
2. **Категоризация отходов**: Бот определяет, к какой категории относится мусор (пластик, металл, бумага, органические отходы и т.д.).

3. **Рекомендации по утилизации**: На основе классификации бот рекомендует, как именно утилизировать или перерабатывать отходы (переработка, компостирование, утилизация на специальных станциях).

4. **Образовательная функция**: Бот предоставляет информацию о важности сортировки мусора, влиянии отходов на экологию и правильных способах переработки.

## Технологии

Проект использует несколько ключевых технологий для реализации:

- **Telegram Bot API**: для создания самого бота.
- **Python**: основной язык разработки.
- **TensorFlow**: для создания и обучения модели распознавания мусора.

## Установка и настройка

### Требования

- Python 3.x
- Библиотеки: `telebot`, `numpy`, `tensorflow`, `requests`
- Токен для Telegram Bot API.

### Подготовка модели

1. Для распознавания мусора на первом этапе будет использоваться предобученная модель "imagenet" от MoblieNetV2. В дальнейшем планируется использование собственной модели с возможностью дообучения.
2. Для создания бота используется телеграм-бот @BotFather. Для этого необходимо:
- Отправить в чат в чат с BotFather команду /newbot.
- Ввести название бота.
- Ввести юзернейм бота — его техническое имя, которое будет отображаться в адресной строке. Юзернейм должен быть уникальным, написан на латинице и обязательно заканчиваться на bot.
- Получить токен бота.

## Работа с ботом

1. **Начало работы:**
   - Отправьте команду /start, чтобы начать работу с ботом.
   - Бот поприветствует вас и предложит отправить изображение.

2. **Отправка изображения:**
   - Отправьте фотографию мусора через интерфейс Telegram.
   - Бот проанализирует изображение и сообщит предполагаемую категорию мусора вместе с вероятностью (например, "Категория мусора: plastic (вероятность: 0.95)").
   - Также бот предоставит рекомендацию по сортировке и утилизации объекта на изображении.

3. **Оценка корректности:**
   - После анализа бот спросит: "Была ли категория определена правильно? Ответьте 'да' или 'нет'."
   - Ответьте "да" или "нет". Ваш ответ будет сохранен в статистике:
     - "да" → 1 (корректно определено).
     - "нет" → 0 (некорректно определено).

4. **Просмотр статистики:**
   - Отправьте команду /stats, чтобы увидеть текущую статистику загрузок изображений.
   - Статистика содержит следующие данные:
     - Image_ID: Уникальный ID изображения.
     - Category: Категория мусора, определенная моделью.
     - Probability: Вероятность принадлежности к категории.
     - Upload_Time: Время загрузки изображения.
     - Correctness: Оценка пользователя (1 — "да", 0 — "нет").

5. **Экспорт статистики:**
   - Отправьте команду /export, чтобы получить CSV-файл со всей собранной статистикой.
   - Файл будет отправлен вам в виде документа.

6. **Очистка статистики:**
   - Отправьте команду /clearstats, чтобы очистить всю собранную статистику.
   - После выполнения этой команды все данные будут удалены.

7. **Справка:**
   - Отправьте команду /help, чтобы получить это описание снова.

## Заключение

Этот Telegram-бот — это шаг к более экологичному миру, в котором каждый человек может внести свой вклад в правильную утилизацию мусора. Сортировка и переработка отходов — важная задача для защиты нашей планеты, и наш проект поможет сделать этот процесс более доступным и понятным для людей.

## Дальнейшее развитие

- Улучшение интерфейса взаимодействия с пользователем, в том числе использование меню и кнопок вместо ручного ввода команд бота.
- Внедрение механизмов дообучения модели при получении обратной связи от пользователей в виде ответов на вопросы бота в результате анализа полученных фотографий мусора.
- Возможность интеграция бота в системы сортировки мусора на конвейре на предприятиях по утилизации отходов. 


