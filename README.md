# Aclaraciones

Para comentar que debido a las bajas especificaciones de mi computador no logre realizar la totalidad de validaciones solicitadas ya que constantemente se cerraba Android studio, logre caputrar algunos pantallazos al momento de que solicitaba al usuario los permisos antes que este se cerrara, en el caso de esta prueba permisos de localizacion, al momento de aprobarlos e ingresar o lanzar la aplicacion ya no los volvia a pedir, para solicitarlos nuevamente hay que ingresar al detalle de la misma y borrar cache para que nos lo vuelva a solicitar.

## Imagen https://prnt.sc/MmECQzgRAwwq


## Explicacion del Codigo

Declaramos el permiso que vamos a solicitar
```
String permiso = Manifest.permission.ACCESS_FINE_LOCATION;
```

Comprobamos si el permiso ya está concedido
```
int permisoConcedido = checkSelfPermission(permiso);
```

Si el permiso ya está concedido, la aplicación muestra un mensaje de confirmación
```
if (permisoConcedido == PackageManager.PERMISSION_GRANTED) {
    Toast.makeText(this, "Permiso concedido", Toast.LENGTH_SHORT).show();
}
```
Si el permiso no está concedido, la aplicación solicita el permiso al usuario
```
if (permisoConcedido != PackageManager.PERMISSION_GRANTED) {
    requestPermissions(new String[]{permiso}, 100);
}
```

Ya para finalizar comento que el metodo de requestPermission() eso le pide al usuario el permiso



Muchas gracias
