# <a name="use-the-activity-feed-rest-api"></a>Usar la API de REST de fuente de actividades

Puede usar la API de fuente de actividades en Microsoft Graph para reanudar la actividad de un usuario en varios dispositivos y plataformas. Las solicitudes de API de fuentes de actividades se realizan en nombre de un usuario a través de [permisos delegados](../../../concepts/permissions_reference.md#delegated-permissions-application-permissions-and-effective-permissions) y el [permiso de actividad de usuario](../../../concepts/permissions_reference.md), que se puede usar con cuentas personales o de trabajo y escolares. 

Las actividades del usuario son representadas por el recurso [activity](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/projectrome_activity) y se organizan en una fuente basada en la hora representada por la colección me/activities. 
<!-- Add missing content.
Each activity represents a unique... 
-->
## <a name="what-makes-a-great-user-activity"></a>¿Qué hace que sea buena una actividad de usuario?

Las actividades de usuario no solo inician aplicaciones: son vínculos profundos en contenido específico dentro de la aplicación. Las actividades de usuario que crea no solo se pueden utilizar en su propia aplicación, sino que también aparecerán en Cortana y Windows Timeline, lo que aumenta el número de reincorporaciones a la aplicación y facilita a los usuarios el uso de la misma en varios dispositivos.  

### <a name="what-should-become-an-activity"></a>¿Qué debería ser una actividad? 

Debido a que cada aplicación es diferente, cada desarrollador de aplicaciones debe entender la mejor manera de asignar acciones dentro de su aplicación a las actividades de usuario. Por ejemplo, los juegos pueden crear una actividad para cada campaña, las aplicaciones de creación de documentos pueden crear una actividad para cada documento único y las aplicaciones de línea de negocio pueden crear una actividad para cada flujo de trabajo. 

Aplique las siguientes directrices al definir actividades en su aplicación:

**QUÉ HACER:** Registre una sola actividad para un grupo de acciones de usuario relacionadas. Si su aplicación se utiliza para una secuencia de contenido relacionado, probablemente tenga sentido grabar una sola actividad durante toda la sesión de compromiso.  

*Escenarios de lista de reproducción:* Esto es especialmente importante para las listas de reproducción de música o programas de TV; una sola actividad de usuario se puede actualizar para mostrar el progreso. En este caso, tendrá una sola actividad de usuario con varios [elementos del historial](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/projectrome_historyitem) que representan los períodos de compromiso a través de varios días o semanas.  

**QUÉ HACER:** Almacenar datos de usuario en la nube. Si desea admitir actividades entre dispositivos, debe asegurarse de que el contenido necesario para volver a activar esta actividad se almacena en una ubicación en la nube. Por ejemplo, si publica una actividad cada vez que un usuario edita un documento, el documento debe almacenarse en la nube en lugar de localmente en el dispositivo del usuario para permitir la reutilización entre dispositivos.  

**QUÉ NO HACER:** Crear una actividad de usuario para las acciones que los usuarios no necesitan reanudar en el futuro. Si su aplicación se utiliza para completar operaciones simples y únicas que no persisten para que usted pueda hacer su seguimiento en el futuro, probablemente no necesite escribir una actividad de usuario. 

Para ser más precisos, incluso si las actividades del usuario se muestran en la Escala de tiempo de Windows, esto no está diseñado como una herramienta de control de versiones: elegir una actividad basada en documentos siempre debería mostrar la versión más reciente de ese documento (incluidos los cambios realizados por otro usuario).

**QUÉ NO HACER:** Crear una actividad de usuario para acciones completadas por *otros usuarios*. Si alguien le envía al usuario un mensaje o @menciona el usuario dentro de la aplicación, no debe escribir una actividad nueva. Estas interacciones se satisfacen mejor mostrando notificaciones.  

*Escenarios de colaboración:* Si varias personas trabajan en la misma actividad (por ejemplo, un documento de Word), habrá casos donde otro usuario ha realizado cambios en el documento después de que se modificara por última vez. En este caso, los desarrolladores de aplicaciones es posible que deseen actualizar los elementos visuales en la actividad para reflejar los cambios realizados en el documento. Para ello, la aplicación podría actualizar la actividad existente sin crear un nuevo elemento de historial. 

>**Nota:** Si está publicando actividades para una aplicación web, es importante incluir un `activationURL` y un `fallbackURL` para cada uno de sus actividades. Las actividades lanzarán al usuario de nuevo en su aplicación tal y como se espera de las experiencias de Microsoft como la Escala de tiempo de Windows. 

## <a name="app-interaction-patterns-and-user-activities"></a>Modelos de interacción de la aplicación y las actividades de usuario 
Las actividades de usuario que cree variará en función del modelo de interacción de la aplicación. Aunque cada aplicación es diferente, la mayoría se inscriben en uno de los siguientes modelos de interacción: 

* **Aplicaciones basadas en documento**: cree una actividad por cada documento con uno o más registros de historial que reflejen períodos de uso. Es importante actualizar su tarjeta de actividad a medida que se realizan cambios en el documento. 
* **Aplicaciones de reproducción de medios**: cree una actividad por agrupación lógica de contenido, como una lista de reproducción, programas o contenido independiente. 
* **Juegos**: cree una actividad para mundo o juego guardado. Si su juego es compatible con solo una única secuencia de niveles, puede escribir la misma actividad a través del tiempo, aunque es posible que desee actualizar su tarjeta para mostrar su progreso o los logros más recientes. 
* **Aplicaciones de utilidad**: si no hay nada dentro de la aplicación que los usuarios deseen reanudar, no debe publicar actividades. Un buen ejemplo es una aplicación simple de un único propósito como la calculadora. 
* **Aplicaciones de línea de negocio**: existen muchas aplicaciones para la administración de tareas sencillas o flujos de trabajo. Cree una actividad para cada flujo de trabajo independiente accedido a través de la aplicación. Por ejemplo, cada informe de gastos será una actividad independiente, porque es posible que desee haga clic en esa actividad para ver si se ha aprobado.

*Algunas aplicaciones complejas incluyen varios modelos de interacción. Es posible que desee seguir diferentes modelos de creación de actividades de usuario para diferentes escenarios manejados por su aplicación.*

<!-- Add content or remove H2.
## Common use cases 
-->

## <a name="next-steps"></a>Pasos siguientes

- Consulte el [recurso activity](https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/projectrome_activity) y defina las actividades de su aplicación para ayudar a los usuarios a reanudar tareas importantes.
- Explore los [ejemplos de tarjetas adaptables](http://adaptivecards.io/samples/) para obtener ideas que hagan que sus actividades **destaquen**.  
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/en-us/graph/graph-explorer).

**¿Necesita más ideas?** 
- Vea [cómo las experiencias de Microsoft usan las actividades](https://channel9.msdn.com/events/Build/2017/B8108).
- Obtenga información sobre [la API de fuente de actividades y siga donde se quedó](https://channel9.msdn.com/Events/Windows/Windows-Developer-Day-Fall-Creators-Update/WinDev011).
