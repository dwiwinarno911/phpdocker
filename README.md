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