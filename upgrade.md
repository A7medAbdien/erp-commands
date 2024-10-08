# store everything

## update something and node

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

source ~/.bashrc

nvm install 18

nvm alias default 18
```

## refresh the cash

```sh
npm cache clean -f
npm install -g n
n stable
n latest
bench setup requirements --node
bench build
```

## upgrade

```sh
bench switch-to-branch version-15 frappe erpnext hrms --upgrade
```

## migrate

```sh
bench --site site1.local migrate
```

## install the apps mentioned in the migration

1. taxjar_integration

```sh
bench get-app https://github.com/frappe/taxjar_integration.git
bench --site site1.local install-app taxjar_integration
```

2. webshop - optional

```sh
bench get-app webshop
bench --site site1.local install-app webshop
```

3. KSA Vat

```sh
bench get-app https://github.com/8848digital/KSA.git
bench --site site1.local install-app ksa
```

## Restart the supervisor

```sh
sudo supervisorctl restart all
```

## Check version

```sh
bench version
```

# fix hrms issue

```sh
bench remove-app hrms
bench uninstall-app hrms
bench get-app https://github.com/frappe/hrms.git --branch version-15
bench install-app hrms
```

## Notes

IDK what it that

Clear `tabSingles` and Payment Reconciliation tables of values

# Sources

[How to Upgrade ERPNext from Version 14 to Version 15](https://codewithkarani.com/2024/01/03/how-to-upgrade-erpnext-from-version-14-to-version-15/)

[Refreshing the cash](https://github.com/A7medAbdien/ka_vehicle_maintenance)
