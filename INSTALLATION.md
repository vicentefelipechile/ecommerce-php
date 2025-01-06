# Pre-requisitos
Asegurate de que estes en el mismo directorio que el proyecto, por ejemplo:

### Windows:

    C:\Users\user\Documents\GitHub\ecommerce-php\...
    C:\ecommerce-php\...

### Linux:

    /home/user/Documents/GitHub/ecommerce-php/...
    /home/user/ecommerce-php/...

# Instalación
1. Clona el repositorio en tu máquina local.

```bash
git clone https://github.com/vicentefelipechile/ecommerce-php.git
```

2. Accede al directorio del proyecto.

```bash
cd ecommerce-php
```

3. Instala las dependencias del proyecto.

```bash
# npm / node
npm install

# composer
composer install
```

4. Copia el archivo `.env.example` y renombralo a `.env`.

```bash
cp .env.example .env
```

5. Genera la clave de la aplicación.

```bash
php artisan key:generate
```

6. Configura la base de datos en el archivo `.env`.

```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1 # localhost
DB_PORT=3306
DB_DATABASE=ecommerce_php
DB_USERNAME=root
DB_PASSWORD=
```

# Errores

### Error al instalar las dependencias de composer
En windows es muy probable que cuando esten instalando el proyecto en un nuevo equipo se encuentren con el siguiente error:

```
In Filesystem.php line 333:

Could not delete C:\Users\Publico\Documents\github\ecommerce-php/vendor/composer/ba74c2b9\Seldaek-monolog-aef6ee7\src\Monolog\Attribute:   

This can be due to an antivirus or the Windows Search Indexer locking the file while they are analyzed
```

Solución:

Ejecuta powershell como administrador y detén el servicio de Windows Search.

```sh
net stop wsearch
```