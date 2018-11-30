---
title: Inscribir dispositivos para administrarlos en Intune
description: " Inscripción (BYOD) permite a los usuarios inscribirse sus teléfonos personal, tabletas o PCs. La inscripción de dispositivos de propiedad corporativa permite escenarios de administración como el borrado remoto, dispositivos compartidos o afinidad de usuario para un dispositivo."
ms.openlocfilehash: af0a8ac113451c775386ee503026cf04a5641a7d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089315"
---
# <a name="enroll-devices-for-management-in-intune"></a>Inscribir dispositivos para administrarlos en Intune

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

Puede inscribir dispositivos, incluidos los equipos con Windows, para habilitar la administración de dispositivos móviles (MDM) con Microsoft Intune. Este tema describe las diferentes formas de inscribir dispositivos móviles en la administración de Intune. La forma en que inscribe los dispositivos depende del tipo de dispositivo, la propiedad y el nivel de administración que necesita. La inscripción "Bring Your Own Device" (BYOD) permite a los usuarios inscribir sus equipos, tabletas o teléfonos personales. La inscripción de dispositivos de propiedad corporativa permite escenarios de administración como el borrado remoto, dispositivos compartidos o afinidad de usuario para un dispositivo.

Los siguientes recursos de Graph están disponibles para administrar la inscripción en Intune:

- [Configuración del conector del certificado](intune-onboarding-certificateconnectorsetting.md)
- [Datos de administración de dispositivos y aplicación](intune-onboarding-deviceandappmanagementdata.md)
- [Configuración de la inscripción de dispositivos](intune-onboarding-deviceenrollmentconfiguration.md)
- [Configuración del límite de inscripción de dispositivos](intune-onboarding-deviceenrollmentlimitconfiguration.md)
- [Restricción de plataforma de inscripción de dispositivos](intune-onboarding-deviceenrollmentplatformrestriction.md)
- [Configuración de las restricciones de la plataforma de inscripción de dispositivos](intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md)
- [Configuración de Windows Hello para empresas para la inscripción de dispositivos](intune-onboarding-deviceenrollmentwindowshelloforbusinessconfiguration.md)
- [Nivel de acceso de exchange de administración de dispositivos](intune-onboarding-devicemanagementexchangeaccesslevel.md)
- [Regla de acceso de exchange de administración de dispositivos](intune-onboarding-devicemanagementexchangeaccessrule.md)
- [Tipo de regla de acceso de dispositivo administración exchange](intune-onboarding-devicemanagementexchangeaccessruletype.md)
- [Conector de Exchange de administración de dispositivos](intune-onboarding-devicemanagementexchangeconnector.md)
- [Estado del conector de exchange de administración de dispositivos](intune-onboarding-devicemanagementexchangeconnectorstatus.md)
- [Tipo de sincronización de conector de exchange de administración de dispositivo](intune-onboarding-devicemanagementexchangeconnectorsynctype.md)
- [Tipo de conector de exchange de administración de dispositivos](intune-onboarding-devicemanagementexchangeconnectortype.md)
- [Clase de dispositivo de exchange de administración de dispositivos](intune-onboarding-devicemanagementexchangedeviceclass.md)
- [Directiva de dispositivo administración exchange local](intune-onboarding-devicemanagementexchangeonpremisespolicy.md)
- [Partner de administración de dispositivos](intune-onboarding-devicemanagementpartner.md)
- [Tipo de aplicación de socio de administración de dispositivos](intune-onboarding-devicemanagementpartnerapptype.md)
- [Estado de inquilino de socio de administración de dispositivos](intune-onboarding-devicemanagementpartnertenantstate.md)
- [Tarea de configuración de inscripción](intune-onboarding-enrollmentconfigurationassignment.md)
- [Marca Intune](intune-onboarding-intunebrand.md)
- [Entidad de certificación MDM](intune-onboarding-mdmauthority.md)
- [Almacén de Microsoft para las opciones de selección del portal de negocio](intune-onboarding-microsoftstoreforbusinessportalselectionoptions.md)
- [Conector de Mobile Threat Defense](intune-onboarding-mobilethreatdefenseconnector.md)
- [Estado de inquilino de socio de amenaza móvil](intune-onboarding-mobilethreatpartnertenantstate.md)
- [Configuración de acceso condicional local](intune-onboarding-onpremisesconditionalaccesssettings.md)
- [Organización](intune-onboarding-organization.md)
- [Clave de carga de lado](intune-onboarding-sideloadingkey.md)
- [Símbolo (token) VPP](intune-onboarding-vpptoken.md)
- [Resultado de la acción de símbolo (token) de VPP](intune-onboarding-vpptokenactionresult.md)
- [Resumen de licencias VPP símbolo (token)](intune-onboarding-vpptokenlicensesummary.md)
- [Resultado de la acción de licencias VPP revoke símbolo (token)](intune-onboarding-vpptokenrevokelicensesactionresult.md)
- [Estado de token VPP](intune-onboarding-vpptokenstate.md)
- [Estado de la sincronización de símbolo (token) de VPP](intune-onboarding-vpptokensyncstatus.md)
- [Configuración de página de finalización de inscripción 10 de Windows](intune-onboarding-windows10enrollmentcompletionpageconfiguration.md)
- [Windows Hello para uso PIN de negocio](intune-onboarding-windowshelloforbusinesspinusage.md)
