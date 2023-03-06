from telegram import ParseMode
import psycopg2
import telegram
import os
import telegram
from telegram import Update
from telegram.ext import CallbackContext
from telegram import ReplyKeyboardMarkup
from telegram.ext import MessageHandler, Filters
# Import necessary modules
from telegram.ext import Updater, CommandHandler, MessageHandler, Filters, ConversationHandler
import telegram
from telegram import ParseMode





def my_function(update: Update, context: CallbackContext):
    # function code here
    pass


TOPIC = "Тема роботи"
PAGES = "Вкажіть кількість сторінок (від 1 до 150)"
UNIQUENESS ="Вкажіть % унікальності"
DEADLINE = "На яку дату вам потрібна робота? (Враховуйте, що якщо робота термінова, то вартість буде збільшена)"
COMMENT = "Можливо є коментар або методичка? Якщо так, напишіть коментар або надішліть файл."
AUTHOR_CHAT_ID = 859360040
COST_CONFIRM = False
task_type = "Реферат"
"Магістерська робота"
"Бакалаврська робота"
"Доповідь"
"Есе"
"Стаття"
"Контрольна робота"
"Відповіді на запитання"
"Бізнес план"
"Переклад"
"Онлайн допомога на іспиті"
"Звіт з практики"
"Лабораторна робота"
"Копірайтінг"
"Рерайтінг"
"Креслення"
"Презентація"
"Домашнє завдання"
"Колоквіум"
"Вирішення задач"
"Підвищення унікальності тексту"
"Рецензія"
"Анотація"

def function_name(update, context):
    task_type = context.user_data['task_type']
    # rest of the function code


import random

def generate_customer_id():
    return random.randint(1000, 9999)


# з'єднання з базою даних
conn = psycopg2.connect(
    host="ec2-52-48-159-67.eu-west-1.compute.amazonaws.com",
    database="d7lr098nlc0jn6",
    user="yqluyjjwqokfic",
    password="668a8e54a7943f0ebca500165b3aa9d9786df25ab6c31eb041e871475d3e53aa",
    port="5432"
)

# створення курсора для виконання запитів
cur = conn.cursor()

# виконання запиту
cur.execute("SELECT * FROM mytable")

# отримання результатів запиту
results = cur.fetchall()

# роздруківка результатів
for row in results:
    print(row)

from telegram.ext import Updater, CommandHandler, CallbackQueryHandler
from telegram import InlineKeyboardButton, InlineKeyboardMarkup
import uuid

TOKEN = "6201719090:AAHVmrXtpwRTD31h2XZtvF29S8sVr2VTOj8"

# словник для зберігання ідентифікаторів клієнтів
clients = {}


def start(update, context):
    #Функція викликається при вході в бота
    chat_id = update.effective_chat.id
    if chat_id not in clients:
        # генеруємо новий унікальний ідентифікатор для клієнта
        client_id = str(uuid.uuid4())
        # зберігаємо ідентифікатор клієнта в словнику
        clients[chat_id] = client_id
    else:
        # отримуємо існуючий ідентифікатор для клієнта
        client_id = clients[chat_id]
    context.bot.send_message(chat_id=chat_id,
                             text="Привіт! Я можу допомогти з виконанням твого завдання. Що потрібно?")
    show_options(update, context)


