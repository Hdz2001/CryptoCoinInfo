# CryptoCoinInfo
A program that gather necessary crypto coin infomation. such as current price, rank, historical data, etc

![image](https://user-images.githubusercontent.com/77633718/197381362-553bdb8f-c873-4bd5-9484-5aeef8b3866e.png)

**1. What are the inputs for the program?**
- input needed: coin name and coin code. For example: uquid coin and UQC. 
* Coin name: you can put any space before or after the name, or write in lower or upper case, but make sure each words of your coin name is separate by a space.
Eg: "    uquid coin  " or "   UqUid CoIn   "  are valid input, but not "uquidcoin" 
* Coin code: code of the coin, for example, BTC for Bitcoin or BNB for Binance. Space and lower/upper are still valid. 
- input will returns error messages if the coin or the code of the coin is not found.

**2. What information it will check?** 
So far: 
* price and rank: data colleted from coinmarketcap.com, using web scraping from beautifulsoup.
* historical data: data colleted from coinmarketcap.com, using CmcScraper from cryptocmd library and print the data out using panda.
Some coin code which doesn't exist still return the data, for example, if you input "a" as the code, you still have the data table.
I will add some conditional function later to avoid this.
* social links: check and return socials link, such as: 'Twitter', 'Facebook', 'Instagram', 'Telegram', 'Discord', 'Reddit'.
* scam check: data collected including safety score percentage from isthiscoinascam.com, using web scraping from beautifulsoup. 
Many datas are still in progress and will be added later on. 

**3. Downloading the .exe file:** 
* If you don't want extra work and just the .exe file, you can download from this link: https://drive.google.com/file/d/139auc5OGk0LX4t0-SMB4bLzkTjcmjaWB/view?usp=sharing because GitHub doesn't allow me to upload the file because of its size. No external libraries or environments installations needed. 
* Make sure to select trust the file and keep it so it will be downloaded to your PC. 
* Choose run anyway if any windows pop-up when you attempt to run the program. You might need to disable virus and security check if it doesn't allow. I will try to add signature to the file in the future to avoid those things.

**4. How to make .exe file from Windows?** 
If you want to explore and DIY, here is what i did:
* I made .exe file and custom the icon for the file using pyinstaller. 
* You either need to add pyinstaller to your PATH or go into pyinstaller source location in order to make the below code work. 
* My location for pyinstaller is: C:\Users\trann\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.8_qbz5n2kfra8p0\LocalCache\local-packages\Python38\Scripts <br />You can try to have a look yourself.
* Download the coin_info.py file and uquid.ico file to your computer, move them in the pyinstaller location if you didn't add pyinstaller as your PATH.

After doing 1 of those above, enter the code below: 
* pyinstaller.exe --onefile coin_info.py
<br />It will return the build and dist folders, along with SPEC file of coin_info and coin_info.exe will be in the dist folder. 
* pyinstaller.exe --onefile --icon=uquid.ico coin_info.py
<br />After that, run this code to add icon to the exe file, both outer and inner (windowed mode).
* Refer to this source: https://mborgerson.com/creating-an-executable-from-a-python-script/ if you want to understand more about how pyinstaller works.

You can move everything into 1 folder to keep track easier.
![image](https://user-images.githubusercontent.com/77633718/197322786-f96c979a-d9b3-4011-b6bf-a5a1842ab735.png)

**To sum up**:
<br />This is my personal project as I'm working for a crypto company - UQUID and I want to make keeping track of coin infos of our partners easier. 

Feel free to try it out and let me know if there are any errors occurred or what infos/features you guys want me to add into this project through my social medias. 

Have a great day and stay safe :) 
