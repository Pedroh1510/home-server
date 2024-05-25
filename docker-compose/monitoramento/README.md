## Telegraf

- instalar o smartctl
  ```sh
  docker exec -it -u root telegraf bash
  apt update
  apt install smartmontools
  ```
- configurar o [sudoers](https://www.thegeekdiary.com/visudo-command-not-found/) para o [telegraf](https://github.com/influxdata/telegraf/blob/master/plugins/inputs/smart/README.md#permissions)
