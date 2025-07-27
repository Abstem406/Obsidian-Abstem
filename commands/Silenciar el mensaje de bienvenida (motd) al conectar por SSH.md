# Silenciar mensajes al conectar por SSH (Ubuntu 24.04)

Crear el fichero `.hushlogin` en el **home del usuario que desees** para que **no** aparezcan:

- `Last login: …`  
- `To run a command as administrator (user "root"), use "sudo <command>".`

```bash
sudo -u USUARIO touch /home/{USUARIO}/.hushlogin
```

# Archivos del sistema que generan el motd en Ubuntu 24.04

Ubicación estándar  
```bash
/etc/update-motd.d/
```


Scripts (orden alfanumérico, ejecutados por `run-parts`)  
| Nombre | Finalidad típica |
|--------|------------------|
| `00-header` | Línea “Welcome to Ubuntu …” |
| `10-help-text` | Enlaces a ayuda, Landscape, Ubuntu Pro |
| `50-landscape-sysinfo` | Carga, uso de disco, memoria, IPs, etc. |
| `50-motd-news` | Noticias dinámicas (puede mostrar anuncios) |
| `80-esm-apps` | Aviso sobre ESM Apps no habilitado |
| `80-livepatch` | Estado de Canonical Livepatch |
| `91-release-upgrade` | Aviso si hay nueva LTS disponible |
| `95-hwe-eol` | Mensaje sobre soporte de hardware |
| `98-fsck-at-reboot` | Aviso si se requiere `fsck` en el próximo arranque |
| `98-reboot-required` | “*** System restart required ***” |
| `99-contabo-banner` | Banner ASCII del proveedor (puede variar) |

Gestión rápida  
```bash
# Desactivar un script concreto
sudo chmod -x /etc/update-motd.d/50-motd-news

# Reactivarlo
sudo chmod +x /etc/update-motd.d/50-motd-news

# Ejecutar todos los scripts a mano (útil para pruebas)
sudo run-parts /etc/update-motd.d
```