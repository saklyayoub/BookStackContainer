# Custom BookStack docker-compose
This works only with precanceled **nginx reverse proxy** container under **bridgre network**

 - Create necessary directory
	 - `sudo mkdir mysql-data storage-uploads uploads`
	 - `sudo chmod -R 777 *`
 - Rename env.sample to .env
	 - `sudo mv env.sample .env`
	 - Edit .env with correct variables, we suggest strong password fro database on production environment generated from [https://passwordsgenerator.net/](https://passwordsgenerator.net/)
- Lunch your docker-compose file with 
	- `sudo docker-docker-compose up -d`

**PS: Default login user `admin@admin.com` and password `password`**

If at first lunching `bookstack` crash then do those steps
- leave `mysql container` continue initializing sequence
- Then shutdown `docker-compose sudo docker-compose down`
- Grant again permissions `sudo chmod -R 777 *`
- Lunch again docker-compose `sudo docker-compose up -d` 

