# <a name="outlook-personal-contacts-api-overview"></a>Información general sobre la API de contactos personales de Outlook

Los contactos de Outlook le permiten almacenar datos de contactos personales y forma parte del centro de mensajes de Outlook en Office 365. En Outlook, puede administrar correos electrónicos, programar reuniones, buscar información sobre los usuarios de una organización, iniciar conversaciones en línea, compartir archivos y colaborar en grupos.

## <a name="why-integrate-with-outlook-personal-contacts"></a>¿Por qué integrar con contactos personales de Outlook?

### <a name="complement-messaging-and-calendaring-scenarios-for-hundreds-of-millions-of-customers"></a>Complementar los escenarios de mensajes y calendarios para cientos de millones de clientes

Cientos de millones de consumidores y decenas de millones de clientes de organizaciones eligen Outlook como su cliente de correo electrónico. Los contactos ofrecen una función complementaria para mensajes y calendarios, ya que permiten a los clientes mantener un almacén integrado y fácil de usar de datos de contactos dentro de Outlook. Para los desarrolladores, usar las funciones enriquecidas de [correo](outlook-mail-concept-overview.md) o [calendario](outlook-calendar-concept-overview.md) equivale a facilitar escenarios avanzados con los datos de contactos de los usuarios.


### <a name="automate-contact-organization"></a>Automatizar la organización de contactos

La API de contactos le permite mantener organizados sus clientes, de forma muy similar a cómo lo hacen los usuarios de Outlook:

- De forma similar a la experiencia del usuario, puede crear instancias de [contactos](../api-reference/v1.0/resources/contact.md) y asignarlas a objetos de [contactFolder](../api-reference/v1.0/resources/contactfolder.md).
- La API de contactos le permite asignar categorías, contactos, eventos, mensajes, tareas y publicaciones de grupo de forma coherente para mejorar la organización y la detección. Además, puede [definir una lista general de categorías de un usuario](../api-reference/v1.0/api/outlookuser_post_mastercategories.md), lo que facilita otros escenarios creativos.
- Puede establecer una marca en un [contacto](../api-reference/v1.0/resources/contact.md) para su seguimiento. (La función de marcar está actualmente [en versión preliminar](versioning_and_support.md#beta-version) en Microsoft Graph).


### <a name="share-contact-information"></a>Compartir información de contacto

La API de contactos le permite obtener elementos de contactos del usuario que inició la sesión, o bien de los usuarios que compartieron sus contactos con el usuario que inició la sesión o los delegaron a este. Por ejemplo, si Sergio compartió una carpeta de contactos con Íker (o si Sergio delegó el acceso a Íker), los [permisos delegados](permissions_reference.md#delegated-permissions-application-permissions-and-effective-permissions) de Íker también le proporcionarían acceso de lectura en los contenidos y el calendario compartido de Sergio.


### <a name="leverage-people-api-in-microsoft-graph-to-make-better-use-of-all-people-data"></a>Usar la API de contactos en Microsoft Graph para mejorar el uso de los datos de todos los contactos

Puede usar operaciones CRUD típicas en un [contacto](../api-reference/v1.0/resources/contact.md) de Outlook para crear y administrar contactos. Como parte de Microsoft Graph, también puede usar la [API de contactos](people_example.md) para examinar los contactos de Outlook de un usuario, así como las redes sociales, el directorio de la organización y los contactos de comunicaciones recientes, y devolver información sobre contactos de todos estos orígenes que sea más relevante para el usuario. Aproveche esta inteligencia adicional en escenarios del Selector de personas.


### <a name="take-advantage-of-other-shared-features-and-conveniences-in-microsoft-graph"></a>Aprovechar otras funciones y características compartidas en Microsoft Graph

- La entidad **contact** admite una foto del contacto que se implementa como la misma entidad [profilePhoto](../api-reference/v1.0/resources/profilephoto.md) como una foto de usuario almacenada en Exchange Online o Azure Active Directory. Esto elimina la sobrecarga de convertir entre fotos de perfil de usuario y de contacto.
- Para mantener sincronizado el almacén local de la aplicación, suscríbase a [notificaciones de cambios](../api-reference/v1.0/resources/webhooks.md) y al [seguimiento de cambios](delta_query_overview.md) en contactos y carpetas de contactos.
- Puede ampliar el almacenamiento de la aplicación en una instancia de contacto como una [extensión abierta](extensibility_overview.md#open-extensions), o bien puede agregar datos personalizados fuertemente tipados al esquema de contactos como una [extensión de esquema](extensibility_overview.md#schema-extensions).


## <a name="next-steps"></a>Pasos siguientes

- Seleccione y pruebe consultas de ejemplo de contactos en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fcontacts&version=v1.0). Seleccione la opción **Mostrar más ejemplos** en la columna de la izquierda. Use el menú para activar los **Contactos personales**.
- Obtenga información sobre cómo [obtener los contactos compartidos](outlook-get-shared-contacts-folders.md)
- Consulte la referencia de la [API de contactos](../api-reference/v1.0/resources/contact.md) de Outlook.
