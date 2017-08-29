# <a name="get-a-site-resource"></a>Obtener un recurso site

Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.

[site]: ../resources/site.md

Un recurso **site** se resuelve con un identificador único compuesto de los siguientes valores:

* Nombre de host de la colección de sitios (contoso.sharepoint.com)
* Identificador único (guid) de la colección de sitios
* Identificador único (guid) del sitio

También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz para un destino especificado de la manera siguiente:

* `/sites/root`: El sitio raíz del inquilino.
* `/groups/{group-id}/sites/root`: The group's team site.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Sites.Read.All, Sites.ReadWrite.All |

## <a name="get-the-tenants-root-site"></a>Obtener el sitio raíz del inquilino

Para obtener acceso al sitio de SharePoint de raíz dentro de un inquilino:

```http
GET /sites/root
GET /sites/contoso.sharepoint.com
```

## <a name="access-a-site-by-server-relative-url"></a>Obtener acceso a un sitio mediante la dirección URL relativa al servidor

Si tiene la dirección URL relativa al servidor de un recurso **site**, puede construir una solicitud de la manera siguiente:

```http
GET /sites/{hostname}:/{server-relative-path}
```

## <a name="access-a-group-team-site"></a>Obtener acceso a un sitio de grupo

Para obtener acceso al sitio de grupo para un [group](../resources/group.md):

```http
GET /groups/{group-id}/sites/root
```

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- { "blockType": "request", "name": "get-site", "scopes": "sites.read.all service.sharepoint" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}
```

##### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "d297964f-d325-424b-a002-f54048a4622e",
    "name": "OneDrive / SharePoint Team",
    "description": "Collaboration site for the OneDrive and SharePoint team",
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Site/Get site by ID"
} -->
