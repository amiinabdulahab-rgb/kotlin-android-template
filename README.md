from telegram import Update
from telegram.ext import Application, CommandHandler, ContextTyp
TOKEN = "fO         "

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text(
        "Akkam! 👋\n"
        "Ani Mana Maxxansaa Gadaa Carcar Bot dha 🤖"
    )

app = Application.builder().token(TOKEN).build()

app.add_handler(CommandHandler("start", start))

print("Bot hojjachaa jira...")
app.run_polling()