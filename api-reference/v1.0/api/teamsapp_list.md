# <a name="list-the-published-apps-from-the-microsoft-teams-app-catalog"></a>Lista de las aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams



Lista de [aplicaciones](../resources/teamsapp.md) desde el catálogo de aplicaciones de Microsoft Teams. Esto incluye aplicaciones de la tienda de Microsoft Teams, así como aplicaciones de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino). Para obtener aplicaciones desde el catálogo de aplicaciones de la organización sólo, especifique `Organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).

>**Nota:** Sólo los administradores globales pueden llamar a esta API. 

| Tipo de permiso                        | Permisos (de menos a más privilegiados)|
|:----------------------------------     |:-------------|
| Delegado (cuenta profesional o educativa)     | AppCatalog.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) | No admitido|
| Aplicación                            | No se admite|

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /appCatalogs/teamsApps
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado        | Valor           |
|:--------------|:--------------  |
| Authorization | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
Ninguna.

>**Nota:** Puede filtrar en cualquiera de los campos del objeto [teamsCatalogApp](../resources/teamsapp.md) para reducir la lista de resultados. Puede usar cualquiera de las siguientes operaciones de filtro: igual, no igual y, o bien y no.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [teamsCatalogApp](../resources/teamsapp.md) en el cuerpo de la respuesta.

## <a name="examples"></a>Ejemplos
### <a name="example-1"></a>Ejemplo 1
En el ejemplo siguiente se enumeran todas las aplicaciones que son específicas de su inquilino.

#### <a name="request"></a>Solicitud
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=distributionMethod eq 'organization'
```

#### <a name="response"></a>Respuesta
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "b1c5353a-7aca-41b3-830f-27d5218fe0e5",
      "externalId": "f31b1263-ba99-435a-a679-911d24850d7c",
      "name": "Test App",
      "version": "1.0.1",
      "distributionMethod":"Organization"
    }
  ]
}
```

### <a name="example-2"></a>Ejemplo 2

En el ejemplo siguiente se enumeran las aplicaciones con un identificador determinado.

#### <a name="request"></a>Solicitud
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=id%20eq%20'b1c5353a-7aca-41b3-830f-27d5218fe0e5'
```

#### <a name="response"></a>Respuesta
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "b1c5353a-7aca-41b3-830f-27d5218fe0e5",
      "externalId": "f31b1263-ba99-435a-a679-911d24850d7c",
      "name": "Test App",
      "version": "1.0.1",
      "distributionMethod":"Organization"
    }
  ]
}
```

