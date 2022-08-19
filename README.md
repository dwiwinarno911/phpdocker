## PHP Docker Workspace
### This is docker workspace CR3. There's MySQL and FakeSMPT containers too.

#### Requirements
1. Docker
2. Docker Compose
3. Git

#### How to use
1. Clone or download this repo `git clone git@github.com:dwiwinarno911/phpdocker.git docker-workspace`
2. Go to cloned folder `cd r-workspace`
3. Copy environtment file `cp .env.example .env`
4. Set your environtment in .env file. You can turn specify port, restart behaviour, and mysql credential.
5. All set! Run docker `docker-compose up`
6. Wait until the process is done, and Voila!
7. Congratulation

You can clone your CR3 app to directory **./web**, based on nginx vhost in this repository each app have these following directory:
- CR3: **./web/cr3** (`git clone git@bitbucket.org:rschooltoday/rsp-crmnscu.git cr3`)


#### Use php version 
To use php version on this docker , you can change nginx vhost conf on `etc/nginx/default.conf`
this docker have 4 php version
1. php 5.6
2. php 7.0
3. php 7.4
4. php 8.0

You can use by change this pass on vhost 
1. php 5.6 `fastcgi_pass php5:9000;`
2. php 7.0 `fastcgi_pass php70:9000;`
2. php 7.4 `fastcgi_pass php74:9000;`
2. php 8.0 `fastcgi_pass php8:9000;`


#### Connect to database
To connect database on this docker you can use this config on yout app
1. MySQL 5.6 
	- host     = db
	- username = root
	- password = password
	- port     = 3306
2. MySQL 5.7
	- host     = db
	- username = root
	- password = password 
	- port     = 3306

Also you can connect this connection via SQL Yog or Another sql management app via 

1. MySQL 5.6 
	- host     = localhost
	- username = root
	- password = password
	- port     = 3306
2. MySQL 5.7
	- host     = localhost
	- username = root
	- password = password 
	- port     = 3307