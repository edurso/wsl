# wsl

contains some wsl notes and things

see [my dotfiles](https://github.com/edurso/dotfiles) for, you know, my dotfiles

## init system (PID 1)

```bash
ps -p 1 -o comm=
```

wsl uses SysV (not systemd) as its init system

here is a lookup table from
[somewhere on the internet](https://linuxhandbook.com/system-has-not-been-booted-with-systemd/)
that lists systemd commands and their sysv equivalents

| Systemd command | Sysvinit command |
|:---:|:---:|
| `systemctl start service_name` | `service service_name start` |
| `systemctl stop service_name` | `service service_name stop` |
| `systemctl restart service_name` | `service service_name restart` |
| `systemctl status service_name` | `service service_name status` |
| `systemctl enable service_name` | `chkconfig service_name on` |
| `systemctl disable service_name` | `chkconfig service_name off` |
