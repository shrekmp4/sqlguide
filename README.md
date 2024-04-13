
# 💉SQL Full Guide 

Guía de como usar **SQL**
- [XAMPP INSTALL](#XAMPP)
- [BASICOS DE CODIGO](#BÁSICOS-DE-CÓDIGO)
- [SELECIONES](#SELECIONES)
- [AÑADIR DATOS](#AÑADIR-DATOS)



## XAMPP
Despúes de descargar en [Instalar Runner](https://www.apachefriends.org/es/download.html)
```bash
cd Descargas
```
Agrega permisos de ejecución al instalador
```bash
cd chmod +x xampp-linux-x64-7.2.12-0-installer.run
```
Inicia el instalador
```bash
sudo ./xampp-linux-x64-7.2.12-0-installer.run
```
Una vez lo instales puedes iniciar los servicios a través de su ruta.
```bash
cd /opt/lampp
sudo ./manager-linux-x64.run
```

## BÁSICOS-DE-CÓDIGO
Crear una base de datos.  **[+]🟢**
```sql
CREATE DATABASE DB1;
```
Crear una tabla con columnas. **[+]🟢**
```sql
CREATE TABLE ejemplo (
    id INT,
    nombre VARCHAR(50)
);
```
Eliminar una columa. **[-]🔴**
```sql
DROP TABLE ejemplo;
```
Eliminar una _base de datos._ **[-]🔴**
```sql
DROP DATABASE ejemplo;
```
Agregar columnas a una tabla. **(Sigue la estructura)** **[+]🟢**
```sql
ALTER TABLE ejemplo
ADD correo VARCHAR(100),
    edad INT NULL DEFAULT 18;
```

Eliminar Columnas de una tabla. **[-]🔴**
```sql
ALTER TABLE ejemplo
DROP COLUMN correo; -- Esto es lo que eliminina las columnas 
```

## SELECCIONES 

Como selecionar datos en nuestras tablas/columnas. Si no sabes agregar datos debes leer

Seleccionar TODOS los datos de una columna  **[+]🟢**
```sql
SELECT * FROM usuarios
```

## AÑADIR-DATOS
