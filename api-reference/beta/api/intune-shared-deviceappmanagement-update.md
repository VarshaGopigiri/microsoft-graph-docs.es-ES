---
title: Actualizar deviceAppManagement
description: Actualice las propiedades de un objeto deviceAppManagement.
author: tfitzmac
ms.openlocfilehash: d5a4b3cfa1af7eb4a465c951a4a10f4c19944d8a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324027"
---
# <a name="update-deviceappmanagement"></a>Actualizar deviceAppManagement

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).
## <a name="prerequisites"></a>Requisitos previos
Uno de los siguientes permisos se requiere para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).  Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
| Delegado (cuenta profesional o educativa) | |
| &nbsp;&nbsp; **Aplicaciones**, **libros**o **incorporación de redes** | DeviceManagementApps.ReadWrite.All |
| &nbsp; &nbsp; **Administración de dispositivos** | DeviceManagementManagedDevices.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) | No admitida. |
| Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|**Incorporación**|
|isEnabledForMicrosoftStoreForBusiness|Boolean|Indica si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.|
|microsoftStoreForBusinessLanguage|String|Información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas. Referencias culturales que son específicas de un país o región. Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores). El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166. Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.|
|microsoftStoreForBusinessLastCompletedApplicationSyncTime|DateTimeOffset|La última vez que se completó una sincronización de aplicaciones desde Microsoft Store para Empresas.|
|microsoftStoreForBusinessLastSuccessfulSyncDateTime|DateTimeOffset|Última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.|
|microsoftStoreForBusinessPortalSelection|[microsoftStoreForBusinessPortalSelectionOptions](../resources/intune-onboarding-microsoftstoreforbusinessportalselectionoptions.md)|La información del portal de usuario final se usa para sincronizar las aplicaciones de Portal de empresa Intune de Microsoft Store para la empresa. Hay tres opciones para elegir entre \['Sólo el portal de la empresa', 'Almacenar compañía del portal y privada', 'Sólo almacén privado'\]. Los valores posibles son: `none`, `companyPortal` y `privateStore`.|

Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 110

{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
}
```