def show_options(update, context):
    # Функція виводить кнопки з варіантами робіт.
    keyboard = [
        [
            InlineKeyboardButton("Дипломна робота", callback_data="diploma"),
            InlineKeyboardButton("Реферат", callback_data="essay")
        ],
        [
            InlineKeyboardButton("Магістерська робота", callback_data="master"),
            InlineKeyboardButton("Бакалаврська робота", callback_data="bachelor")
        ],
        [
            InlineKeyboardButton("Доповідь", callback_data="report"),
            InlineKeyboardButton("Есе", callback_data="composition")
        ],
        [
            InlineKeyboardButton("Стаття", callback_data="article"),
            InlineKeyboardButton("Контрольна робота", callback_data="test")
        ],
        [
            InlineKeyboardButton("Відповіді на запитання", callback_data="faq"),
            InlineKeyboardButton("Бізнес план", callback_data="business_plan")
        ],
        [
            InlineKeyboardButton("Переклад", callback_data="translation"),
            InlineKeyboardButton("Онлайн допомога на іспиті", callback_data="exam_help")
        ],
        [
            InlineKeyboardButton("Звіт з практики", callback_data="practice_report"),
            InlineKeyboardButton("Лабораторна робота", callback_data="lab")
        ],
        [
            InlineKeyboardButton("Копірайтінг", callback_data="copywriting"),
            InlineKeyboardButton("Рерайтінг", callback_data="rewriting")
        ],
        [
            InlineKeyboardButton("Креслення", callback_data="drawing"),
            InlineKeyboardButton("Презентація", callback_data="presentation")
        ],
        [
            InlineKeyboardButton("Домашнє завдання", callback_data="homework"),
            InlineKeyboardButton("Колоквіум", callback_data="quiz")
        ],
        [
            InlineKeyboardButton("Вирішення задач", callback_data="problem_solving"),
            InlineKeyboardButton("Підвищення унікальності тексту", callback_data="uniqueness")
        ],
        [
            InlineKeyboardButton("Рецензія", callback_data="review"),
            InlineKeyboardButton("Анотація", callback_data="abstract")
        ],
        [
            InlineKeyboardButton("План до дипломної роботи", callback_data="diploma_plan"),
            InlineKeyboardButton("План до дипломної роботи", callback_data="diploma_plan")
        ]
    ]

    reply_markup = InlineKeyboardMarkup(keyboard)
    update.message.reply_text('Виберіть вид роботи:', reply_markup=reply_markup)


def button_click(update, context):
    # Code here
    pass

# Функція обробляє вибір з кнопок.
def callback_handler(update, context):
    query = update.callback_query
    query.answer()
    query.edit_message_text(text=f"Ви обрали: {query.data}")


def main():
    # Функція створює бота і запускає його.
    updater = Updater(TOKEN, use_context=True)
    dp = updater.dispatcher
    # Обробка команд
    dp.add_handler(CommandHandler("start", start))

def button_click(update, context):
    # Функція обробляє вибір з кнопок.
    def callback_handler(update, context):
        query = update.callback_query
        query.answer()
        query.edit_message_text(text=f"Ви обрали: {query.data}")

def show_options(update, context):
    # Функція виводить кнопки з варіантами робіт.
    keyboard = [
        [
            InlineKeyboardButton("Дипломна робота", callback_data="diploma"),
            InlineKeyboardButton("Реферат", callback_data="essay")
        ],
        [
            InlineKeyboardButton("Магістерська робота", callback_data="master"),
            InlineKeyboardButton("Бакалаврська робота", callback_data="bachelor")
        ],
        [
            InlineKeyboardButton("Доповідь", callback_data="report"),
            InlineKeyboardButton("Есе", callback_data="composition")
        ],
        [
            InlineKeyboardButton("Стаття", callback_data="article"),
            InlineKeyboardButton("Контрольна робота", callback_data="test")
        ],
        [
            InlineKeyboardButton("Відповіді на запитання", callback_data="faq"),
            InlineKeyboardButton("Бізнес план", callback_data="business_plan")
        ],
        [
            InlineKeyboardButton("Переклад", callback_data="translation"),
            InlineKeyboardButton("Онлайн допомога на іспиті", callback_data="exam_help")
        ],
        [
            InlineKeyboardButton("Звіт з практики", callback_data="practice_report"),
            InlineKeyboardButton("Лабораторна робота", callback_data="lab")
        ],
        [
            InlineKeyboardButton("Копірайтінг", callback_data="copywriting"),
            InlineKeyboardButton("Рерайтінг", callback_data="rewriting")
        ],
        [
            InlineKeyboardButton("Креслення", callback_data="drawing"),
            InlineKeyboardButton("Презентація", callback_data="presentation")
        ],
        [
            InlineKeyboardButton("Домашнє завдання", callback_data="homework"),
            InlineKeyboardButton("Колоквіум", callback_data="quiz")
        ],
        [
            InlineKeyboardButton("Вирішення задач", callback_data="problem_solving"),
            InlineKeyboardButton("Підвищення унікальності тексту", callback_data="uniqueness")
        ],
        [
            InlineKeyboardButton("Рецензія", callback_data="review"),
            InlineKeyboardButton("Анотація", callback_data="abstract")
        ],
        [
            InlineKeyboardButton("План до дипломної роботи", callback_data="diploma_plan")
        ]
    ]

