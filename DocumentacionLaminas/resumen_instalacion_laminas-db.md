# Instalación del componente `laminas/laminas-db` con Composer

**Resumen breve:** se crea un proyecto PHP en Windows, se consulta la documentación oficial de Laminas y se usa Composer para instalar el componente `laminas-db`, verificando al final que quedó correctamente registrado.

## Pasos

**1. Verificar el entorno**
Abrir la terminal (CMD) y ejecutar `php -v` para confirmar que PHP está instalado (versión 8.2.12).

![Verificación de PHP](imagenes/01_php_version.png)

**2. Crear la carpeta del proyecto**
En el Explorador de Windows, dentro de `Documentos`, crear la ruta `optativa\7e\php` para alojar el proyecto.

![Creación de carpeta del proyecto](imagenes/02_crear_carpeta.png)

**3. Revisar los comandos de Composer**
En la terminal ejecutar `composer` (sin argumentos) para ver el listado de comandos disponibles.

![Ayuda de Composer](imagenes/03_composer_help.png)

**4. Consultar la documentación de Laminas**
Entrar al sitio oficial **getlaminas.org** y revisar la sección de componentes (Cache, Db, Gestor de eventos, etc.), hasta llegar a la guía de instalación de `Laminas\Db`.

![Sitio de documentación de Laminas](imagenes/04_sitio_laminas.png)
![Documentación de componentes](imagenes/05_docs_componentes.png)

**5. Instalar el paquete**
Dentro de la carpeta del proyecto, ejecutar:
```
composer require laminas/laminas-db
```

![Ejecución del comando composer require](imagenes/06_composer_require.png)
![Composer actualizando composer.json e instalando dependencias](imagenes/07_composer_output.png)

**6. Verificar los archivos generados**
Ejecutar `dir` y confirmar que se crearon `composer.json`, `composer.lock` y la carpeta `vendor`.

![Verificación de archivos con dir](imagenes/08_dir.png)

**7. Confirmar el contenido de composer.json**
Ejecutar `type composer.json` y comprobar que el paquete quedó registrado:
```json
{
    "require": {
        "laminas/laminas-db": "^2.22"
    }
}
```

![Contenido final de composer.json](imagenes/09_composer_json.png)
