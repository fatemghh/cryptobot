import telebot
import cryptocompare
from telebot import TeleBot,types
from datetime import datetime

token=""
text_menu=" /btc bitcoin \n /eth eter \n /shib"
bot=telebot.TeleBot(token)
print("bot is run")
@bot.message_handler(commands=['start'])
def start (msg):
        
        btne=types.InlineKeyboardButton("English", callback_data="english")
        btnp=types.InlineKeyboardButton("Persian",callback_data="persian")
        btns=types.InlineKeyboardMarkup(row_width=3)
        btns.add(btne,btnp)
        bot.send_message(msg.chat.id,"Hi\n Choose your language before starting ",reply_markup=btns)
@bot.message_handler(commands=['datep'])
def time (msg):
    time=datetime.now()
    bot.reply_to(msg,f"   تاریخ و ساعت امروز⏰:  {time}")


@bot.message_handler(commands=['date'])
def time (msg):
    time=datetime.now()
    bot.reply_to(msg,f"Today's date and time⏰:  {time}")

@bot.message_handler(commands=['selectp'])
def select (msg):
    btc=types.InlineKeyboardButton("بیت کوین",callback_data="btc")
    eth=types.InlineKeyboardButton("اتریوم", callback_data="eth")
    shib=types.InlineKeyboardButton("شیبا", callback_data="shib")
    ltc=types.InlineKeyboardButton("لاین کوین", callback_data="ltc")
    usdt=types.InlineKeyboardButton("تتر",callback_data="usdt")
    xrp=types.InlineKeyboardButton("ریپل",callback_data="xrp")
    bch=types.InlineKeyboardButton("بیت کوین کش",callback_data="bch")
    bnb=types.InlineKeyboardButton("بایننس کوین",callback_data="bnb")
    eos=types.InlineKeyboardButton("ایاس",callback_data="eos")
    xlm=types.InlineKeyboardButton("استلار",callback_data="xlm")
    etc=types.InlineKeyboardButton("اتریوم کلاسیک",callback_data="etc")
    trx=types.InlineKeyboardButton("ترون",callback_data="trx")
    doge=types.InlineKeyboardButton("دوج کوین",callback_data="doge")
    uni=types.InlineKeyboardButton("یونی سواپ",callback_data="uni")
    dai=types.InlineKeyboardButton("دای",callback_data="dai")
    link=types.InlineKeyboardButton("چین لینک",callback_data="link")
    dot=types.InlineKeyboardButton("پولکادات",callback_data="dot")
    aave=types.InlineKeyboardButton("آوه",callback_data="aave")
    ada=types.InlineKeyboardButton("کاردانو",callback_data="ada")
    ftm=types.InlineKeyboardButton("فانتوم",callback_data="ftm")
    btns=types.InlineKeyboardMarkup()
    btns.add(btc,eth,shib,ltc,usdt,xrp,bch,bnb,eos,xlm,etc,trx,doge,uni,dai,link,dot,aave,ada,ftm)
    bot.send_message(msg.chat.id," نمایش رمز و ارز ها💰",reply_markup=btns)
    
