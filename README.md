Replace Contents of the file 
```
/var/cache/yunohost/app_tmp_work_dirs/linkwarden_patch/upgrade with this file.
```

Then upgrade linkwarden with this command:
```
sudo yunohost app upgrade linkwarden --file=/var/cache/yunohost/app_tmp_work_dirs/linkwarden_patch
```
After upgrade use this commands:
```
cd /var/www/linkwarden
npx prisma migrate deploy
systemctl restart linkwarden
```
