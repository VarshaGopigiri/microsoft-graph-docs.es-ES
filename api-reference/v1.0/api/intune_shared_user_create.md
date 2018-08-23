# <a name="create-user"></a>Crear usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Cree un objeto [user](../resources/intune_shared_user.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).  Según el contexto, se le requerirá un permiso específico.

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)| _varía según el contexto_ |
| &nbsp; &nbsp; Dispositivos | DeviceManagementManagedDevices.ReadWrite.All |
| &nbsp; &nbsp; MAM | DeviceManagementApps.ReadWrite.All |
| &nbsp; &nbsp; Incorporación | DeviceManagementServiceConfig.ReadWrite.All |
| &nbsp; &nbsp; Solución de problemas | DeviceManagementManagedDevices.ReadWrite.All |
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto user.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto user.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del usuario.|
|**Incorporación**|
|deviceEnrollmentLimit|Int32|El límite del número máximo de dispositivos que el usuario puede inscribir. Los valores permitidos son 5 o 1000.|

La compatibilidad con las propiedades de cuerpo de solicitud varía según el contexto.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [user](../resources/intune_shared_user.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

``` http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json
Content-length: 46

{
  "@odata.type": "#microsoft.graph.user"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Las propiedades que devuelve una llamada real varían según el contexto.

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