@bot.message_handler(commands=['allp'])
def btc_price (user):
    username=user.from_user.username
    text=user.text
    id=user.chat.id
    bot.reply_to(user,"صبر کنید...")

    btc_price=cryptocompare.get_price("BTC",currency='USD')["BTC"]['USD']
    eth_price=cryptocompare.get_price("ETH",currency='USD')["ETH"]['USD']
    shib_price=cryptocompare.get_price("SHIB",currency='USD')["SHIB"]['USD']
    ltc_price=cryptocompare.get_price("LTC",currency='USD')["LTC"]['USD']
    usdt_price=cryptocompare.get_price("USDT",currency='USD')["USDT"]['USD']
    xrp_price=cryptocompare.get_price("XRP",currency='USD')["XRP"]['USD']
    bch_price=cryptocompare.get_price("BCH",currency='USD')["BCH"]['USD']
    bnb_price=cryptocompare.get_price("BNB",currency='USD')["BNB"]['USD']
    eos_price=cryptocompare.get_price("EOS",currency='USD')["EOS"]['USD']
    xlm_price=cryptocompare.get_price("XLM",currency='USD')["XLM"]['USD']
    etc_price=cryptocompare.get_price("ETC",currency='USD')["ETC"]['USD']
    trx_price=cryptocompare.get_price("TRX",currency='USD')["TRX"]['USD']
    doge_price=cryptocompare.get_price("DOGE",currency='USD')["DOGE"]['USD']
    uni_price=cryptocompare.get_price("UNI",currency='USD')["UNI"]['USD']
    dai_price=cryptocompare.get_price("DAI",currency='USD')["DAI"]['USD']
    link_price=cryptocompare.get_price("LINK",currency='USD')["LINK"]['USD']
    dot_price=cryptocompare.get_price("DOT",currency='USD')["DOT"]['USD']
    aave_price=cryptocompare.get_price("AAVE",currency='USD')["AAVE"]['USD']
    ada_price=cryptocompare.get_price("ADA",currency='USD')["ADA"]['USD']
    ftm_price=cryptocompare.get_price("FTM",currency='USD')["FTM"]['USD']
    bot.send_message(id, f"نمایش همه رمز و ارز ها💸\n\n بیت کوین ==> {btc_price}\nاتریوم ==> {eth_price}\nشیبا ==> {shib_price}\nلایت کوین ==> {ltc_price}\nتتر ==> {usdt_price}\nریپل ==> {xrp_price}\nبیت کوین کش ==> {bch_price}\nبایننس کوین ==> {bnb_price}\nایاس ==> {eos_price}\nاستلار ==> {xlm_price}\nاتریوم کلاسیک ==> {etc_price}\nترون ==> {trx_price}\nدوج کوین ==> {doge_price}\nیونی سواپ ==> {uni_price}\nدای ==> {dai_price}\nچین لینک ==> {link_price}\nپولکادات ==> {dot_price}\nآوه ==> {aave_price}\nکاردانو ==> {ada_price}\nفانتوم ==> {ftm_price}")
  
@bot.message_handler(commands=['select'])
def select (msg):
    btc=types.InlineKeyboardButton("BTC",callback_data="btc")
    eth=types.InlineKeyboardButton("ETH", callback_data="eth")
    shib=types.InlineKeyboardButton("SHIB", callback_data="shib")
    ltc=types.InlineKeyboardButton("LTC", callback_data="ltc")
    usdt=types.InlineKeyboardButton("USDT",callback_data="usdt")
    xrp=types.InlineKeyboardButton("XRP",callback_data="xrp")
    bch=types.InlineKeyboardButton("BCH",callback_data="bch")
    bnb=types.InlineKeyboardButton("BNB",callback_data="bnb")
    eos=types.InlineKeyboardButton("EOS",callback_data="eos")
    xlm=types.InlineKeyboardButton("XLM",callback_data="xlm")
    etc=types.InlineKeyboardButton("ETC",callback_data="etc")
    trx=types.InlineKeyboardButton("TRX",callback_data="trx")
    doge=types.InlineKeyboardButton("DOGE",callback_data="doge")
    uni=types.InlineKeyboardButton("UNI",callback_data="uni")
    dai=types.InlineKeyboardButton("DAI",callback_data="dai")
    link=types.InlineKeyboardButton("LINK",callback_data="link")
    dot=types.InlineKeyboardButton("DOT",callback_data="dot")
    aave=types.InlineKeyboardButton("AAVE",callback_data="aave")
    ada=types.InlineKeyboardButton("ADA",callback_data="ada")
    ftm=types.InlineKeyboardButton("FTM",callback_data="ftm")
    btns=types.InlineKeyboardMarkup()
    btns.add(btc,eth,shib,ltc,usdt,xrp,bch,bnb,eos,xlm,etc,trx,doge,uni,dai,link,dot,aave,ada,ftm)
    bot.send_message(msg.chat.id," Show Cryptocurrency💰",reply_markup=btns)
    

@bot.message_handler(commands=['help'])
def help (msg):
    bot.reply_to(msg, "Help!\n You can access any of the options using the created parameters.\nYou can view the price of currencies in dollars, of course, this view can be general or individual which you can choose according to your needs")

