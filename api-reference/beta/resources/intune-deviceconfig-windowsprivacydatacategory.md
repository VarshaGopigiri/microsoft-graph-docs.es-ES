---
title: tipo de enumeración windowsPrivacyDataCategory
description: Especificador de categoría de Windows privacidad datos para el acceso a datos de privacidad.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 03a7e1d7f017d7c7df9c27257c8f2a3e01c861d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931191"
---
# <a name="windowsprivacydatacategory-enum-type"></a>tipo de enumeración windowsPrivacyDataCategory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especificador de categoría de Windows privacidad datos para el acceso a datos de privacidad.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Ningún nivel de acceso no especificado, del color. Es posible que se comportan de dispositivo ya sea como en UserInControl o ForceAllow. Es posible que dependen de los datos de privacidad sido tener acceso a las versiones de Windows y otros factores.|
|accountInfo|1|Permiten el nombre del usuario de acceso de aplicaciones, imágenes y otra información de cuenta creado en la cuenta de Microsoft. Se agregó en Windows 10, versión 1607.|
|appsRunInBackground|2|Permitir aplicaciones recibir la información, enviar notificaciones y mantenerse actualizados, incluso cuando el usuario no está utilizando. Tenga en cuenta que al deshabilitar aplicaciones de comunicación (correo electrónico, voz, etcetera) desde access fondo estas aplicaciones pueden o no funcionen como con el acceso de fondo. Se agregó en Windows 10, versión 1703.|
|calendario|3|Permiten calendario del usuario de acceso de aplicaciones. Se agregó en Windows 10, versión 1607.|
|callHistory|4|Permiten historial de llamadas del usuario de acceso de aplicaciones. Se agregó en Windows 10, versión 1607.|
|cámara|5|Permitir que aplicaciones tener acceso a la cámara en el dispositivo del usuario. Se agregó en Windows 10, versión 1607.|
|contactos|6|Permiten la información de contacto del usuario de acceso de aplicaciones. Se agregó en Windows 10, versión 1607.|
|diagnosticsInfo|7|Permitir que aplicaciones tener acceso a información de diagnóstico acerca de la ejecución de otras aplicaciones. Se agregó en Windows 10, versión 1703.|
|email|8|Permiten el acceso de aplicaciones y enviar correo electrónico. Se agregó en Windows 10, versión 1607.|
|location|9|Permitir que aplicaciones tener acceso a los datos de ubicación precisa de usuario del dispositivo. Se agregó en Windows 10, versión 1607.|
|mensajería|10|Permitir que aplicaciones leer o enviar mensajes, texto o MMS. Se agregó en Windows 10, versión 1607.|
|microphone|11|Permiten a aplicaciones usar micrófono en el dispositivo del usuario. Se agregó en Windows 10, versión 1607.|
|movimiento|12|Permiten a aplicaciones usar datos de movimiento generados en el usuario del dispositivo. Se agregó en Windows 10, versión 1607.|
|notificaciones|13|Permitir que las notificaciones del usuario de acceso de aplicaciones. Se agregó en Windows 10, versión 1607.|
|phone|14|Permiten el acceso de aplicaciones de datos de teléfono y realizar llamadas de teléfono. Se agregó en Windows 10, versión 1607.|
|radios|15|Permiten a aplicaciones usar radios, incluyendo Bluetooth, enviar y recibir datos. Se agregó en Windows 10, versión 1607.|
|tasks|16|Acceso de aplicaciones permiten que el programador de tareas. Se agregó en Windows 10, versión 1703.|
|syncWithDevices|17|Permitir que aplicaciones automáticamente compartir y sincronizar la información con los dispositivos inalámbricos que explícitamente no emparejar con dispositivo del usuario. Se agregó en Windows 10, versión 1607.|
|trustedDevices|18|Permitir que aplicaciones tener acceso a dispositivos de confianza. Se agregó en Windows 10, versión 1607.|





