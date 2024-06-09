## Telegraf

- instalar o smartctl
  ```sh
  docker exec -it -u root telegraf bash
  apt update && apt install smartmontools sudo nano -y
  sudo EDITOR=nano visudo
  ```
- configurar o [sudoers](https://www.thegeekdiary.com/visudo-command-not-found/) para o [telegraf](https://github.com/influxdata/telegraf/blob/master/plugins/inputs/smart/README.md#permissions)

```
Cmnd_Alias SMARTCTL = /usr/sbin/smartctl
telegraf  ALL=(ALL) NOPASSWD: SMARTCTL
Defaults!SMARTCTL !logfile, !syslog, !pam_session
```
