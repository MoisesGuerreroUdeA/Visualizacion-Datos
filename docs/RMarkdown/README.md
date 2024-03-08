# Instalación de RMarkdown desde cero sin usar RStudio

Para realizar la instalación de los paquetes necesarios primero se hace la instalación de R desde la página oficial accediendo al enlace [RProject](https://www.r-project.org/).

## Descarga e instalación de R

1. Hacemos clic en "download R"
2. Seleccionamos un CRAN mirror para la descarga (en mi caso lo hice con 
https://cloud.r-project.org/).
3. Descargamos R para el sistema operativo correspondiente (en mi caso selecciono Windows).
4. Abrimos el ejecutable correspondiente y realizamos la instalación
5. Adicionalmente es importante verificar que se tenga incluída la ruta de instalación **R_HOME/bin** al path para poder ejecutar los comandos de R desde línea de comandos.

## Configuración de RMarkdown

Para realizar la instalación de los componentes necesarios de RMarkdown se debe:

1. Abrir un nuevo terminal de línea de comandos (**como administrador**) y ejecutar el comando R. Para habilitar el entorno de línea de comandos de R.

```sh
R
```

2. Desde el entorno instalamos el paquete de RMarkdown por medio del comando

```R
install.packages('rmarkdown')
```

3. Instalamos el paquete tinytex para la compilación de archivos en formato PDF.

```R
install.packages("tinytex")
tinytex::install_tinytex()  # install TinyTeX
```

```R
rmarkdown::render('Monografia.Rmd', 'pdf_document')
```