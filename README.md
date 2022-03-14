## PHP Docker Workspace
### This is docker workspace CR3. There's MySQL and FakeSMPT containers too.

#### Requirements
1. Docker
2. Docker Compose
3. Git

#### How to use
1. Clone or download this repo `git clone ssh://git@dwcgitlab.dwebsite.com:65534/cr/cr3-docker-workspace.git`
2. Go to cloned folder `cd cr3-docker-workspace`
3. Copy environtment file `cp .env.example .env`
4. Set your environtment in .env file. You can turn specify port, restart behaviour, and mysql credential.
5. All set! Run docker `docker-compose up`
6. Wait until the process is done, and Voila!
7. Congratulation

You can clone your CR3 or CR3-MnST app to directory **./web**, based on nginx vhost in this repository each app have these following directory:
- CR3: **./web/cr3-live** (`git clone ssh://git@dwcgitlab.dwebsite.com:65534/cr/CR3.git cr3-live`)
- MnST: **./web/cr3-mnscu** (`git clone ssh://git@dwcgitlab.dwebsite.com:65534/cr/crmnscu.git cr3-mnscu`)