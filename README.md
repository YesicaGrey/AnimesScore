<div style="border-radius:10px;border:#8441a0 solid:10px;padding: 10px;background-color:##f8eefb;font-size:100%;text-align:left">
<div style="font-family:Arial;background-color:'#DEB887'; padding:30px; font-size:15px">
    
<h3 align="left"><font color=purple> Introducción:</font></h3><br>
Al anime se le conoce como un estilo de animación tradicional de origen japonés, que en los últimos años ha tenido gran relevancia, especialmente en la parte occidental del mundo. Gracias a las plataformas de streaming es como una gran varidad titulos han llegado a la mayoría de la población, y a sus grandes y diferentes historias es que su demanda sigue en aumento.

<h3 align="left"><font color=purple> Contexto comercial:</font></h3><br>
<b> My anime list </b> es una pagina web conformada por una comunidad virtual, donde el tema principal son los animes y mangas. Dentro de esta pagina podrás encontrar además de una red social, bases de datos, recomendaciones, reseñas, etc. sobre los animes más conocidos, relevantes o no que se han publicado hasta el día de hoy. Dentro de la información visible en la pagina se encuentra la variable <b> Score </b>, que es el puntaje promedio que le han otorgado los distintos usuarios en my anime list a un anime en particular.  

<h3 align="left"><font color=purple> Objetivo del proyecto:</font></h3><br>
    
La importancia del **Score** en un anime recién lanzado radica en su capacidad para prever si el anime tendrá éxito o no. Por esta razón, el proposito de este proyecto fue el realizar la predicción de este valor mediante técnicas de regresión. Adicional, llevamos a cabo una discretización de la variable para determinar si el anime será clasificado como exitoso, malo o poco éxitoso. Y como información adicional, se codificó una función que ofrece recomendaciones basadas en un anime previamente dado.

    
<b>Contamos con el siguiente dataset obtenido de kaggle : </b> <a href="https://www.kaggle.com/datasets/hernan4444/anime-recommendation-database-2020">Clic para obtener el dataset </a><br> Y los subsecuentes campos

| No  | Columna     | Descripción| Ejemplo
|-----|----------|----------|----------|
| 1   | MAL_ID  | MyAnimelist ID del anime   |     1     |
| 2   | Name   | nombre completo del anime  |      Cowboy Bebop    |
| 3   | Score   | puntaje promedio del anime dado por todos los usuarios en la base de datos MyAnimelist   |  8,78        |
| 4   | Genres  | lista de géneros separados por comas para este anime | Acción, Aventura, Comedia, Drama, Ciencia ficción, Espacio      |
| 5   | English name   | nombre completo en inglés del anime   |     Cowboy Bebop     |
| 6   | Japanese name   | nombre completo en japonés del anime   |   カウボーイビバップ       |
| 7   | Type   | TV, película, OVA, etc  |     TV     |
| 8   | Episodes   | número de capítulos   |     26     |
| 9   | Aired  | fecha de emisión  |   del 3 de abril de 1998 al 24 de abril de 1999    |
| 10  | Premiered   | estreno de temporada   |    primavera de 1998      |
| 11  | Producers  | lista de productores separados por comas  |   Bandai Visual       |
| 12  | Licensors  | lista de licenciantes separados por comas  |   Funimation, Bandai Entertainment       |
| 13  | Studios  | lista de estudios separados por comas  |    Sunrise      |
| 14  | Source  | Manga, Novela ligera, Libro, etc. |    Original      |
| 15  | Duration  | duración del anime por episodio  |   24 min. por ep.       |
| 16  | Rating   | tasa de edad   |   R - 17+ (violencia y blasfemias)    |
| 17  | Ranked  | posición basada en la puntuación  |     28     |
| 18  | Popularity   | posición basada en la cantidad de usuarios que han agregado el anime a su lista  |    39   |
| 19  | Members  | número de miembros de la comunidad que están en el "grupo" de este anime   |    1251960      |
| 20  | Favorites   | número de usuarios que tienen el anime como "favoritos"   |   61.971      |
| 21  | Watching   | número de usuarios que están viendo el anime   |    105808      |
| 22  | Completed   | número de usuarios que han completado el anime  |    718161      |
| 23  | On-Hold  | número de usuarios que tienen el anime en espera   |     71513     |
| 24  | Dropped  | número de usuarios que han dejado caer el anime   |   26678       |
| 25  | Plan to Watch   | número de usuarios que planean ver el anime  |    329800      |
| 26  | Score-10   | número de usuarios que puntuaron 10   |    229170      |
| 27  | Score-9   | número de usuarios que puntuaron 9   |    182126  |
| 28  | Score-8 | número de usuarios que puntuaron 8   |     131625   |
| 29  | Score-7 | número de usuarios que puntuaron 7   |    62330     |
| 30  | Score-6 | número de usuarios que puntuaron 6   |    20688     |
| 31  | Score-5 | número de usuarios que puntuaron 5   |     8904     |
| 32  | Score-4 | número de usuarios que puntuaron 4   |     3184     |
| 33  | Score-3 | número de usuarios que puntuaron 3   |      1357    |
| 34  | Score-2 | número de usuarios que puntuaron 2   |     741      |
| 35  | Score-1 | número de usuarios que puntuaron 1   |     1580     |
    

    
    

<h3 align="left"><font color=purple> Preguntas y/o Hipotesis :</font></h3><br>
    
Las preguntas en un contexto comercial que nos podríamos hacer de utilidad serían las siguientes:
1. ¿Los animes de que género suelen ser los mejores rankeados?
2. ¿Existe una relación entre la temporada en que es publicado un anime y el que sea completado o dejado de ver?
3. ¿Cuál es el estudio con mayor número de éxitos?
4. ¿Los animes que tienen como antecesor un manga son más exitosos que otros?
5. Los animes con más tiempo de transmisión suelen ser los más famosos o éxitosos
    </div>
    </div>


<h3 align="left"><font color=purple>  Contenido: </font></h3><br>
<div style="border-radius:10px;border:##8441a0 solid;padding: 10px;background-color:#f8eefb;font-size:110%;text-align:left">
<div style="font-family:Arial;background-color:'#DEB887'; padding:3px; font-size:15px">
    
1. <b>Importación de librerías </b>
2. <b> Data Wrangling</b>   
3. <b> EDA </b>    
4. <b> Feature Engineer </b>
- Análisis Bivarido y Multivariado
- Hot Enconding
- Estadarización de datos
5. <b> Reducción de dimensionalidad </b>   
- PCA
- Mapeo de caracteristicas isométricas - Isomap
    
6. <b>  Regresión </b>

- Modelado y Evaluación
- Cross Validation
- Grid Search
- Halving Grid Search
- Conclusiones

7. <b> Clasificación </b>

- Discretización
- SMOTE
- Curva ROC y AUC
- LazyClassifier
- Halving Grid Search
- Conclusiones
    
8. <b> Recomendación </b>

- KNN
- Conclusiones

    
</div>
