# <a name="reportroot-getskypeforbusinesspeertopeeractivityusercounts"></a>reportRoot: getSkypeForBusinessPeerToPeerActivityUserCounts

Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de punto a punto realizadas en la organización. Entre los diferentes tipos, se incluyen sesiones de mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos en sesiones de punto a punto.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de punto a punto de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713).

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

| Tipo de permiso                        | Permisos (de menos a más privilegiados) |
| :------------------------------------- | :--------------------------------------- |
| Delegado (cuenta profesional o educativa)     | Reports.Read.All                         |
| Delegado (cuenta personal de Microsoft) | No admitida.                           |
| Aplicación                            | Reports.Read.All                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a>Parámetros de la solicitud

En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.

| Parámetro | Tipo   | Descripción                              |
| :-------- | :----- | :--------------------------------------- |
| period    | cadena | Especifica la duración de tiempo durante la que se agrega el informe. Los valores admitidos para {period_value} son: D7, D30, D90 y D180. Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe. Necesario. |

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre          | Descripción                              |
| :------------ | :--------------------------------------- |
| Authorization | {token} de portador. Obligatorio.                |
| If-None-Match | Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`. Opcional. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe. La URL se encuentra en el encabezado `Location` de la respuesta.

Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.

El archivo CSV tiene los siguientes encabezados de columna.

- Fecha de actualización del informe
- Fecha del informe
- Período del informe
- Mensajería instantánea
- Audio
- Vídeo
- Uso compartido de aplicaciones
- Transferencia de archivos

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinesspeertopeeractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='D7')
```

#### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio,Video,App Sharing,File Transfer
```