def subject(update, context):
    # Function to ask for the subject of the work"
    text = "З якого предмету вам потрібна допомога?"
    update.message.reply_text(text)
    return TOPIC



def topic(update, context):
    # Function to ask for the topic of the work
    text = "Вкажіть тему."
    update.message.reply_text(text)
    return PAGES


def pages(update, context):
    # Function to ask for the number of pages
    text = "Вкажіть кількість сторінок (від 1 до 150)"
    update.message.reply_text(text)
    return UNIQUENESS


def uniqueness(update, context):
    """Function to ask for the uniqueness percentage"""
    text = "Вкажіть % унікальності"
    update.message.reply_text(text)
    return DEADLINE


def deadline(update, context):
    """Function to ask for the deadline"""
    text = "На яку дату вам потрібна робота? (Враховуйте, що якщо робота термінова, то вартість буде збільшена)"
    update.message.reply_text(text)
    return COMMENT


def comment(update, context):
    """Function to ask if there are any comments or additional materials"""
    text = "Можливо є коментар або методичка? Якщо так, напишіть коментар або надішліть файл."
    update.message.reply_text(text)
    return ConversationHandler.END

DATABASE_URL = os.environ['DATABASE_URL']


def save_order_to_database(update: Update, context: CallbackContext):
    chat_id = update.message.chat_id
    customer_id = generate_customer_id()  # Функція для генерації ID замовника
    order_type = context.user_data['order_type']
    theme = context.user_data['theme']
    uniqueness = context.user_data['uniqueness']
    date = context.user_data['date']
    comment = context.user_data['comment']

    # Збереження інформації в базу даних
    conn = psycopg2.connect(DATABASE_URL, sslmode='require')
    cursor = conn.cursor()

    cursor.execute(
        "INSERT INTO orders (customer_id, chat_id, order_type, theme, uniqueness, date, comment) VALUES (%s, %s, %s, %s, %s, %s, %s)",
        (customer_id, chat_id, order_type, theme, uniqueness, date, comment)
    )

    conn.commit()
    cursor.close()
    conn.close()

    # Збереження інформації в Heroku
    order_info = f"<b>ID ЗАМОВНИКА:</b> {customer_id}\n" \
                 f"<b>ПРЕДМЕТ:</b> {order_type}\n" \
                 f"<b>ПРЕДМЕТ-ВІДПОВІДЬ:</b> {theme}\n" \
                 f"<b>СТОРІНОК:</b> {context.user_data['pages']}\n" \
                 f"<b>УНІКАЛЬНІСТЬ:</b> {uniqueness}%\n" \
                 f"<b>ДАТА:</b> {date}\n" \
                 f"<b>КОМЕНТАР:</b> {comment}"

    context.bot.send_message(chat_id=os.environ['HEROKU_APP_NAME'], text=order_info, parse_mode=ParseMode.HTML)

DATABASE_URL = os.environ['DATABASE_URL']

