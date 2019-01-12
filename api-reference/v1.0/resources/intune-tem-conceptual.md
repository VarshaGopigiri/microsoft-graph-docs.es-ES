---
title: Administración de gastos de telecomunicaciones en Microsoft Intune
description: Puede limitar el uso de datos e itinerancia en dispositivos de propiedad corporativa al usar el servicio de administración de gastos de telecomunicaciones de Saaswedo, que se integra con Intune. El servicio le permite establecer y aplicar límites de uso y enviar una alerta a los usuarios cuando superen el límite configurado. También puede configurar el servicio para que realice diferentes acciones, como deshabilitar la itinerancia, cuando los usuarios superan el límite. En la consola de Saaswedo tiene los informes que proporcionan la información del uso de datos y de supervisión. Para poder usar el servicio de administración de gastos de telecomunicaciones de Saaswedo con Intune, debe configurar los ajustes en una consola de Saaswedo y en Intune. La conexión debe estar activada para el servicio de Saaswedo e Intune. Si la conexión del lado de Saaswedo está habilitada, pero no lo está en el lado Intune, Intune recibe la comunicación, pero la ignora.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 7ae9aefc3504de430b11c2d80a8cf51906426d16
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970468"
---
# <a name="telecom-expense-management-in-microsoft-intune"></a>Administración de gastos de telecomunicaciones en Microsoft Intune

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

Puede limitar el uso de datos e itinerancia en dispositivos de propiedad corporativa al usar el servicio de administración de gastos de telecomunicaciones de Saaswedo, que se integra con Intune. El servicio le permite establecer y aplicar límites de uso y enviar una alerta a los usuarios cuando superen el límite configurado. También puede configurar el servicio para que realice diferentes acciones, como deshabilitar la itinerancia, cuando los usuarios superan el límite. En la consola de Saaswedo tiene los informes que proporcionan la información del uso de datos y de supervisión. Para poder usar el servicio de administración de gastos de telecomunicaciones de Saaswedo con Intune, debe configurar los ajustes en una consola de Saaswedo y en Intune. La conexión debe estar activada para el servicio de Saaswedo e Intune. Si la conexión del lado de Saaswedo está habilitada, pero no lo está en el lado Intune, Intune recibe la comunicación, pero la ignora.

Los siguientes recursos de Graph están disponibles para administrar los gastos de telecomunicaciones en Intune:  

- [Partner de administración de gastos de telecomunicaciones](intune-tem-telecomexpensemanagementpartner.md)
