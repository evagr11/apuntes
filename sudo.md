su -
usermod -aG sudo <usuario>

sudo visudo
usuario ALL=(ALL) NOPASSWD: ALL

dev_user ALL=(ALL) NOPASSWD: /usr/bin/apt, /usr/bin/npm, /usr/bin/docker
viewer_user ALL=(ALL) NOPASSWD: /usr/bin/cat /var/log/syslog, /usr/bin/journalctl
deploy_user ALL=(ALL) NOPASSWD: /bin/systemctl restart myapp, /usr/bin/git pull, /usr/bin/docker-compose up -d

