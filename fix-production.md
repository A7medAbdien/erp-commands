I will reset the porduction configration

```sh
sudo bench setup production [frappe-user]
```

if you faced an issue with nignx

check the status
```sh
sudo systemctl status nginx
```
if disabled, start it
```sh
sudo systemctl start nginx
```
then re configure the porduction

```sh
sudo bench setup production [frappe-user]
```

all
```sh
sudo bench setup production frappe
sudo systemctl status nginx
sudo systemctl start nginx
sudo bench setup production frappe
```
