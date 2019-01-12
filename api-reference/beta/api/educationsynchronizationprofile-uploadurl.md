---
title: 'educationSynchronizationProfile: uploadUrl'
description: Recuperar una firma acceso compartido (SAS) para cargar archivos de origen para el almacenamiento de Azure blob para un perfil de sincronización de datos de school específicos en el inquilino. El token de SAS tiene una validez de una hora.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: e0119a583ea1cdc753b44a984af84a42173a4295
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969915"
---
# <a name="educationsynchronizationprofile-uploadurl"></a>educationSynchronizationProfile: uploadUrl

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recuperar una firma acceso compartido (SAS) para cargar archivos de origen al almacenamiento de blobs Azure para school específico datos en un [perfil de sincronización](../resources/educationsynchronizationprofile.md) del inquilino. El token de SAS tiene una validez de una hora.

La carga se proporciona la dirección URL sólo para el [proveedor de datos CSV](../resources/educationcsvdataprovider.md).

> **Nota:** Para tener acceso el almacenamiento de blobs con el token de SAS, use el [almacenamiento de Azure SDK](https://github.com/search?q=org%3AAzure+azure-storage) o [AzCopy](https://docs.microsoft.com/en-us/azure/storage/storage-use-azcopy).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso | Permisos |
|:-----------|:----------|
| Delegado (cuenta profesional o educativa) | EduAdministration.ReadWrite |
|Delegado (cuenta Microsoft personal|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /synchronizationProfiles/{id}/uploadUrl
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una dirección URL de SAS para el [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md) en el cuerpo de la respuesta.

Si aún se está procesando una solicitud anterior, este método devuelve una `409 Conflict` que indica que la carga está bloqueada actualmente para la [educationSynchronizationProfile](../resources/educationsynchronizationprofile.md).

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_educationSynchronizationProfile_uploadurl"
}-->
```http
GET https://graph.microsoft.com/beta/education/synchronizationProfiles/{id}/uploadUrl
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "@odata.type": "String",
} -->
```http
HTTP/1.1 201 OK
Content-type: application/json
Content-length: 314

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#String",
    "value": "https://sdsstorage.blob.core.windows.net/86904b1e-c7d0-4ead-b13a-98f11fc400ee?sv=2015-07-08&sr=c&si=SharedAccessPolicy_20170704044441&sig=CH65vxxqXETCkQNH0Lfsu31cUo0s0XcEEo0OE2YiL6Q%3D&se=2017-07-04T08%3A43%3A01Z&sp=w"
}
```
