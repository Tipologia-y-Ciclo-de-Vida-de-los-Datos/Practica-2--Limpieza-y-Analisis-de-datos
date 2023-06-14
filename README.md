
<div id="top"></div>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica-2--Limpieza-y-Analisis-de-datos">
    <img src="https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica-2--Limpieza-y-Analisis-de-datos/assets/57969201/80c8c9be-1fb8-4ced-8dc8-f49998c328c2" alt="Logo" width="390" height="130">
  </a>
  

<h1 align="center">Práctica 2 - Limpieza y Análisis de Datos</h3>

  <p align="center">
    En esta práctica, se ha complementado el dataset final de países extraído en la Práctica 1- Web scraping con el PIB anual y el SMI por país. Una vez conseguido, se ha procedido a la limpieza y análisis de los datos.
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>ÍNDICE</summary>
  <ol>
    <li>
      <a href="#sobre-los-datasets">Sobre los Datasets</a>
      <ul>
        <li><a href="#descripcioen-de-los-datasets">Descripción de los Datasets</a></li>
        <li><a href="#herramientas-y-librerias">Herramientas y Librerias utilizadas</a></li>
      </ul>
    </li>
    <li>
      <a href="#el-proyecto">El proyecto</a>
      <ul>
        <li><a href="#requisitos">Requisitos previos</a></li>
        <li><a href="#codigo-de-la-practica">Código de la Práctica</a></li>
      </ul>
    </li>    
    <li><a href="#contactos">Contactos</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Sobre los datasets

<div align="center">
<a href="https://www.expatistan.com/cost-of-living/index?ranking=1">
    <img src="https://user-images.githubusercontent.com/57969201/232224215-296bb7d1-10bb-4db9-b3b8-bdf1da25453c.png" alt="Page" width="670" height="580">
  </a>
</div>

### Descripción de los datasets

Expatistan es un <i>webpage</i> que nos ofrece una forma sencilla, intiutiva y eficaz de visualizar el coste de vida por ciudades y países. Además, también se pueden hacer comparativas entre ellos y cálcular tu salarios aproximado por ciudad actual y ciudad de destino. </br></br>

Par este proyecto nos centraremos en ampliar la extracción de datos sobre países que hicismos sobre Expatistan para la práctica 1 con los datos del PIB anual y SMI del <i>webpage</i> Datosmacro. De ahí que en el repositorio hayan dos datasets originales: `PIB_SMI_divisas.xlsx` y `cost_of_living_countries.csv`. Como dicen sus nombres, cada uno corresponde al tipo de datos que contienen y, con el notebook `Ampliaciones del dataset.ipynb` que se puede encontrar dentro del directorio `/code`, los fusionaremos para crear el dataset inicial de la práctica: `cost_of_living_countries_updated.csv`. Este dataset contiene las siguientes variables:

| cost_of_living_cities.csv  | Tipo de variable             | Explicación                                                                                      |
| -------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------------ |
| Ranking position           | int                          | Posición numérica del país o ciudad en el Raking de la web                                       |
| Country                    | chr                          | Nombre del país de originen de la ciudad o país al que se le hace el Web Scraping respectivamente|
| Category                   | chr                          | Nombre de la clasificación genérica que se le ha otorgado a un conjunto de `items`               |
| Items                      | chr                          | Objetos o servicioscuyos precios nos sirven para estimar el coste de vida por país o ciudad      |
| Original Currency          | chr                          | Nombre de la moneda usada por el país o ciudad a los que se ha aplicado el Web Scraping          |
| Original Currency Value    | chr                          | Valor de la moneda usada por el país o ciudad a los que se ha aplicado el Web Scraping           |
| Exchanged Currency         | chr                          | Nombre de la moneda usada para el cambio de divisa                                               |
| Exchanged Currency Value   | chr                          | Valor de la moneda usada para el cambio de divisa                                                |
| PIB anual                  | chr                          | Último valor deProducto Interior Bruto anual registrado por país en Euros                        |
| SMI (dolares)              | chr                          | Salario Mínimo Interprofesional por país en Dólares                                              |
|SMI (euros)                 | chr                          | Salario Mínimo Interprofesional por país en Euros                                                |

</br></br>
Una vez se lleve a cabo y se finalice la limpieza de los datos, este dataset final se guardará (apartado 3. Guardamos los datos pre-procesados) bajo el nombre `cost_of_living_countries_clean.csv`.


<p align="right">(<a href="#top">back to top</a>)</p>


<!-- herramientas-utilizadas -->
### Herramientas y Librerias utilizadas

* [Jupyter Notebook](https://jupyter.org/)
* [RStudio](https://posit.co/download/rstudio-desktop/)
* dplyr
* VIM
* readxl
* tidyr
* tinytex
* car
* caret
* vcd
* pROC
* pandas 
* mtranslate 

<p align="right">(<a href="#top">back to top</a>)</p>

## El proyecto

### Requisitos previos

1. Tener instalado Jupyter Notebook en local o una cuenta de alguna plataforma de servicio Cloud con python notebooks habilitados (Google Colab, Kaggle, etc.)
2. Tener python instalado en la máquina si se quiere usar el notebook en local.
3. Tener instalado RStudio y R en elocal junto con las librerías mencionadas en el punto anterior

### Código de la Práctica
Para pòder dar incio a la práctica, tenemos como primera parte el notebook `Ampliaciones del dataset.ipynb` en el directorio `/code`. Este notebook tendrá como función principal generar el dataset que usaremos a lo largo de la práctica: `cost_of_living_countries_updated.csv`. Sin embargo, como no era posible una unión directa de los datos del PIB anual y SMI con el dataset extraído en la primera práctica, se han llevado a cabo los isguinertes pasos:
1. Cargar las distintas hojas del dataset `PIB_SMI_divisas.xlsx`, una para el PIB y otra para los valores del SMI
2. Cargar el dataset original `cost_of_living_countries.csv`
3. Combinar los dataframes del punto 1 tomando como referencia la columna "Países"
4. Eliminar los espacios y caracteres especiales de la columna "Países" de cada dataframe del punto 1
5. Traducir los nombres de cada país del español al inglés
6. Renombrar la columna como "Country"
7. Fusionar el dataset original con los nuevos datos y guardar como `cost_of_living_countries_updated.csv`

En cuanto al código principal de la práctica, este se puede encontrar en el directorio `/source`, donde está el archivo rmd `PRA2_Data_cleaning_and_analysis.Rmd` que hemos generado el RStudio para hacer el informe interactivo resultante.


<p align="right">(<a href="#top">back to top</a>)</p>


<!-- CONTACT -->
## Contactos

Este proyecto ha sido llevado a cabo por:
1. José Luis Santos Durango - josant05@uoc.edu
2. María Isabel González Sánchez - mgonzalezsanchez19@uoc.edu

Contáctanos: [Miembros del equipo](https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping/graphs/contributors)


<p align="right">(<a href="#top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping.svg?style=for-the-badge
[contributors-url]: https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping.svg?style=for-the-badge
[forks-url]: https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping/network/members
[stars-shield]: https://img.shields.io/github/stars/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping.svg?style=for-the-badge
[stars-url]: https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping/stargazers
[issues-shield]: https://img.shields.io/github/issues/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping.svg?style=for-the-badge
[issues-url]: https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping/issues
[license-shield]: https://img.shields.io/github/license/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping.svg?style=for-the-badge
[license-url]: https://github.com/Tipologia-y-Ciclo-de-Vida-de-los-Datos/Practica1-Web_Scraping/blob/master/LICENSE.txt
