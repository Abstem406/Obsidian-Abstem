
como root en la vps
```bash
adduser nuevo_usuario
```
### 🔑 **Dar permisos de sudo (opcional)**

```bash
usermod -aG sudo nuevo_usuario   # Para Ubuntu/Debian
usermod -aG wheel nuevo_usuario  # Para CentOS/RHEL
```
