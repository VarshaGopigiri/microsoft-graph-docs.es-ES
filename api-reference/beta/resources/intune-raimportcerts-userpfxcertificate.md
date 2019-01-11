---
title: tipo de recurso userPFXCertificate
description: Entidad que encapsula toda la información necesaria para los certificados PFX de un usuario.
localization_priority: Normal
ms.openlocfilehash: 87516c48e53c8117c9efa119fb6cab62844e6b68
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809999"
---
# <a name="userpfxcertificate-resource-type"></a>tipo de recurso userPFXCertificate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que encapsula toda la información necesaria para los certificados PFX de un usuario.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista userPFXCertificates](../api/intune-raimportcerts-userpfxcertificate-list.md)|colección de [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Propiedades de la lista y relaciones de los objetos [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|
|[Obtener userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-get.md)|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Leer las propiedades y las relaciones del objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|
|[Crear userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-create.md)|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Crear un nuevo objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|
|[Eliminar userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-delete.md)|Ninguno|Elimina un [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md).|
|[Actualizar userPFXCertificate](../api/intune-raimportcerts-userpfxcertificate-update.md)|[userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md)|Actualizar las propiedades de un objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único para el certificado PFX.|
|huella digital|Cadena|SHA-1 huella digital del certificado PFX.|
|intendedPurpose|[userPfxIntendedPurpose](../resources/intune-raimportcerts-userpfxintendedpurpose.md)|Del certificado propósito desde el punto de vista de la implementación. Los valores posibles son: `unassigned`, `smimeEncryption`, `smimeSigning`, `vpn` y `wifi`.|
|userPrincipalName|Cadena|Nombre Principal de usuario del certificado PFX.|
|startDateTime|DateTimeOffset|Fecha/hora de inicio de validez del certificado.|
|expirationDateTime|DateTimeOffset|Fecha de expiración de validez y hora del certificado.|
|providerName|Cadena|Proveedor de cifrado usado para cifrar este blob.|
|nombre de clave|Cadena|Nombre de la clave (en el proveedor) utilizada para cifrar el blob.|
|paddingScheme|[userPfxPaddingScheme](../resources/intune-raimportcerts-userpfxpaddingscheme.md)|Espaciado interno utilizado por el proveedor durante el cifrado y descifrado de combinación. Los valores posibles son: `none`, `pkcs1`, `oaepSha1`, `oaepSha256`, `oaepSha384`, `oaepSha512`.|
|encryptedPfxBlob|Binario|Blob PFX cifrado.|
|encryptedPfxPassword|Cadena|Contraseña PFX cifrada.|
|createdDateTime|DateTimeOffset|Fecha y hora cuando se importó este certificado PFX.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora cuando se modificó por última vez este certificado PFX.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userPFXCertificate"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userPFXCertificate",
  "id": "String (identifier)",
  "thumbprint": "String",
  "intendedPurpose": "String",
  "userPrincipalName": "String",
  "startDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "providerName": "String",
  "keyName": "String",
  "paddingScheme": "String",
  "encryptedPfxBlob": "binary",
  "encryptedPfxPassword": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)"
}
```





