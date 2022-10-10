+++ 
draft = false
date = 2022-09-26T20:16:43+02:00
title = "HTML Y CSS"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

# HTML Y CSS

---

#### Página web con menu vertical

```HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menú</title>

    <style>

    #cuerposerrano{
        background-color: aquamarine
    }

    .vertical-menu {
        width: 200px; 
        border: 5px solid rgb(97, 97, 97);
        position: absolute;
        bottom: 545px;
    }
    .vertical-menu a {
        background-color: rgb(163, 163, 163); 
        color: rgb(0, 0, 0); 
        display: block; 
        padding: 12px; 
        text-decoration: none; 
}

    .vertical-menu a:hover {
        background-color: rgb(77, 77, 77); 
        color:white;
    }

    h1{
        position: absolute;
        left: 250px;
        top: 5px;
    }

    #cuadradogrande{
            position:relative;
            top: 70px;
            left: 220px;
            padding: 1px 1px;
            border: blue 5px solid;
            margin-top: 10px;
            margin-left: 10px;
            margin-right: 10px;
            background-color:rgb(255, 255, 255);
            width: 950px;
            height: 115px;
    }

    img{
       margin-top: -70px;
       margin-left: 1220px;
       margin-right: 10px;
    }
        </style>
</head>
<body id="cuerposerrano">
    <h1>Madrid</h1>

    <div class="vertical-menu">
        <a href="Madrid.html"target="self">Madrid</a>
        <a href="Paris.html"target="self">Paris</a>
        <a href="Roma.html"target="self">Roma</a>
      </div>

      <div id="cuadradogrande">
        <p>
        Madrid es un municipio y una ciudad de España. La localidad, con categoría histórica de villa, es la capital de
        España y de la Comunidad de Madrid. También conocida como la Villa y Corte, es la más poblada del Estado, con
        3165235 de habitantes en el año 2014, mientras que, con la inclusión de su área metropolitana8 la cifra de
        población asciende a 6543031 habitantes, siendo por ello la tercera o cuarta área metropolitana, según la fuente,
        por detrás de las de París y Londres, y en algunas fuentes detrás también de la Región del Ruhr, y la tercera
        ciudad más poblada de la Unión Europea, por detrás de Berlín y Londres.</p>
    </div>
    <img src="madrid.jpg">
</body>
</html>

```

![texto_alternativo](C:\Users\hecto\Desktop\hugoasir2\hugo-coder\assets\images\capturas.PNG){width=80 height=100}