---
title: Cómo proteger los datos empresariales de aplicaciones con Microsoft Intune
description: Las directivas de protección de aplicaciones de Microsoft Intune ayudan a proteger los datos empresariales y evitar la pérdida de datos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 03b0db7a2bc2b79edf0156939b9ddb8e89f84dbd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810048"
---
# <a name="how-to-protect-your-company-app-data-with-microsoft-intune"></a>Cómo proteger los datos empresariales de aplicaciones con Microsoft Intune

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

Las directivas de protección de aplicaciones de Microsoft Intune ayudan a proteger los datos empresariales y evitar la pérdida de datos.

Puede usar las directivas de protección de aplicaciones de Intune para ayudar a proteger los datos de su empresa. Debido a que las directivas de protección de aplicaciones de Intune se pueden usar de forma independiente de cualquier solución de administración de dispositivos móviles (MDM), protege los datos de su empresa con o sin inscribir los dispositivos en una solución de administración de dispositivos. Mediante la implementación de directivas de nivel de aplicación, puede restringir el acceso a los recursos de la empresa y mantener los datos dentro del ámbito del departamento de TI.

Los siguientes recursos de Graph están disponibles para administrar las directivas de protección de aplicaciones en Intune:  

- [Protección de aplicaciones administradas de Android](intune-mam-androidmanagedappprotection.md)
- [Registro de aplicaciones administradas de Android](intune-mam-androidmanagedappregistration.md)
- [Identificador de aplicaciones para móviles de Android](intune-mam-androidmobileappidentifier.md)
- [Tipo de aplicación](intune-wip-applicationtype.md)
- [Protección predeterminada de aplicaciones administradas](intune-mam-defaultmanagedappprotection.md)
- [Protección de aplicaciones administradas de iOS](intune-mam-iosmanagedappprotection.md)
- [Registro de aplicaciones administradas de iOS](intune-mam-iosmanagedappregistration.md)
- [Identificador de aplicaciones para móviles de iOS](intune-mam-iosmobileappidentifier.md)
- [Intervalo IP](intune-mam-iprange.md)
- [Intervalo IPv4](intune-mam-ipv4range.md)
- [Intervalo IPv6](intune-mam-ipv6range.md)
- [JSON](intune-mam-json.md)
- [Par clave-valor](intune-mam-keyvaluepair.md)
- [Administrado de uso compartido de nivel de Portapapeles de aplicación](intune-mam-managedappclipboardsharinglevel.md)
- [Configuración de aplicaciones administradas](intune-mam-managedappconfiguration.md)
- [Administra el tipo de cifrado de datos de aplicación](intune-mam-managedappdataencryptiontype.md)
- [Ubicación de almacenamiento de datos de aplicación administrada](intune-mam-managedappdatastoragelocation.md)
- [Nivel de transferencia de datos de aplicación administrada](intune-mam-managedappdatatransferlevel.md)
- [Estado de diagnóstico de aplicaciones administradas](intune-mam-managedappdiagnosticstatus.md)
- [Motivo de la aplicación administrada marcado](intune-mam-managedappflaggedreason.md)
- [Operación de aplicaciones administradas](intune-mam-managedappoperation.md)
- [Conjunto de caracteres de la aplicación administrada PIN](intune-mam-managedapppincharacterset.md)
- [Directiva de aplicaciones administradas](intune-mam-managedapppolicy.md)
- [Resumen de implementación de directivas de aplicaciones administradas](intune-mam-managedapppolicydeploymentsummary.md)
- [Resumen de implementación de directivas de aplicaciones administradas por aplicación](intune-mam-managedapppolicydeploymentsummaryperapp.md)
- [Protección de aplicaciones administradas](intune-mam-managedappprotection.md)
- [Registro de aplicaciones administradas](intune-mam-managedappregistration.md)
- [Estado de las aplicaciones administradas](intune-mam-managedappstatus.md)
- [Estado de las aplicaciones administradas sin procesar](intune-mam-managedappstatusraw.md)
- [Aplicación móvil administrada](intune-mam-managedmobileapp.md)
- [Directiva de Windows Information Protection de MDM](intune-mam-mdmwindowsinformationprotectionpolicy.md)
- [Identificador de aplicaciones para móviles](intune-mam-mobileappidentifier.md)
- [Dominio con proxy](intune-mam-proxieddomain.md)
- [Configuración de aplicaciones administradas dirigidas](intune-mam-targetedmanagedappconfiguration.md)
- [Asignación de directiva de administración de aplicaciones objetivo](intune-mam-targetedmanagedapppolicyassignment.md)
- [Protección de aplicaciones administradas de objetivo](intune-mam-targetedmanagedappprotection.md)
- [Windows Information Protection](intune-mam-windowsinformationprotection.md)
- [Aplicación de Windows Information Protection](intune-mam-windowsinformationprotectionapp.md)
- [Resumen de aprendizaje sobre las aplicaciones de Windows Information Protection](intune-wip-windowsinformationprotectionapplearningsummary.md)
- [Archivo de bloqueo de aplicaciones de Windows Information Protection](intune-mam-windowsinformationprotectionapplockerfile.md)
- [Certificado de recuperación de datos de Windows Information Protection](intune-mam-windowsinformationprotectiondatarecoverycertificate.md)
- [Aplicación de escritorio de Windows Information Protection](intune-mam-windowsinformationprotectiondesktopapp.md)
- [Nivel de cumplimiento de protección de información de Windows](intune-mam-windowsinformationprotectionenforcementlevel.md)
- [Colección de intervalos IP de Windows Information Protection](intune-mam-windowsinformationprotectioniprangecollection.md)
- [Resumen de aprendizaje sobre la red de Windows Information Protection](intune-wip-windowsinformationprotectionnetworklearningsummary.md)
- [Requisitos de carácter PIN de protección de información de Windows](intune-mam-windowsinformationprotectionpincharacterrequirements.md)
- [Directiva de Windows Information Protection](intune-mam-windowsinformationprotectionpolicy.md)
- [Colección de dominios con proxy de Windows Information Protection](intune-mam-windowsinformationprotectionproxieddomaincollection.md)
- [Colección de recursos de Windows Information Protection](intune-mam-windowsinformationprotectionresourcecollection.md)
- [Aplicación de la tienda de Windows Information Protection](intune-mam-windowsinformationprotectionstoreapp.md)