@bot.callback_query_handler(func=lambda call:True)
def callback_query(call):
    if call.data == "english":
        bot.send_message(call.message.chat.id , "Hi\nFor quick access to cryptocurrencies, click /select 💸\nAnd click to see the list of /all digital currencies")
    elif call.data == "persian":
        bot.send_message(call.message.chat.id , "سلام\n /selectp برای دسترسی سریع به ارزهای رمزنگاری شده انتخاب  را کلیک کنید💸\n /allp و برای دیدن همه لیست ارزهای دیجیتال کلیک کنید \n  /datep تاریخ و ساعت امروز ")
       
    elif call.data =="btc":
        
        btc_price=cryptocompare.get_price("BTC",currency='USD')["BTC"]['USD']
        bot.send_message(call.message.chat.id ,f"  بیت کوین-BTC==>{btc_price}dollar")

    elif call.data =="eth":

        eth_price=cryptocompare.get_price("ETH",currency='USD')["ETH"]['USD']
        bot.send_message(call.message.chat.id , f" اتریوم-ETH==>{eth_price}dollar")

    elif call.data =="shib":
        shib_price=cryptocompare.get_price("SHIB",currency='USD')["SHIB"]['USD']
        bot.send_message(call.message.chat.id , f" شیبا-SHIB==>{shib_price}dollar")
    elif call.data =="ltc":
        ltc_price=cryptocompare.get_price("LTC",currency='USD')["LTC"]['USD']
        bot.send_message(call.message.chat.id , f" لاین کوین-LTC==>{ltc_price}dollar")
    elif call.data =="usdt":
        usdt_price=cryptocompare.get_price("USDT",currency='USD')["USDT"]['USD']
        bot.send_message(call.message.chat.id , f" تتر-USDT==>{usdt_price}dollar")
    elif call.data =="xrp":
        xrp_price=cryptocompare.get_price("XRP",currency='USD')["XRP"]['USD']
        bot.send_message(call.message.chat.id , f" ریپل-XRP==>{xrp_price} dollar")
    elif call.data =="bch":

        bch_price=cryptocompare.get_price("BCH",currency='USD')["BCH"]['USD']
        bot.send_message(call.message.chat.id , f" بیت کوین کش-BCH==>{bch_price}dollar")
    elif call.data =="bnb":

        bnb_price=cryptocompare.get_price("BNB",currency='USD')["BNB"]['USD']
        bot.send_message(call.message.chat.id , f" بایننس کوین-BNB==>{bnb_price}dollar")
    elif call.data =="eos":

        eos_price=cryptocompare.get_price("EOS",currency='USD')["EOS"]['USD']
        bot.send_message(call.message.chat.id , f" ایاس-EOS==>{eos_price}dollar")
    elif call.data =="xlm":

        xlm_price=cryptocompare.get_price("XLM",currency='USD')["XLM"]['USD']
        bot.send_message(call.message.chat.id , f" استلار-XLM==>{xlm_price}dollar")
    elif call.data =="etc":

        etc_price=cryptocompare.get_price("ETC",currency='USD')["ETC"]['USD']
        bot.send_message(call.message.chat.id , f" اتریوم کلاسیک-ETC==>{etc_price}dollar")
    elif call.data =="trx":

        trx_price=cryptocompare.get_price("TRX",currency='USD')["TRX"]['USD']
        bot.send_message(call.message.chat.id , f" ترون-TRX==>{trx_price}dollar")
    elif call.data =="doge":

        doge_price=cryptocompare.get_price("DOGE",currency='USD')["DOGE"]['USD']
        bot.send_message(call.message.chat.id , f" دوج کوین-DOGE==>{doge_price}dollar")
    elif call.data =="uni":

        uni_price=cryptocompare.get_price("UNI",currency='USD')["UNI"]['USD']
        bot.send_message(call.message.chat.id , f" یونی سواپ-UNI==>{uni_price}dollar")
    elif call.data =="dai":

        dai_price=cryptocompare.get_price("DAI",currency='USD')["DAI"]['USD']
        bot.send_message(call.message.chat.id , f" دای-DAI==>{dai_price}dollar")
    elif call.data =="link":

        link_price=cryptocompare.get_price("LINK",currency='USD')["LINK"]['USD']
        bot.send_message(call.message.chat.id , f" چین لینک-LINK==>{link_price}dollar")
    elif call.data =="dot":

        dot_price=cryptocompare.get_price("DOT",currency='USD')["DOT"]['USD']
        bot.send_message(call.message.chat.id , f" پولکادات-DOT==>{dot_price}dollar")
    elif call.data =="aave":

        aave_price=cryptocompare.get_price("AAVE",currency='USD')["AAVE"]['USD']
        bot.send_message(call.message.chat.id , f" آوه-AAVE==>{aave_price}dollar")
    elif call.data =="ada":

        ada_price=cryptocompare.get_price("ADA",currency='USD')["ADA"]['USD']
        bot.send_message(call.message.chat.id , f" کاردانو-ADA==>{ada_price}dollar")
    elif call.data =="ftm":

        ftm_price=cryptocompare.get_price("FTM",currency='USD')["FTM"]['USD']
        bot.send_message(call.message.chat.id , f" فانتوم-FTM==>{ftm_price}dollar")

