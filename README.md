# Creando un submodule de git 

Los submodules de git permiten incluir un repositorio en otro en cualquier ubicación. Incluir por ejemplo una librería de javascript, modelos etc en un proyecto web como un módulo permite funcionar con su última versión fácilmente, sin necesidad de preocuparse por sustituir versiones manualmente: basta actualizar el repositorio.



## AÑADIR UN MÓDULO A UN REPOSITORIO

Al añadir el primer módulo se crea en el repositorio principal el archivo .gitmodules, en el que se listan todos los módulos que se han añadido.

```bash
git submodule add git@bitbucket.org:###/### /<nombre-carpeta>
```

## CLONAR UN PROYECTO CON SUS SUBMODULES ACTUALIZADOS

```bash
git clone --recursive git@bitbucket.org:###/### <nombre-carpeta>
```

## PARA ACTUALIZAR EL REPOSITORIO 

```bash
Para actualizar debemos ingresar a la carpeta donde esta nuestro submodule y hacer git pull
```

```bash
git clone --recursive git@bitbucket.org:###/### <nombre-carpeta>
```

## PROBLEMAS

```

Algunos de los problemas mas usuales que se pueden presentar es que te hayas equivocado ingresando la ruta o algún parametro equivocado en este caso debemos eliminar el submodule 

```

```bash
1.Eliminar el archivo .gitmodules.
2.rm -rf .git/modules/<nombre-carpeta>
3.git rm --cached <nombre-carpeta>
```

## License
[MIT](https://choosealicense.com/licenses/mit/)
