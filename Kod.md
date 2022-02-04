from tkinter import *
from time import *        #kütüphanelerimizi İmport ediyoruz.
import datetime

root = Tk()
root.title('Python ile saat')    #Program başlığnı ayarladık.

def saat():
    text = strftime('%H:%M:%S')
    label.config(text=text)            #saatin fonksiyonunu yazdık.
    label.after(1000,saat)

label = Label(root,font=("ds-digital",100),background="black",foreground="white") #font,fontun boyutunu arkaplan ve yazı rengini ayarladık.
label.pack(anchor="center") #yazıyı ortaya ayarladık.

saat()         #fonksiyonu çağırdık ve loop'a aldık.
mainloop()
