from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext
# Функция обработки команды /start
def start(update: Update, context: CallbackContext) -> None:
    update.message.reply_text('И вам добрый вечер.')

def main():
    # Замените 'YOUR_TOKEN' на ваш токен
    updater = Updater("7671450435:AAEHQDCjpoZvZzouYfvuHF1gO39829-1y_g")
    # Получаем диспетчер для регистрации обработчиков
    dispatcher = updater.dispatcher

    # Регистрируем обработчик команды /start
    dispatcher.add_handler(CommandHandler("start", start))

    # Запускаем бота
    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()
    
