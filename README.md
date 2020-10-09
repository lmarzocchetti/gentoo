# dio

**1) crea un profilo** <br/>
\# useradd -m -G wheel -s /bin/bash dio<br/>
\# passwd dio<br/>
**2) autorizza i privilegi da amministratore su quel profilo** <br/>
\# EDITOR=nano visudo<br/>
usa CTRL+W per cercare "#wheel ALL=(ALL) ALL"<br/>
elimina il "#" davanti a wheel<br/>
CTRL+O, ENTER, CTR+X per salvare<br/>
CTRL+D per uscire dal profilo root ed entrare con quello appena creato (dio)<br/>
**3) installa i driver grafici, la WM, e varie robe utili** <br/>
\# sudo pacman -S xf86-video-nouveau xorg-server xorg-xinit i3 i3status rxvt-unicode ttf-liberation dmenu firefox emacs feh compton unclutter git<br/>
usando sudo sfrutti dei privilegi da amministratore quindi ti chiederà di inserire la password (quella dell'account corrente non del root)<br/>
**4) scarica i vari file delle configurazioni**<br/>
\# git clone https://github.com/lmarzocchetti/gentoo<br/>
**5) copiali nei loro posti**<br/>
\#cp dio/.xinitrc ~/<br/>
\#cp dio/.Xdefaults ~/<br/>
\#cp -r dio/.config ~/ <br/>
\#cp -r dio/.wall ~/<br/>
**6) avvia la Window Manager**<br/>
\#startx<br/>

<h2>lista comandi </h2>

**- Win = Windows key** <br/>
**- s=s mentre S=Shift+s**<br/>
Win+ENTER = apri finestra terminale<br/>
Win+q = chiudi la finestra che sta in focus<br/>
Win+p = apri dmenu (launcher dei programmi)<br/>
Win+h = sposta il focus alla finestra di sinistra<br/>
Win+j = sposta il focus alla finestra di sotto<br/>
Win+k = sposta il focus alla finestra di sopra<br/>
Win+l = sposta il focus alla finestra di destra<br/>
Win+H = sposta la finestra in focus a sinistra</br>
Win+J = sposta la finestra in focus sotto</br>
Win+K = sposta la finestra in focus sopra</br>
Win+L = sposta la finestra in focus a destra</br>
Win+1 = vai alla workspace n. 1 (puoi usare numeri da 1 a 9 e 0)</br>
Win+Shift+1 = sposta la finestra in focus alla workspace n.1 (come prima, puoi usare numeri da 1 a 9 e 0)</br>
Win+f = schermo pieno</br>
Win+Shift+Spazio = cambia modalità da Tiling a Floating e viceversa</br>
Win+e = apri emacs su una finestra terminale<br/>
Win+E = apri emacs con la sua GUI<br/>
Win+w = apri firefox<br/>
Win+m = alza il volume<br/>
Win+M = abbassa il volume<br/>
Win+g = aumenta spazio far finestre<br/>
Win+G = diminuisci spazio far finestre<br/>
Win+t = fai tornare lo spazio fra finestre default<br/>
Win+T = togli tutto lo spazio fra finestre<br/>
Win+Q = esci dalla WM<br/>

<h2>file che potranno esserti utili</h2>
~/.xinitrc<br/>
file configurazione del server xorg<br/>
~/.Xdefaults<br/>
file configurazione del terminal urxvt<br/>
~/.config/i3/config<br/>
file configurazione di i3, la WM<br/>
~/.config/i3status/config<br/>
file configurazione della barra di i3status, la barra di informazioni che trovi in alto<br/>
~/.wall/wall1.jpg 
immagine di sfondo
