import telebot
from telebot import types

bot = telebot.TeleBot('5893096644:AAGdtk_aqgXV-vNeOQI1NTDEbc9u68jyn4E')


@bot.message_handler(commands=['start'])
def start (message):
    mess = f'приветствую,<b>{message.from_user.first_name}.Сейчас ты со мной, ниже тебе представлено чему я смотру тебя научить, ' \
           f',/turtle - Черепашка ' \
           f',/function - Функция ' \
           f',/cycle - Цикл'\
           f',/Debugger - Паучок' \
           f',/global - Операторы global и nonlocal' \
           f',/fline - Форматирование с f-строками' \
           f',/files - Файлы в операционной системе' \
           f',/tkinter - Графический интерфейс через tkinter' \
           f',/datetime  - Библиотека datetime' \
           f',/py - Программа в коротой мы работаем </b>'


    markup = types.ReplyKeyboardMarkup(resize_keyboard=True, row_width=3)
    but1  = types.InlineKeyboardButton('Помощь')
    but2 = types.InlineKeyboardButton('Проводник')
    bakc = types.InlineKeyboardButton('Назад')

    markup.add(but1,but2,bakc)


    bot.send_message(message.chat.id, mess, parse_mode='html')





@bot.message_handler(commands = ['turtle'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://ru.stackoverflow.com/questions/1206470/%D0%9D%D0%B5-%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D1%82%D1%81%D1%8F-%D0%BA%D0%BD%D0%BE%D0%BF%D0%BA%D0%B0-%D0%B2-%D1%82%D0%B5%D0%BB%D0%B5%D0%B3%D1%80%D0%B0%D0%BC-%D0%B1%D0%BE%D1%82%D0%B5-%D0%BD%D0%B0-python'))
   bot.send_message(message.chat.id,'Вы выбрали проект Черепашка.У нас есть видео за которым ты можешь научиться ',reply_markup = markup)

@bot.message_handler(commands = ['function'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=DJAlfolEv9A&ab_channel=egoroff_channel'))
   bot.send_message(message.chat.id,'Вы выбрали проект Функция.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['cycle'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=6uSUQz3k_EM&ab_channel=%D0%93%D0%BE%D1%88%D0%B0%D0%94%D1%83%D0%B4%D0%B0%D1%80%D1%8C'))
   bot.send_message(message.chat.id,'Вы выбрали проект Цикл.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['Debugger'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=HpJYVIRuQbU&ab_channel=luchanos'))
   bot.send_message(message.chat.id,'Вы выбрали проект Debugger.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['global'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=TacyWpUF1Kk&ab_channel=selfedu'))
   bot.send_message(message.chat.id,'Вы выбрали проект Операторы global и nonlocal.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['fline'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=QlkQNWQUCLc&ab_channel=egoroff_channel'))
   bot.send_message(message.chat.id,'Вы выбрали проект Форматирование с f-строками.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['files'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=oRr_bEXJbV0&t=522s&ab_channel=egoroff_channel'))
   bot.send_message(message.chat.id,'Вы выбрали проект Файлы в операционной системе.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['tkinter'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=qsAfMWWmAF8&ab_channel=%D0%93%D0%BE%D1%88%D0%B0%D0%94%D1%83%D0%B4%D0%B0%D1%80%D1%8C'))
   bot.send_message(message.chat.id,'Вы выбрали проект Графический интерфейс через tkinter.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands = ['datetime'])
def website(message):
   markup = types.InlineKeyboardMarkup()
   markup.add(types.InlineKeyboardButton('Просмотр',url='https://www.youtube.com/watch?v=pvIF0Moo-Ok&ab_channel=%D0%9F%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5l%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%D0%B8%D0%B3%D1%80%2C%D1%81%D0%B0%D0%B9%D1%82%D0%BE%D0%B2%D0%B8%D1%82.%D0%B4.'))
   bot.send_message(message.chat.id,'Вы выбрали проект Библиотека datetime.У нас есть видео за которым ты можешь научиться',reply_markup = markup)

@bot.message_handler(commands=['py'])
def website(message):
    markup = types.InlineKeyboardMarkup()
    markup.add(types.InlineKeyboardButton('Тут его можно скачать',
                                          url='https://www.youtube.com/watch?v=X_2kyPCSPoU&ab_channel=PythonRussian'))
    bot.send_message(message.chat.id, 'Pобота проходит в приложении PyCharm.', reply_markup=markup)



@bot.message_handler(content_types=['text'])
def send_text(message):
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True, row_width=2)
    if message.text == 'Помощь':
        bot.send_message(message.chat.id, 'О боте :Бот был создан для новичков. Для помощи изучения языка программирования Python. Бот содержит не всю информацию об этом языке, есть минимальный фундамент ,для дайнельшего понимания хотите ли вы этим заниматься'
                                          'О нас :Я не могу представить эту инфотмацию', reply_markup=markup)
    elif message.text == 'Проводник':
        bot.send_message(message.chat.id, '/turtle - Черепашка ,/function - Функция ,/cycle - Цикл,/Debugger - Паучок,/global - Операторы global и nonlocal,/fline - Форматирование с f-строками,/files - Файлы в операционной системе ,/tkinter - Графический интерфейс через tkinter,/datetime  - Библиотека datetime ,/py - Программа в коротой мы работаем')
    elif message.text == 'Назад':
        bot.send_message(message.chat.id, 'Вы вышли в главное меню')





bot.polling(none_stop=True)