def save_order_to_database(update: Update, context: CallbackContext):
    chat_id = update.message.chat_id
    customer_id = generate_customer_id() # Функція для генерації ID замовника
    order_type = context.user_data['order_type']
    theme = context.user_data['theme']
    uniqueness = context.user_data['uniqueness']
    date = context.user_data['date']
    comment = context.user_data['comment']
    # Запис інформації в файл
    with open('orders.txt', 'a') as file:
        file.write(f"{customer_id} - {order_type}\n")
        file.write(f"Предмет: {theme}\n")
        file.write(f"Тема: {context.user_data['topic']}\n")
        file.write(f"Сторінок: {context.user_data['pages']}\n")
        file.write(f"Унікальність: {uniqueness}%\n")
        file.write(f"Дата: {date}\n")
        file.write(f"Коментар: {comment}\n\n")

    # Запис інформації в базу даних
    conn = psycopg2.connect(DATABASE_URL, sslmode='require')
    cursor = conn.cursor()

    cursor.execute(
        "INSERT INTO orders (customer_id, chat_id, order_type, theme, uniqueness, date, comment) VALUES (%s, %s, %s, %s, %s, %s, %s)",
        (customer_id, chat_id, order_type, theme, uniqueness, date, comment)
    )

    conn.commit()
    cursor.close()
    conn.close()

    # Надіслати підтвердження про збереження інформації
    update.message.reply_text("Інформацію збережено. Дякую!")

def confirm_author(update, context):
    """Function to confirm if the author can do the work"""
    text = "Зараз запитаю авторів, чи зможуть вони це зробити."
    update.message.reply_text(text)

    # send order information to author
    order_id = context.user_data['order_id']
    subject = context.user_data['subject']
    topic = context.user_data['topic']
    pages = context.user_data['pages']
    uniqueness = context.user_data['uniqueness']
    deadline = context.user_data['deadline']
    comment = context.user_data['comment']
    author_info = f"New Order: \nOrder ID: {order_id} \nSubject: {subject} \nTopic: {topic} \nPages: {pages} \nUniqueness: {uniqueness} \nDeadline: {deadline} \nComment: {comment}"

    # send the order information to the author
    keyboard = ReplyKeyboardMarkup([['Accept', 'Reject']], one_time_keyboard=True)
    context.bot.send_message(chat_id=AUTHOR_CHAT_ID, text=author_info, reply_markup=keyboard)

    return AUTHOR_CONFIRM

def author_response(update, context):
    """Function to handle the author's response"""
    response = update.message.text.lower()
    if response == 'accept':
        update.message.reply_text("Ви прийняли роботу.")
        # send confirmation to customer
        context.bot.send_message(chat_id=CUSTOMER_CHAT_ID, text="Автор прийняв вашу роботу.")
        return ConversationHandler.END
    elif response == 'reject':
        update.message.reply_text("Ви відхилили роботу.")
        return ConversationHandler.END
    else:
        update.message.reply_text("Будь ласка, виберіть 'Accept' або 'Reject'.")
        return AUTHOR_CONFIRM

AUTHOR_CHAT_ID = 859360040
CUSTOMER_CHAT_ID = None
AUTHOR_CONFIRM = range(1)

# Create ConversationHandler
author_handler = ConversationHandler(
    entry_points=[CommandHandler('confirm_author', confirm_author)],
    states={
        AUTHOR_CONFIRM: [MessageHandler(Filters.text, author_response)]
    },
    fallbacks=[],
)

work_type = input("Enter the type of work: ")
uniqueness = int(input("Enter the uniqueness of the content: "))
pages = int(input("Enter the number of pages: "))
def calculate_order_cost(pages, task_type, urgency, uniqueness):
    # калькулятор
    if task_type in ['Дипломна робота', 'магістерська робота', 'бакалаврська робота']:
        if uniqueness <= 30:
            cost = 20 * pages
        elif 30 < uniqueness <= 50:
            cost = 30 * pages
        elif 50 < uniqueness <= 80:
            cost = 50 * pages
        elif 80 < uniqueness <= 100:
            cost = 60 * pages
    else:
        if uniqueness <= 50:
            cost = 10 * pages
        elif 50 < uniqueness <= 80:
            cost = 20 * pages
        elif 80 < uniqueness <= 100:
            cost = 30 * pages

    if task_type in ['Курсова робота', 'есе', 'стаття', 'копірайтинг', 'рерайт']:
        if urgency == '6-12 днів':
            cost = cost * 1.5
        elif urgency == '3-5 днів':
            cost = cost * 2
        elif urgency == '1-2 дні':
            cost = cost * 3
        elif urgency == '6-24 години':
            cost = cost * 5

    elif task_type in ['Реферат', 'доповідь']:
        if urgency == '6-12 днів':
            cost = cost * 1.2
        elif urgency == '3-5 днів':
            cost = cost * 1.5
        elif urgency == '1-2 дні':
            cost = cost * 2
        elif urgency == '6-24 години':
            cost = cost * 3

    return cost

