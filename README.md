bot = commands.Bot(
    command_prefix="$", # $コマンド名　でコマンドを実行できるようになる
    case_insensitive=True, # コマンドの大文字小文字を区別しない ($hello も $Hello も同じ!)
    intents=intents # 権限を設定
)

@bot.event
async def on_ready():
    print("Bot is ready!")


@bot.event
async def on_message(message: discord.Message):
    """メッセージをおうむ返しにする処理"""

    if message.author.bot: # ボットのメッセージは無視
        return

    await message.reply(message.content)


bot.run("MTEzNzA0ODgxMDcxMTk0MTE1Mg.GBIzJX.HO26-Rqn4ZK-Q9UHL2xnyb8-GXmzr-ubWYSN8o)

#一般へメッセージを送信
