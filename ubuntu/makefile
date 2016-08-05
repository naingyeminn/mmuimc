install:
	wget http://packages.sil.org/sil.gpg
	apt-key add sil.gpg
	apt-add-repository "deb http://packages.sil.org/ubuntu/ $(lsb_release -sc) main"
	apt-get update
	apt-get install -y ibus-kmfl
	cp -fv ./src/keyboards/*.kmn /usr/share/kmfl
	cp -fv ./src/icons/*.bmp /usr/share/kmfl/icons

uninstall:
	rm -fv /usr/share/kmfl/*.kmn
	rm -fv /usr/share/kmfl/icons/*.bmp
	apt-get purge -y ibus-kmfl
	apt-add-repository --remove "deb http://packages.sil.org/ubuntu/ $(lsb_release -sc) main"

.PHONY: install uninstall
