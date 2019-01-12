---
title: tipo enum de habilitación
description: 'Valores utilizados para indicar el estado de un dispositivo. '
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 539d57111003f348147a6be3952d969ab4206b5d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911962"
---
# <a name="enablement-enum-type"></a>tipo enum de habilitación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores utilizados para indicar el estado de un dispositivo. 

Tenga en cuenta que hay una diferencia entre deshabilitado y no está definida.

## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Valor predeterminado de dispositivo, sin intención.|
|enabled|1|Habilita a la configuración en el dispositivo.|
|deshabilitado|2|Deshabilita a la configuración en el dispositivo.|
