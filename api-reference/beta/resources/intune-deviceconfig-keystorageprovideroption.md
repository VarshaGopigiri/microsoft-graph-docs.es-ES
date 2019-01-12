---
title: tipo de enumeración keyStorageProviderOption
description: Opciones de importación de almacenamiento de claves (KSP) del proveedor.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8f3a8169b4bb6cd2357f02aa7fec89ba640780f7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946556"
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





