# xampp-autostart
Membuat xampp service autostart saat system booting

>Test di Debian/Ubuntu base, base lain coba aja


## Indonesia:
### Via Git clone :
Clone Repositori ini :
```
git clone https://github.com/Ipeng13/xampp-autostart.git
```

Masuk ke folder 'xampp-autostart' :

```
cd ~/xampp-autostart
```

Copy file xampp.service :
```
sudo cp xampp.service /etc/systemd/system/
```
Lalu jalankan perintah ini :

```
systemctl enable xampp
```

Dan :

```
systemctl start xampp
```


### Manual
Buat file xampp.service

```
sudo nano /etc/systemd/system/xampp.service
```
 

Isi file tersebut dengan:

```
[Unit]
Description=XAMPP auto start by ServerOk.in

[Service]
ExecStart=/opt/lampp/lampp start
ExecStop=/opt/lampp/lampp stop
Type=forking

[Install]
WantedBy=multi-user.target
```
 

 

Lalu
```
systemctl enable xampp
```
Dan
```
systemctl start xampp
```
