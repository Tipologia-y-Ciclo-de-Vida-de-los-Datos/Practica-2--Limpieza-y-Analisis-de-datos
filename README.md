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
    <img src="https://user-images.githubusercontent.com/57969201/232225800-5c7ecb7a-3f55-47cc-bd46-a94e17dfe6e2.png" alt="Logo" width="390" height="120">
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
      <a href="#sobre-el-proyecto">Sobre el proyecto</a>
      <ul>
        <li><a href="#herramientas-y-librerias-utilizadas">Herramientas y Librerias utilizadas</a></li>
      </ul>
    </li>
    <li>
      <a href="#inicio-del-proyecto">Incio del proyecto</a>
      <ul>
        <li><a href="#requisitos-previos">Requisitos previos</a></li>
      </ul>
    </li>
    <li><a href="#dataset-link">Dataset link</a></li>
    <li><a href="#contactos">Contactos</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Sobre el proyecto
<div align="center">
<a href="https://www.expatistan.com/cost-of-living/index?ranking=1">
    <img src="https://user-images.githubusercontent.com/57969201/232224215-296bb7d1-10bb-4db9-b3b8-bdf1da25453c.png" alt="Page" width="670" height="580">
  </a>
</div>

MODIFICAR PARA PONER AQUI UNA DESCRIPCION DEL PROYECTO

Expatistan es un <i>webpage</i> que nos ofrece una forma sencilla, intiutiva y eficaz de visualizar el coste de vida por ciudades y países. Además, también se pueden hacer comparativas entre ellos y cálcular tu salarios aproximado por ciudad actual y ciudad de destino. </br></br>

Par este proyecto nos centraremos en extraer los datos que hacer referencia a cada ciudad y país explicados por la página web. De ahí que en el repositorio hayan dos datasets extraídos: `cost_of_living_cities.csv` y `cost_of_living_countries.csv`. Como dicen sus nombres, cada uno corresponde al tipo de Web Scraping realizado en la página web y contendrán los siguinetes valores. 

| cost_of_living_cities.csv  | cost_of_living_countries.csv | Explicación                                                                                      |
| -------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------------ |
| Ranking position           | Ranking position             | Posición numérica del país o ciudad en el Raking de la web                                       |
| Country                    | Country                      | Nombre del país de originen de la ciudad o país al que se le hace el Web Scraping respectivamente|
| City                       | (No presenta esta columna)   | Nombre de la ciudad a la que se le está aplicando el Web Scraping                                |
| State                      | (No presenta esta columna)   | Nombre del estado, si lo presenta, de la ciudad a la que se le está aplicando el Web Scraping    |
| Category                   | Category                     | Nombre de la clasificación genérica que se le ha otorgado a un conjunto de `items`               |
| Items                      | Items                        | Objetos o servicioscuyos precios nos sirven para estimar el coste de vida por país o ciudad      |
| Original Currency          | Original Currency            | Nombre de la moneda usada por el país o ciudad a los que se ha aplicado el Web Scraping          |
| Original Currency Value    | Original Currency Value      | Valor de la moneda usada por el país o ciudad a los que se ha aplicado el Web Scraping           |
| Exchanged Currency         | Exchanged Currency           | Nombre de la moneda usada para el cambio de divisa                                               |
| Exchanged Currency Value   | Exchanged Currency Value     | Valor de la moneda usada para el cambio de divisa                                                |

</br></br>
Estos CSV se consiguen a partir del código explicado en el Jupyter notebook `Scraping-notebook.ipynb`, que contiene una pequeña introducción a la página web y el Web Scraping de Ciudades (clase `ExpatistanCityScraper()`) y de Países (clase `ExpatistanCountryScraper()`).




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

<p align="right">(<a href="#top">back to top</a>)</p>


### Requisitos previos

1. Tener instalado Jupyter Notebook en local o una cuenta de alguna plataforma de servicio Cloud con python notebooks habilitados (Google Colab, Kaggle, etc.)
2. Tener python instalado en la máquina si se quiere usar el notebook en local.
3. Tener instalado RStudio y R en elocal junto con las librerías mencionadas en el punto anterior

<!-- Dataset link -->
## Dataset link

NO SE SI SE NECESITA
- Cost of Living by Country: https://doi.org/10.5281/zenodo.7833244


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
