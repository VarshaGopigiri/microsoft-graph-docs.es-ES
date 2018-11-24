# <a name="remove-an-app-from-your-organizations-app-catalog"></a>Quitar una aplicación de catálogo de aplicaciones de la organización



Quitar la [aplicación](../resources/teamsapp.md) de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino). Para quitar la aplicación de catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .

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
DELETE /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado        | Valor           |
|:--------------|:--------------  |
| Authorization | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud

Ninguna.

>**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp_list.md) para hacer referencia a la aplicación que desea actualizar. No use el identificador del manifiesto del paquete de la aplicación de zip.

## <a name="response"></a>Respuesta

```
HTTP/1.1 204 No Content
```

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

```http
DELETE https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
```

### <a name="response"></a>Respuesta

```http
HTTP/1.1 204 No Content
```
