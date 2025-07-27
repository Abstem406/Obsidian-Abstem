
1.  Añadimos un nuevo usuario a Ubuntu con la siguiente linea, recuerda sustituir "nuevoUsuario" por el nombre de usuario que deseas.
```bash
	sudo adduser nuevoUsuario
```

Esto te pedirá que crees una nueva contraseña para el usuario, y te pedirá más información sobre el mismo, la única información que es obligatoria es el la contraseña

2.  Añadir al nuevo usuario al grupo sudo:
```bash
	usermod -aG sudo nuevoUsuario
```

Normalmente queremos que el nuevo usuario tenga privilegios de administración, para ello **es necesario que lo añadamos al grupo de usuarios sudo**, el siguiente comando lo añade al grupo sudo, recuerda cambiar el texto "nuevoUsuario", por el nombre de usuario que acabas de añadir en el comando anterior

3.  Usar el nuevo usuario:
```bash
	su – nuevoUsuario
```