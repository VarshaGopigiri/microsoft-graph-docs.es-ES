# <a name="update-device"></a>Actualizar device

Actualiza las propiedades de un dispositivo registrado.

Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.ReadWrite.All, Directory.AccessAsUser.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación | No se admite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | cadena  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. |
|operatingSystem|Cadena|Tipo de sistema operativo del dispositivo.|
|operatingSystemVersion|Cadena|Versión del sistema operativo del dispositivo.|
|displayName|Cadena|Nombre para mostrar del dispositivo.|
|isCompliant|Booleano|**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**. Esto solo lo puede actualizar Intune para cualquier tipo de sistema operativo del dispositivo o por una [aplicación MDM aprobada](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows. |
|isManaged|Booleano|**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**. Esto solo lo puede actualizar Intune para cualquier tipo de sistema operativo del dispositivo o por una [aplicación MDM aprobada](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "update_device"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/devices/{id}
Content-type: application/json
Content-length: 31

{
  "accountEnabled": false
}
```
##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