def confirm_order(update, context):
    # ... get information from the user_data dictionary ...

    # Get the task type from user data
    task_type = context.user_data.get('task_type', '')

    def confirm_order_details(update, context):
        # Get the order details from the user
        task_type = context.user_data['task_type']
        uniqueness = context.user_data['uniqueness']
        pages = context.user_data['pages']
        urgency = context.user_data['urgency']

        # Calculate the order cost
        cost = calculate_order_cost(pages, task_type, urgency, uniqueness)

        # Check the cost and perform additional actions if necessary
        if task_type in ["Дипломна робота", "магістерська робота", "бакалаврська робота"]:
            # Perform additional actions for diploma, term paper, master's thesis, and bachelor's thesis
            if cost > 1000:
                update.message.reply_text("Ціна замовлення дорожча 1000 грн, чи ви погоджуєтеся?")
                return COST_CONFIRM

                # Format the order details as a string
            order_details = f"Тип роботи: {task_type}\nУнікальність контенту: {uniqueness}%\nКількість сторінок: {pages}\nТермін виконання: {urgency}\nЦіна: {cost} грн"

            # Send the order details to the user
            update.message.reply_text(order_details)

            # Ask the user to confirm the order
            update.message.reply_text("Чи підтверджуєте замовлення?")

            # Return the confirmation status as a string
            return "CONFIRMED"

        else:
            # Perform actions for other types of tasks
            # ...

            cost = calculate_order_cost(pages, task_type, urgency, uniqueness)

            # Do something
            if cost > 500:
                update.message.reply_text("Ціна замовлення дорожча 500 грн, чи ви погоджуєтеся?")
                return COST_CONFIRM
            else:
                update.message.reply_text("Вартість роботи становить {} грн".format(cost))
def confirm_cost(update, context):
    user_response = update.message.text.lower()
    if user_response == "yes":
        cost = context.user_data.get('cost')
        update.message.reply_text("Вартість роботи становить {} грн".format(cost))

        def confirm_order_details(update, context):
            # Get the user's confirmation status
            confirmed = update.message.text.lower()

            # Check if the user confirmed the order
            if confirmed in ["yes", "так", "авжеж", "ок"]:
                # Perform actions to confirm the order
                # ...
                update.message.reply_text("Дякуємо за замовлення! Ми зв'яжемося з вами найближчим часом.")
                return "ORDER_COMPLETED"

            else:
                # Perform actions if the user didn't confirm the order
                # ...
                update.message.reply_text("Замовлення скасовано.")
                return "ORDER_CANCELLED"

    else:
        update.message.reply_text("Ви відхилили вартість замовлення.")
        return ConversationHandler.END

def calculate_cost(task_type, task_details):
    # Implementation of the function goes here
    pass
def get_task_details():
    # Ask the user for input regarding the task details
    details = input("Please provide details about the task: ")
    return details

def calculate_cost(task_type, task_details):
    # Calculate the cost of the task based on its type and details
    if task_type == "diploma thesis":
        cost = 5000
    elif task_type == "term paper":
        cost = 3000
    elif task_type == "master's thesis":
        cost = 7000
    elif task_type == "bachelor's thesis":
        cost = 4000
    else:
        cost = 1000

    # Add additional cost based on the length of the task details
    cost += len(task_details) // 100

    return cost


# Check if the task type is a diploma, term paper, master's thesis, or bachelor's thesis
if task_type in ["diploma thesis", "term paper", "master's thesis", "bachelor's thesis"]:
    # perform additional actions for diploma, term paper, master's thesis, and bachelor's thesis
    task_details = get_task_details()
    # Calculate the cost of the task
    amount = calculate_cost(task_type, task_details)
    # Ask the person to confirm their entry
    bot_message = "Ваша робота коштуватиме " + str(
        amount) + " грн. Для підтвердження внесіть аванс у розмірі 10% і протягом 24 годин ми надішлемо вам план вашого завдання для узгодження з викладачем."
