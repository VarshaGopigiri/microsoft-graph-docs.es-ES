---
title: tipo de enumeración keyStorageProviderOption
description: Opciones de importación de almacenamiento de claves (KSP) del proveedor.
ms.openlocfilehash: 236489d288ec0be70a818e1c51b8c634ad3933a8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084044"
---
# <a name="keystorageprovideroption-enum-type"></a>tipo de enumeración keyStorageProviderOption

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Opciones de importación de almacenamiento de claves (KSP) del proveedor.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|useTpmKspOtherwiseUseSoftwareKsp|0|Importar a Trusted Platform Module (TPM) KSP si está presente, en caso contrario, importar a Software KSP.|
|useTpmKspOtherwiseFail|1|En caso contrario, producirá un error en la importación a Trusted Platform Module (TPM) KSP si está presente.|
|usePassportForWorkKspOtherwiseFail|2|Importar a la cuenta de Passport para el trabajo KSP si está disponible, en caso contrario, producirá un error.|
|useSoftwareKsp|3|Importación a Software KSP.|





