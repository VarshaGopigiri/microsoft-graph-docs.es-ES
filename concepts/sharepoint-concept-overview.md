# <a name="sharepoint-sites-and-content-api-overview"></a>Información general sobre la API de contenido y sitios de SharePoint

SharePoint es su intranet móvil inteligente. Con SharePoint, los usuarios pueden compartir y administrar contenido, conocimientos y aplicaciones para mejorar el trabajo en equipo, buscar información y colaborar en la organización. Puede usar la API de REST de SharePoint en Microsoft Graph para integrar sus soluciones con contenidos y sitios de SharePoint.

## <a name="why-integrate-with-sharepoint-sites-and-content"></a>¿Por qué integrar con contenidos y sitios de SharePoint?

Los sitios de SharePoint mejoran la colaboración en grupo y la comunicación. Grupos de Office 365, Microsoft Teams y los portales se basan en SharePoint, por lo que puede usar Microsoft Graph para obtener acceso a datos, sin importar dónde se encuentren. Use la API de SharePoint en Microsoft Graph para obtener acceso a:

- Sitios de grupo que almacenen contenido donde colaboran los usuarios con sus compañeros.
- Portales y sitios de comunicación donde los usuarios publiquen páginas de contenido enriquecido que compartan con toda la organización.

### <a name="unleash-your-data-with-sharepoint-lists"></a>Mejorar los datos con listas de SharePoint

Las [listas][lista] son la base del almacenamiento de datos en SharePoint.
[Cree listas][crear] para almacenar una amplia variedad de datos empresariales, desde una sencilla lista de contactos de clientes a una aplicación empresarial personalizada con PowerApps como front-end.
Al usar [columnas][] para definir el esquema, SharePoint puede proteger la integridad de los datos, así como habilitar funciones enriquecidas de indexación, consultas y búsqueda.

### <a name="bring-the-power-of-lists-to-your-teams-files"></a>Llevar las funciones avanzadas de las listas a los archivos de su equipo

SharePoint almacena archivos en un [tipo de lista][] especial denominado biblioteca de documentos.
Puede usar la [API de OneDrive para la Empresa][] y una biblioteca como una [unidad][], o bien puede usar la API de SharePoint para trabajar con una biblioteca como una [lista][].
Al igual que con una lista normal, puede ampliar el esquema de una biblioteca de documentos para adaptarlo a sus necesidades empresariales con columnas personalizadas.

### <a name="light-up-your-app-with-your-users-sharepoint-intranet-data"></a>Mejorar la aplicación con los datos de intranet de SharePoint de los usuarios

Con Microsoft Graph, puede mostrar los datos más importantes de los usuarios en la aplicación.
Para mantener actualizados los datos, realice [consultas][] en la lista donde se almacenen los datos de los usuarios.
[Cree][] sus propias listas para la aplicación y permita a los usuarios obtener acceso a los datos en otras experiencias de SharePoint, o bien mantenga todo oculto.

### <a name="use-microsoft-graph-to-extend-sharepoint"></a>Usar Microsoft Graph para ampliar SharePoint

Como plataforma, SharePoint ofrece distintos modelos para la extensión e integración:

- [SharePoint Framework][] ofrece una forma de crear elementos web con tecnologías del lado cliente y herramientas de código abierto que se pueden hospedar en páginas de SharePoint.
- Los [complementos de SharePoint][] son extensiones independientes que se pueden agregar a un sitio de SharePoint sin que sea necesario ejecutar código personalizado en el servidor.

Cuando las aplicaciones se ejecutan en la página de SharePoint, puede usar fácilmente Microsoft Graph para obtener acceso a datos en Office 365.

Para obtener más información sobre estos modelos, visite el [Centro de desarrollo de SharePoint][] o la [Documentación para desarrolladores de SharePoint][].

## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre cómo [trabajar con sitios][SharePoint] para empezar a usar SharePoint en Microsoft Graph.

[lista]: ../api-reference/v1.0/resources/list.md
[columnas]: ../api-reference/v1.0/resources/columndefinition.md
[tipo de lista]: ../api-reference/v1.0/resources/listinfo.md
[crear]: ../api-reference/v1.0/api/list_create.md
[consultas]: ../api-reference/v1.0/api/listitem_get.md
[unidad]: ../api-reference/v1.0/resources/drive.md

  [API de OneDrive]: https://developer.microsoft.com/en-us/graph/docs/api-reference/v1.0/resources/onedrive
[SharePoint Framework]: https://docs.microsoft.com/sharepoint/dev/spfx/sharepoint-framework-overview
[Complementos de SharePoint]: https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins
[Centro de desarrollo de SharePoint]: https://developer.microsoft.com/sharepoint
[Documentación para desarrolladores de SharePoint]: http://aka.ms/spdev-docs
[SharePoint]: https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/sharepoint
