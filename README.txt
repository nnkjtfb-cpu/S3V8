╔══════════════════════════════════════════════════════════╗
   🔥 FREE 24/7 TELEGRAM BOT HOSTING - COMPLETE GUIDE 🔥
   📢 Channel: @testwithfahim
   👨‍💻 Owner: @FAHIM_TRADER1
╚══════════════════════════════════════════════════════════╝

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📦 এই ZIP ফাইলে কী কী আছে:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  1. bot.py          → মূল বট কোড
  2. requirements.txt → প্যাকেজ লিস্ট
  3. README.txt       → এই গাইড

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 1 — Webhostmost একাউন্ট খুলুন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  🌐 Website: https://webhostmost.com
  → Free Hosting সাইনআপ করুন
  → Email verify করুন
  → cPanel এ লগিন করুন

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 2 — Telegram Bot Token নিন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → Telegram এ @BotFather তে যান
  → /newbot লিখুন
  → Bot নাম ও username দিন
  → Token কপি করুন

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 3 — bot.py তে Token বসান
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → bot.py ফাইল খুলুন
  → BOT_TOKEN = "এখানে আপনার token বসান"
  → সেভ করুন

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 4 — Python App তৈরি করুন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → cPanel → Setup Python App
  → Create Application
  → Python Version: 3.11
  → Application Root: Pybot
  → Create বাটন চাপুন

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 5 — bot.py আপলোড করুন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → cPanel → File Manager
  → Pybot/Bot/ ফোল্ডার খুলুন
  → bot.py আপলোড করুন

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 6 — Package Install করুন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → cPanel → Terminal খুলুন
  → প্রথমে pip এর path খুঁজুন:

    find /home/$(whoami)/virtualenv -name "pip" 2>/dev/null

  → যা দেখাবে সেই path দিয়ে install করুন:

    /home/USERNAME/virtualenv/Pybot/3.11/bin/pip install pyTelegramBotAPI psutil requests

  ⚠️ USERNAME এর জায়গায় আপনার আসল username বসান
  ⚠️ username জানতে: echo $HOME

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 7 — প্রথমবার বট চালু করুন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → Terminal এ দিন:

    /home/USERNAME/virtualenv/Pybot/3.11/bin/python3 /home/USERNAME/Pybot/Bot/bot.py

  → Telegram এ /start দিন — কাজ করলে পরের ধাপে যান

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ STEP 8 — Cron Job সেট করুন (24/7 চালু রাখতে)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  → cPanel → Cron Jobs
  → সব ঘরে * রাখুন (Every Minute)
  → Command বক্সে দিন:

    /usr/bin/flock -n /tmp/bot.lock /home/USERNAME/virtualenv/Pybot/3.11/bin/python3 /home/USERNAME/Pybot/Bot/bot.py > /dev/null 2>&1

  → Add New Cron Job চাপুন ✅

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🛠️ দরকারি Commands
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  Username জানতে:      echo $HOME
  বট বন্ধ করতে:        pkill -f bot.py
  বট চলছে কিনা:        pgrep -f bot.py
  Lock file মুছতে:     rm -f /tmp/bot.lock
  bot.py খুঁজতে:       find /home/$(whoami) -name "bot.py" 2>/dev/null

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✅ BOT FEATURES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ✅ .py / .js / .zip ফাইল আপলোড
  ✅ Auto package install
  ✅ Start / Stop / Restart
  ✅ Real-time Logs
  ✅ CPU & RAM monitoring
  ✅ প্রতি user ১০টি ফাইল
  ✅ ২৪/৭ চালু থাকে

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📢 Channel: @testwithfahim
👨‍💻 Owner: @FAHIM_TRADER1
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