else:
    # perform actions for other types of tasks
    task_details = get_task_details()
    # Calculate the cost of the task
    amount = calculate_cost(task_type, task_details)

    # Ask the person to confirm their entry
    bot_message = "Ваша робота коштуватиме " + str(
        amount) + " грн. Для підтвердження внесіть аванс у розмірі 10% і протягом 24 годин ми надішлемо вам план вашого завдання для узгодження з викладачем."

# Check if the task requires a plan
if task_type == "diploma thesis" or task_type == "term paper" or task_type == "master's thesis" or task_type == "bachelor's thesis":
    # Ask the person to make a partial payment to confirm the task
    bot_message = "Після перевірки вашого авансу, ми надішлемо вам ваш план роботи."
else:
    # Ask the person to make a full payment to confirm the task
    bot_message = "Маю перевірити вашу оплату."

# Check if the task requires a plan
def send_messager(client_id, bot_message):
    pass

def has_partial_payment(person_id):
    # Check if the person has made a partial payment for their task
    # (implementation details omitted for brevity)
    return True  # replace with actual implementation

def attach_link(bot_message, link):
    # Attach the link to the bot message
    bot_message += f"\n\nПосилання на частину роботи: {link}"
    return bot_message  # return the updated bot message

    # Define the missing functions here
    def has_partial_payment(person_id):
        # Check if the person has made a partial payment for their task
        # (implementation details omitted for brevity)
        return True  # replace with actual implementation

    def attach_link(bot_message, link):
        # Attach the link to the bot message
        bot_message += f"\n\nПосилання на частину роботи: {link}"
        return bot_message  # return the updated bot message

    # Check if the task type is a diploma, term paper, master's thesis, or bachelor's thesis
    if task_type in ["diploma thesis", "term paper", "master's thesis", "bachelor's thesis"]:
        # Check if the person has made a partial payment
        if has_partial_payment(person_id):
            # Send a message with a link to the completed part of the task
            bot_message = "Частина вашої роботи виконана і ви можете її переглянути за посиланням ..."
            # Attach the link to the completed part of the task
            bot_message = attach_link(bot_message, "http://link-to-the-completed-task.com")
            # Send the message to the person
            send_message(person_id, bot_message, parse_mode=ParseMode.HTML)
    else:
        # perform actions for other types of tasks
        task_details = get_task_details()
        # ... rest of the code follows

        # Send a message with a link to the completed part of the task
        bot_message = "Частина вашої роботи виконана і ви можете її переглянути за посиланням ..."
        # Attach the link to the completed part of the task
        attach_link(bot_message, "http://link-to-the-completed-task.com")
        # Send the message to the person
        send_messager(client_id, bot_message)

    # Download the task
    download_task(task_type, task_details)
    # Send a message to the person
    bot_message = "Ваша робота готова до завантаження. Ви можете завантажити її за посиланням ..."
    # Attach the download link
    attach_link(bot_message, "http://download-link.com")
    # Send the message to the person
    send_message(person, bot_message)

    if has_partial_payment(person):
        # Attach two buttons - Paid and Not Paid
        attach_buttons(bot_message, ["Оплачено", "Неоплачено"])
        # Send the message to the person
        send_message(person, bot_message)
    else:
        # Check if the task is fully completed and ready for download
        if is_task_ready(task_type, task_details):
            # Send a message to the person
            bot_message = "Ви успішно отримали доступ до завантаження вашої роботи."
            send_message(person, bot_message)
        else:
            # Check if there are any other tasks ready without a plan
            if has_ready_task_without_plan():
                # Do something
                pass
            else:
                # Do something else
                pass

            # Send a message with a link to the ready task
            bot_message = "Ваша робота готова до завантаження за посиланням ..."
            # Attach the link to the completed task
            attach_link(bot_message, "http://link-to-the-ready-task.com")
            # Send the message to the person
            send_message(person, bot_message)
# закриття курсора та з'єднання з базою даних
cur.close()
conn.close()
