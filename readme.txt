apt-get update
apt-get install git

install go
wget https://storage.googleapis.com/golang/go1.5.linux-amd64.tar.gz

tar -xzf go1.5.linux-amd64.tar.gz

vim /etc/profile

GOPATH="/YOUR/USER/HOME/go"
GOROOT="/usr/local/go"
PATH=$GOROOT/bin:$PATH

git clone go project(beego project)https://github.com/ghd214/beego-test.git

apt-get install supervisor

add the file
/etc/supervisor/conf.d/myapp.conf

[program:myapp]
command=/root/work/beego-test/beego-blog
directory=/root/work/beego-test
process_name=%(program_name)s
numprocs=1
autostart=true
autorestart=true

command

supervisord
supervisorctl
