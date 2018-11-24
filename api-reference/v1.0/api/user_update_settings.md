# <a name="update-settings"></a>Configuración de actualización

Actualizar las propiedades del objeto [settings](../resources/user_settings.md) . Los usuarios en la misma organización pueden tener diferentes configuraciones basadas en sus preferencias o en las directivas de la organización. Para obtener al usuario actual configuración, vea [Configuración del usuario actual](user_get_settings.md). 

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.ReadWrite, User.ReadWrite.All   |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | User.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

```http
PATCH https://graph.microsoft.com/v1.0/me/settings
```

Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All. Para obtener más información, vea [permisos](../../../concepts/permissions_reference.md). 

```http
PATCH https://graph.microsoft.com/v1.0/users/{id | userPrincipalName}/settings/
```

## <a name="request-headers"></a>Encabezados de solicitud

| Encabezado       | Valor|
|:-----------|:------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contributionToContentDiscoveryDisabled|Booleano|En el valor true deshabilita el acceso de delegado a la API de [tendencias](../../beta/resources/insights_trending.md) y deshabilitar el acceso a los documentos de Office profundizar para el usuario. Configuración en true también afecta a la relevancia del contenido que se muestra en Office 365: por ejemplo, los sitios que se sugiere en la página principal de SharePoint y la vista de detección en OneDrive para la empresa muestran resultados menos relevantes. Esta configuración refleja el estado de control en [Office profundizar](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).|

## <a name="example"></a>Ejemplo 

##### <a name="request"></a>Solicitud

Este es un ejemplo de solicitud en cómo voluntaria de un usuario desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización.

```http
PATCH https://graph.microsoft.com/v1.0/me/settings
Content-type: application/json
Content-length: 37

{
  "contributionToContentDiscoveryDisabled": true
}
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": true
}
```

#### <a name="batch-request"></a>Solicitud de lote

También es posible voluntaria de varios usuarios desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización a través de una solicitud por lotes.
Para obtener más información, vea [el procesamiento por lotes de JSON](https://developer.microsoft.com/graph/docs/concepts/json_batching).

**Importante**: sólo los miembros del grupo de roles de [Administración de la organización](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) pueden actualizar varios usuarios. 



