# <a name="working-with-sharepoint-sites-in-microsoft-graph"></a>Trabajar con sitios de SharePoint en Microsoft Graph

La API de SharePoint en Microsoft Graph admite los siguientes escenarios principales:

* Acceso a los **sitios** de SharePoint, y a las **unidades** (bibliotecas de documentos)
* Soporte de solo lectura de los recursos del **sitio** (sin capacidad para crear nuevos sitios)
* Compatibilidad de lectura y escritura para **driveItems**
* Recursos de dirección por la ruta de acceso relativa, URL o id. de SharePoint

## <a name="sharepoint-api-root-resources"></a>Recursos raíz de las API de SharePoint

Los ejemplos siguientes son relativos al `https://graph.microsoft.com/v1.0`.

| Ruta de acceso                                   | Descripción
|:---------------------------------------|:------------------------------------
| /sites/root                            | [Sitio][] predeterminado de la organización.
| /sites/{site-id}                       | Acceso a un [sitio][] específico por su id.
| /sites/{site-id}/drive                 | Acceso a la [unidad](drive.md) predeterminada (biblioteca de documentos) para este [sitio][].
| /sites/{site-id}/drives                | Enumerar las [unidades](drive.md) (bibliotecas de documentos) en el [sitio][].
| /sites/{site-id}/sites                 | Enumerar los sitios secundarios en [sitio][].
| /groups/{group-id}/sites/root          | Acceso a un [sitio][] de equipo de grupo.

Los sitios también pueden dirigirse a través de la ruta al utilizar el nombre de host de SharePoint, seguido de dos puntos y la ruta de acceso relativa al sitio. Opcionalmente, puede hacer la transición de vuelta mientras dirige el modelo de recursos al colocar otro signo de dos puntos al final.

| Ruta de acceso                                           | Descripción
|:-----------------------------------------------|:-----------------------------------
| /sites/contoso.sharepoint.com:/teams/hr        | El sitio asociado con https://contoso.sharepoint.com/teams/hr
| /sites/contoso.sharepoint.com:/teams/hr:/drive | Acceso a la [unidad](drive.md) predeterminada para este sitio.

## <a name="note-for-existing-sharepoint-developers"></a>Nota para los desarrolladores de SharePoint existentes

La API de SharePoint de Microsoft Graph tiene algunas diferencias clave con las API de CSOM. El recurso del [sitio][] se asigna a `SPWeb`. El [sitio][] raíz (`SPWeb`) en un sitio de la colección tiene una faceta de [colecciónDeSitios](sitecollection.md), que contiene información acerca de `SPSite`. Debido a que los identificadores para los sitios solo son únicos dentro de su colección de sitios, el direccionamiento a un sitio a través del id. requiere proporcionar el identificador de la colección de sitios y el identificador del sitio.

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname},{spsite-id},{spweb-id}/
```
Una dirección URL creada solo con el nombre de host apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname}
```

Una dirección URL creada solo con el nombre de host y el id. de siteCollection (`SPSite`) apuntará al sitio raíz (`SPWeb`) en la colección de sitios predeterminada.

```http
GET https://graph.microsoft.com/v1.0/sites/{hostname},{spsite-id}
```

[sitio]: site.md
[drive]: drive.md
[siteCollection]: siteCollection.md

<!-- {
  "type": "#page.annotation",
  "description": "Getting started programming with the SharePoint API",
  "keywords": "getting started sharepoint rest api programming C# ios android rest http",
  "section": "documentation",
  "tocPath": "Getting Started",
  "tocIndex": -100
} -->
