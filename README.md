# Prueba Tecnica
Proyecto gradle el cual contiene tres escenarios de prueba automatizados en java bajo el framework de Serenity BDD con cucumber utilizando patron de diseño ScreenPlay.

Para la obtencion de los datos se utilizaron archivos JSON.


# Pre-requisitos 📋
Tener instalado :
- Gradle version 7.3.3
- Java version 11

# Ejecutar caso de prueba ⚙️
- El proyecto se encuentra configurado para ejecutarse en un sistema operativo Mac, con el navegador chrome (version 99.0.4844.74 )
  En caso de requerir ejecutar el proyecto bajo otro sistema operativo, debe agregar los respectivos WebDriver en la carpeta correspondiente que se encuentra dentro de **"src/test/resources/webdriver"**
- Para ejecutar los tres flujos basta con abrir una terminal de comandos, ubicarse en la carpeta donde haya alojado el proyecto y posterior a ello ejecutar el comando :

       gradle clean test

- Si desea ejecutar los flujos de manera independiente lo puede realizar tambien con los siguientes comandos

    - **Primer escenario** y **segundo escenario** :  `gradle clean test --tests WebTablesRunner`
    - **Tercer escenario**: `gradle clean test --tests WidgetsDatePickerRunner`
  
  
- En caso que desee correr unicamente un escenario lo puede realizar especificando el tag a ejecutar con el siguiente comando:
    
        gradle clean test -Dcucumber.filter.tags="@Prueba1"


# Visualizar reportes
Para acceder a los reportes puede realizarlo dirigiendose al apartado de SERENITY REPORTS el cual podra visualizar en consola al terminar la ejecucion. Serenity proporciona dos tipos de reporte, uno completo y uno resumido

- **Reporte**: target/site/serenity/index.html