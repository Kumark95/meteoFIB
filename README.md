# MeteoFIB

Proyecto orientado a la recolección de datos de una estación meteorológica, para poder ofrecer al usuario la posibilidad de visualizarlos mediante una aplicación web.

# Apartados y funcionalidades
- **Home**

Es la pantalla de inicio de la web. En ella se puede apreciar el nombre de nuestro proyecto, MeteoFIB, junto con una pequeña descripción del mismo. Aquí también podemos encontrar un mapa que muestra la ubicación de nuestra estación, que será de donde obtenemos los diferentes datos meteorológicos de temperatura, humedad y presión atmosférica.

![Alt text](/static/img/home.png?raw=true "Apartado Home")

- **Medición**

En este apartado se muestra una lista con diferentes horas. Estas corresponden a las horas en las que la estación ha recogido datos con los sensores. Podemos observar que, inicialmente el último elemento de la lista, que corresponde con la hora actual, contiene además los datos meteorológicos de la estación para aquella hora, que vemos en una pequeña tabla.

Si deseamos ver por ejemplo, cuál era la temperatura o humedad a una determinada hora, solo hace falta hacer click en el elemento de la lista que contiene dicha hora. Al hacerlo, aparecerán estos datos en la pantalla y desaparecerán de la misma los que hasta el momento habían estado presentes.

Por último, podemos observar que en la parte inferior se encuentra otra sección, en ella se muestran los datos que la estación ha ido obteniendo de la última semana, mostrando así los valores medios de temperatura, humedad relativa y presión atmosférica de todos estos días.

![Alt text](/static/img/medicion.png?raw=true "Apartado Medicion")


- **Estadísticas**

Aquí lo que se intenta es comparar la información que obtenemos con nuestros sensores con las que obtienen otros servicios, en este caso la Agencia Estatal de Meteorología (AEMET). 

Para realizar esta comparación se utilizan dos gráficas, una para la temperatura y otra para la humedad relativa. Esto se debe a que AEMET no proporciona información de la presión atmosférica.

Estas gráficas, al igual que la lista en el apartado anterior, Medición, se crean dinámicamente mostrando solo la información relevante hasta la hora actual en la que nos encontremos.

![Alt text](/static/img/estadisticas.png?raw=true "Apartado Estadísticas")


- **Suscripción**

Este apartado permite al usuario suscribirse a nuestro servicio. Con esto lo que conseguiría es recibir semanalmente la información de nuestra estación. Y si así lo desea complementar estos datos con la previsión para los siguientes días proporcionada por AEMET dado que nuestro servicio no es capaz de hacer predicciones meteorológicas.

Esta información se enviaría cada Miércoles a la dirección de correo electrónico que el usuario ingrese. Antes de poder enviar esta petición de suscripción a nuestro servicio, esta dirección de correo será validada para comprobar que tiene un formato adecuado.

Una vez los datos sean correctos se enviarán a base de datos no relacional, que almacenará todas estas direcciones y de la que hablaremos más adelante.

![Alt text](/static/img/sub1.png?raw=true "Apartado Suscripción")


Al enviarse, el formulario desaparece y se muestra al usuario un mensaje de agradecimiento.

![Alt text](/static/img/sub2.png?raw=true "Apartado Mensaje de suscripción finalizada")

A partir de ese momento, el usuario queda suscrito a nuestra aplicación y semanalmente recibirá información sobre nuestra estación, concretamente los Miércoles a las 8h.

Además, si el usuario decidió recibir también la predicción de AEMET, al recibir el informe semanal, también figurará esta información.

El mensaje que el usuario recibiría cada semana sería el siguiente:

![Alt text](/static/img/sub3.png?raw=true "Informe semanal de MeteoFIB")


![Alt text](/static/img/sub4.png?raw=true "Información de suscripción")


![Alt text](/static/img/sub5.png?raw=true "Mensaje de cancelación de suscripción")


- **Contacto**

Para aquellos usuarios que sientan la necesidad de ponerse en contacto con nosotros existe este apartado. De esta forma, una vez rellenados los diferentes apartados, se procede a la validación como en el caso anterior, comprobando que los campos no esten vacios y en el caso del correo electrónico de contacto, sea válido.

![Alt text](/static/img/contacto.png?raw=true "Apartado Contacto")


Una vez enviados estos datos, vemos que el formulario desaparece y en su lugar se presenta un mensaje avisando al usuario que su mensaje se ha enviado e informando que responderemos con la mayor brevedad posible. 

![Alt text](/static/img/contacto2-cut.png?raw=true "Mensaje de envío correcto")



Para recibir todos estos mensajes hemos creado un correo electrónico especial desde el que podremos recibir estos mensajes y contestarlos. A continuación podemos ver cómo llegaría el mensaje:

![Alt text](/static/img/contacto3.png?raw=true "Mensaje recibido")


- **Sobre nosotros**

Finalmente, este apartado muestra información sobre la composición de nuestro grupo.

![Alt text](/static/img/nosotros.png?raw=true "Apartado Sobre Nosotros")