@bot.message_handler(commands=['all'])
def btc_price (user):
    username=user.from_user.username
    text=user.text
    id=user.chat.id
    bot.reply_to(user,"wait...")

    btc_price=cryptocompare.get_price("BTC",currency='USD')["BTC"]['USD']
    eth_price=cryptocompare.get_price("ETH",currency='USD')["ETH"]['USD']
    shib_price=cryptocompare.get_price("SHIB",currency='USD')["SHIB"]['USD']
    ltc_price=cryptocompare.get_price("LTC",currency='USD')["LTC"]['USD']
    usdt_price=cryptocompare.get_price("USDT",currency='USD')["USDT"]['USD']
    xrp_price=cryptocompare.get_price("XRP",currency='USD')["XRP"]['USD']
    bch_price=cryptocompare.get_price("BCH",currency='USD')["BCH"]['USD']
    bnb_price=cryptocompare.get_price("BNB",currency='USD')["BNB"]['USD']
    eos_price=cryptocompare.get_price("EOS",currency='USD')["EOS"]['USD']
    xlm_price=cryptocompare.get_price("XLM",currency='USD')["XLM"]['USD']
    etc_price=cryptocompare.get_price("ETC",currency='USD')["ETC"]['USD']
    trx_price=cryptocompare.get_price("TRX",currency='USD')["TRX"]['USD']
    doge_price=cryptocompare.get_price("DOGE",currency='USD')["DOGE"]['USD']
    uni_price=cryptocompare.get_price("UNI",currency='USD')["UNI"]['USD']
    dai_price=cryptocompare.get_price("DAI",currency='USD')["DAI"]['USD']
    link_price=cryptocompare.get_price("LINK",currency='USD')["LINK"]['USD']
    dot_price=cryptocompare.get_price("DOT",currency='USD')["DOT"]['USD']
    aave_price=cryptocompare.get_price("AAVE",currency='USD')["AAVE"]['USD']
    ada_price=cryptocompare.get_price("ADA",currency='USD')["ADA"]['USD']
    ftm_price=cryptocompare.get_price("FTM",currency='USD')["FTM"]['USD']
    bot.send_message(id, f"Show all cryptocurrencies💸\n\n BTC ==> {btc_price}\nETH ==> {eth_price}\nSHIB ==> {shib_price}\nLTC ==> {ltc_price}\nUSDT ==> {usdt_price}\nXRP ==> {xrp_price}\nBCH ==> {bch_price}\nBNB ==> {bnb_price}\nEOS ==> {eos_price}\nXLM ==> {xlm_price}\nETC ==> {etc_price}\nTRX ==> {trx_price}\nDOGE ==> {doge_price}\nUNI ==> {uni_price}\nDAI ==> {dai_price}\nLINK ==> {link_price}\nDOT ==> {dot_price}\nAAVE ==> {aave_price}\nADA ==> {ada_price}\nFTM ==> {ftm_price}")
    

bot.polling()
