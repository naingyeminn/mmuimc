install:
	wget http://packages.sil.org/sil-repository.deb -O sil-repository.deb
	dpkg -i sil-repository.deb
	apt-get update
	apt-get install -y ibus-kmfl
	cp -fv ./src/keyboards/*.kmn /usr/share/kmfl
	cp -fv ./src/icons/*.bmp /usr/share/kmfl/icons

uninstall:
	rm -fv /usr/share/kmfl/*.kmn
	rm -fv /usr/share/kmfl/icons/*.bmp
	apt-get purge -y ibus-kmfl
	apt-get purge -y sil-repository

.PHONY: install uninstall
