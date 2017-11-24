# Установка DOS Box
Для начала необходимо установить DOSBox, скачать его можно либо здесь: [мой dropbox](https://www.dropbox.com/sh/par2aub6s2rd6b8/AACRqWabxHMqnVFZfdp6cUeoa?dl=0) или [здесь](https://www.google.ru/)

Я устанавливал на диск **C:\Program Files**

Так же вам понадобится сам Prolog, его можно так же скачать здесь [мой dropbox](https://www.dropbox.com/sh/lh6mk5r37or9mqr/AAAl3DBleqlKgtXhhiaIkhKXa?dl=0) или [здесь](https://www.google.ru/)

Папку Prolog я скопировал в **C:\/**

После установки запускаете **DOSBox.exe** появится такое окно:

![group](https://github.com/ivanleontev/prolog/blob/master/DOSBox%200.74%2C%20Cpu%20speed_%20%20%20%20%203000%20cycles%2C%20Frameskip%20%200%2C%20Program_%20%20%20DOSBOX%202017-11-25%2000.18.49.png)

Здесь нужно смонтировать Prolog

Листинг команд:
```bash
mount c C:/Prolog
C:
prolog.exe
```

![group](https://github.com/ivanleontev/prolog/blob/master/DOSBox%200.74%2C%20Cpu%20speed_%20%20%20%20%203000%20cycles%2C%20Frameskip%20%200%2C%20Program_%20%20%20DOSBOX%202017-11-25%2000.22.20.png)

Если всё прошло успешно, то у вас должно появиться окно компилятора, выглядит вот так:

![group](https://github.com/ivanleontev/prolog/blob/master/DOSBox%200.74%2C%20Cpu%20speed_%20%20%20%20%203000%20cycles%2C%20Frameskip%20%200%2C%20Program_%20%20%20PROLOG%202017-11-25%2000.25.15.png)

Пример программы взятой с просторов:

```prolog
predicates
	parent(String, String)
	male(String)
	female(String)
	brother(String, String)
	print
 clauses
 	parent("Tom","Jake").
 	parent("Janna","Jake").
	parent("Tom","Tim").
 	parent("Janna","Tim").
	male("Tom").
	male("Tim").
	male("Jake").
	female("Janna").
	
	brother(X,Y):-parent(Z,X), parent(Z,Y), male(X),X<>Y.
	print:-brother(X,Y), write(X,"- btar- ", Y), nl, fail.
```

Результат работы: 
![group](https://github.com/ivanleontev/prolog/blob/master/DOSBox%200.74%2C%20Cpu%20speed_%20%20%20%20%203000%20cycles%2C%20Frameskip%20%200%2C%20Program_%20%20%20PROLOG%202017-11-25%2000.35.24.png)
