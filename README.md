# goss-onion-runkit-task

В качестве учебного задания необходимо было создать одностраничный .onion сайт, использующий runkit и выводящий имя студента, а также текущие дату и время с помощью библиотеки moment.

Использовался минимальный сервер на Fedora на платформе Vscale.

## Последовательность действий:

```bash
sudo dnf install nginx tor
sudo nano /etc/tor/torrc
# в файле выше были раскомментированы строки c HiddenServiceDir и HiddenServicePort
sudo systemctl start nginx
sudo systemctl start tor
cd /var/lib/tor/hidden_service
cat hostname
# 6ojxiuio3yfln2nhwfsj744ypucphtk2zkh77ai2wp4h6znjfgru3wyd.onion
cd /usr/share/nginx/html
# Далее index.html в директории был заменен на index.html из данного Github репозитория
```
