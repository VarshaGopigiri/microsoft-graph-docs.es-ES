---
title: Configuración del dispositivo en Microsoft Intune
description: Use la carga de trabajo de la configuración de dispositivos de Microsoft Intune para administrar la configuración y las características en todos los dispositivos que administre.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7ea30ad4ad490390f7de0b5a5342d2040fe00716
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820198"
---
# <a name="device-configuration-in-microsoft-intune"></a>Configuración del dispositivo en Microsoft Intune

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

Use la carga de trabajo de la configuración de dispositivos de Microsoft Intune para administrar la configuración y las características en todos los dispositivos que administre.

Los siguientes recursos de Graph están disponibles para administrar la configuración y las características en Intune:

- [Directiva de cumplimiento de Android](intune-deviceconfig-androidcompliancepolicy.md)
- [Configuración personalizada de Android](intune-deviceconfig-androidcustomconfiguration.md)
- [Configuración general de dispositivos de Android](intune-deviceconfig-androidgeneraldeviceconfiguration.md)
- [Tipo de contraseña requerida para Android](intune-deviceconfig-androidrequiredpasswordtype.md)
- [Directiva de cumplimiento de perfil de trabajo para Android](intune-deviceconfig-androidworkprofilecompliancepolicy.md)
- [Perfil de trabajo Android entre el tipo de datos de perfil de uso compartido](intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)
- [Configuración personalizada de perfil de trabajo para Android](intune-deviceconfig-androidworkprofilecustomconfiguration.md)
- [Tipo de directiva de permisos de aplicación trabajo Android perfil predeterminado](intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)
- [Configuración de dispositivo general de perfil de trabajo para Android](intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)
- [Perfil de trabajo Android requiere contraseña, escriba](intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)
- [Elemento de lista de la aplicación](intune-deviceconfig-applistitem.md)
- [Tipo de aplicación de lista](intune-deviceconfig-applisttype.md)
- [Tipo de control de aplicación de bloqueo de aplicación](intune-deviceconfig-applockerapplicationcontroltype.md)
- [Base de configuración de características de dispositivos de Apple](intune-deviceconfig-appledevicefeaturesconfigurationbase.md)
- [Portapapeles de bloque de aplicación guardián del uso compartido de tipo](intune-deviceconfig-applicationguardblockclipboardsharingtype.md)
- [Tipo de transferencia de archivos de aplicación guardián del bloque](intune-deviceconfig-applicationguardblockfiletransfertype.md)
- [Modo de actualización automática](intune-deviceconfig-automaticupdatemode.md)
- [Método de cifrado de BitLocker](intune-deviceconfig-bitlockerencryptionmethod.md)
- [Directiva de unidad extraíble de BitLocker](intune-deviceconfig-bitlockerremovabledrivepolicy.md)
- [Día de la semana](intune-deviceconfig-dayofweek.md)
- [Tipo de nivel de bloque Defender en la nube](intune-deviceconfig-defendercloudblockleveltype.md)
- [Acciones de software malintencionado detectado por Defender](intune-deviceconfig-defenderdetectedmalwareactions.md)
- [Supervisar la actividad del archivo Defender](intune-deviceconfig-defendermonitorfileactivity.md)
- [Símbolo del sistema de Defender para el envío de ejemplo](intune-deviceconfig-defenderpromptforsamplesubmission.md)
- [Tipo de examen de Defender](intune-deviceconfig-defenderscantype.md)
- [Acción de amenaza Defender](intune-deviceconfig-defenderthreataction.md)
- [Elemento de acción de cumplimiento de dispositivos](intune-deviceconfig-devicecomplianceactionitem.md)
- [Tipo de acción de cumplimiento de normas de dispositivo](intune-deviceconfig-devicecomplianceactiontype.md)
- [Información general del dispositivo sobre el cumplimiento de dispositivos](intune-deviceconfig-devicecompliancedeviceoverview.md)
- [Estado del dispositivo de cumplimiento de dispositivos](intune-deviceconfig-devicecompliancedevicestatus.md)
- [Directiva de cumplimiento de dispositivos](intune-deviceconfig-devicecompliancepolicy.md)
- [Asignación de directivas de cumplimiento de dispositivos.](intune-deviceconfig-devicecompliancepolicyassignment.md)
- [Resumen de estado de dispositivo de directiva de cumplimiento de dispositivos](intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)
- [Estado de configuración de la directiva de cumplimiento de dispositivos](intune-deviceconfig-devicecompliancepolicysettingstate.md)
- [Resumen de estado de configuración de directiva de cumplimiento de dispositivos](intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)
- [Acción programada de cumplimiento de dispositivos para la regla](intune-deviceconfig-devicecompliancescheduledactionforrule.md)
- [Estado de configuración del cumplimiento de dispositivos](intune-deviceconfig-devicecompliancesettingstate.md)
- [Información general del usuario de cumplimiento de dispositivos](intune-deviceconfig-devicecomplianceuseroverview.md)
- [Estado del usuario de cumplimiento de dispositivos](intune-deviceconfig-devicecomplianceuserstatus.md)
- [Configuración de dispositivos](intune-deviceconfig-deviceconfiguration.md)
- [Asignación de configuración de dispositivos](intune-deviceconfig-deviceconfigurationassignment.md)
- [Información general del dispositivo sobre la configuración de dispositivos](intune-deviceconfig-deviceconfigurationdeviceoverview.md)
- [Resumen de estado de dispositivo de configuración de dispositivo](intune-deviceconfig-deviceconfigurationdevicestatesummary.md)
- [Estado del dispositivo de la configuración de dispositivos](intune-deviceconfig-deviceconfigurationdevicestatus.md)
- [Estado de configuración de la configuración de dispositivos](intune-deviceconfig-deviceconfigurationsettingstate.md)
- [Información general del usuario sobre la configuración de dispositivos](intune-deviceconfig-deviceconfigurationuseroverview.md)
- [Estado del usuario de la configuración de dispositivos](intune-deviceconfig-deviceconfigurationuserstatus.md)
- [Configuración de administración de dispositivos](intune-deviceconfig-devicemanagementsettings.md)
- [Nivel de protección de amenaza de dispositivo](intune-deviceconfig-devicethreatprotectionlevel.md)
- [Modo de envío de datos de diagnóstico](intune-deviceconfig-diagnosticdatasubmissionmode.md)
- [Directiva de cookie de borde](intune-deviceconfig-edgecookiepolicy.md)
- [Motor de búsqueda de Edge](intune-deviceconfig-edgesearchengine.md)
- [Base de motor de búsqueda de Edge](intune-deviceconfig-edgesearchenginebase.md)
- [Motor de búsqueda de Edge personalizado](intune-deviceconfig-edgesearchenginecustom.md)
- [Tipo de motor de búsqueda de borde](intune-deviceconfig-edgesearchenginetype.md)
- [Configuración de la actualización de edición](intune-deviceconfig-editionupgradeconfiguration.md)
- [Tipo de licencia de edición de actualización](intune-deviceconfig-editionupgradelicensetype.md)
- [Lista de revocación de certificados de servidor de seguridad comprobar tipo (método)](intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)
- [Tipo de servidor de seguridad paquete queueing (método)](intune-deviceconfig-firewallpacketqueueingmethodtype.md)
- [Clave compartida previamente de Firewall, tipo de método de codificación](intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)
- [Nivel de seguridad de sitios de Internet](intune-deviceconfig-internetsitesecuritylevel.md)
- [Perfil de certificado de iOS](intune-deviceconfig-ioscertificateprofile.md)
- [Directiva de cumplimiento de iOS](intune-deviceconfig-ioscompliancepolicy.md)
- [Configuración personalizada de iOS](intune-deviceconfig-ioscustomconfiguration.md)
- [Configuración de características de dispositivos iOS](intune-deviceconfig-iosdevicefeaturesconfiguration.md)
- [Configuración general de dispositivos de iOS](intune-deviceconfig-iosgeneraldeviceconfiguration.md)
- [Aplicación de la pantalla de inicio de iOS](intune-deviceconfig-ioshomescreenapp.md)
- [Carpeta para la pantalla de inicio de iOS](intune-deviceconfig-ioshomescreenfolder.md)
- [Página de la carpeta para la pantalla de inicio de iOS](intune-deviceconfig-ioshomescreenfolderpage.md)
- [Elemento de la pantalla de inicio de iOS](intune-deviceconfig-ioshomescreenitem.md)
- [Página de la pantalla de inicio de iOS](intune-deviceconfig-ioshomescreenpage.md)
- [Regla de uso de red de iOS](intune-deviceconfig-iosnetworkusagerule.md)
- [tipo de notificación de alerta de iOS](intune-deviceconfig-iosnotificationalerttype.md)
- [Configuración de notificaciones de iOS](intune-deviceconfig-iosnotificationsettings.md)
- [Configuración de actualización de iOS](intune-deviceconfig-iosupdateconfiguration.md)
- [Estado del dispositivo de actualización de iOS](intune-deviceconfig-iosupdatedevicestatus.md)
- [estado de la instalación de actualizaciones de iOS](intune-deviceconfig-iosupdatesinstallstatus.md)
- [Directiva de cumplimiento de macOS](intune-deviceconfig-macoscompliancepolicy.md)
- [Configuración personalizada de macOS](intune-deviceconfig-macoscustomconfiguration.md)
- [Configuración de características de dispositivos MacOS](intune-deviceconfig-macosdevicefeaturesconfiguration.md)
- [Configuración general de dispositivos de macOS](intune-deviceconfig-macosgeneraldeviceconfiguration.md)
- [Clasificación del contenido multimedia de Australia](intune-deviceconfig-mediacontentratingaustralia.md)
- [Clasificación del contenido multimedia de Canadá](intune-deviceconfig-mediacontentratingcanada.md)
- [Clasificación del contenido multimedia de Francia](intune-deviceconfig-mediacontentratingfrance.md)
- [Clasificación del contenido multimedia de Alemania](intune-deviceconfig-mediacontentratinggermany.md)
- [Clasificación del contenido multimedia de Irlanda](intune-deviceconfig-mediacontentratingireland.md)
- [Clasificación del contenido multimedia de Japón](intune-deviceconfig-mediacontentratingjapan.md)
- [Clasificación del contenido multimedia de Nueva Zelanda](intune-deviceconfig-mediacontentratingnewzealand.md)
- [Clasificación del contenido multimedia del Reino Unido](intune-deviceconfig-mediacontentratingunitedkingdom.md)
- [Clasificación de contenido multimedia de Estados Unidos](intune-deviceconfig-mediacontentratingunitedstates.md)
- [Canal de Miracast](intune-deviceconfig-miracastchannel.md)
- [Configuración de OMA](intune-deviceconfig-omasetting.md)
- [Base64 de la configuración de OMA](intune-deviceconfig-omasettingbase64.md)
- [Booleano de la configuración de OMA](intune-deviceconfig-omasettingboolean.md)
- [Fecha y hora de la configuración de OMA](intune-deviceconfig-omasettingdatetime.md)
- [Número de punto flotante de la configuración de OMA](intune-deviceconfig-omasettingfloatingpoint.md)
- [Entero de la configuración de OMA](intune-deviceconfig-omasettinginteger.md)
- [Cadena de configuración de OMA](intune-deviceconfig-omasettingstring.md)
- [Cadena de configuración XML de OMA](intune-deviceconfig-omasettingstringxml.md)
- [Tipo de plataforma de directiva](intune-deviceconfig-policyplatformtype.md)
- [Características de la versión preliminares](intune-deviceconfig-prereleasefeatures.md)
- [Tipo de aplicaciones de clasificación](intune-deviceconfig-ratingappstype.md)
- [Tipo de Australia películas de clasificación](intune-deviceconfig-ratingaustraliamoviestype.md)
- [Tipo de televisión Australia de clasificación](intune-deviceconfig-ratingaustraliatelevisiontype.md)
- [Tipo de Canadá películas de clasificación](intune-deviceconfig-ratingcanadamoviestype.md)
- [Tipo de televisión de clasificación Canadá](intune-deviceconfig-ratingcanadatelevisiontype.md)
- [Tipo de clasificación Francia películas](intune-deviceconfig-ratingfrancemoviestype.md)
- [Tipo de televisión de clasificación Francia](intune-deviceconfig-ratingfrancetelevisiontype.md)
- [Tipo de Alemania películas de clasificación](intune-deviceconfig-ratinggermanymoviestype.md)
- [Tipo de televisión de Alemania de clasificación](intune-deviceconfig-ratinggermanytelevisiontype.md)
- [Clasificación de tipo de películas (Irlanda)](intune-deviceconfig-ratingirelandmoviestype.md)
- [Tipo de televisión de clasificación (Irlanda)](intune-deviceconfig-ratingirelandtelevisiontype.md)
- [Tipo de Japón películas de clasificación](intune-deviceconfig-ratingjapanmoviestype.md)
- [Tipo de televisión de Japón de clasificación](intune-deviceconfig-ratingjapantelevisiontype.md)
- [Tipo de Nueva Zelanda películas de clasificación](intune-deviceconfig-ratingnewzealandmoviestype.md)
- [Clasificación de tipo de televisión de Nueva Zelanda](intune-deviceconfig-ratingnewzealandtelevisiontype.md)
- [Clasificación de tipo de películas Reino Unido](intune-deviceconfig-ratingunitedkingdommoviestype.md)
- [Clasificación de tipo de televisión Reino Unido](intune-deviceconfig-ratingunitedkingdomtelevisiontype.md)
- [Clasificación de tipo de películas de Estados Unidos](intune-deviceconfig-ratingunitedstatesmoviestype.md)
- [Tipo de televisión de Estados Unidos de clasificación](intune-deviceconfig-ratingunitedstatestelevisiontype.md)
- [Requiere contraseña, escriba](intune-deviceconfig-requiredpasswordtype.md)
- [Tipo de filtro de búsqueda segura](intune-deviceconfig-safesearchfiltertype.md)
- [Origen de la configuración](intune-deviceconfig-settingsource.md)
- [Resumen de dispositivo de estado de configuración](intune-deviceconfig-settingstatedevicesummary.md)
- [Tipo de directiva de eliminación de PC cuenta compartido](intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)
- [Directiva de administrador de cuentas de PC compartida](intune-deviceconfig-sharedpcaccountmanagerpolicy.md)
- [Shared PC permitida el tipo de cuenta](intune-deviceconfig-sharedpcallowedaccounttype.md)
- [Configuración de PC compartida](intune-deviceconfig-sharedpcconfiguration.md)
- [Nivel de seguridad de sitios](intune-deviceconfig-sitesecuritylevel.md)
- [Resumen del estado de la actualización de software](intune-deviceconfig-softwareupdatestatussummary.md)
- [Configuración de la administración de estado](intune-deviceconfig-statemanagementsetting.md)
- [Configuración de visibilidad](intune-deviceconfig-visibilitysetting.md)
- [Configuración de cookies de explorador Web](intune-deviceconfig-webbrowsercookiesettings.md)
- [Programación semanal](intune-deviceconfig-weeklyschedule.md)
- [Información de la reunión de pantalla de bienvenida](intune-deviceconfig-welcomescreenmeetinginformation.md)
- [Directiva de cumplimiento de Windows 10](intune-deviceconfig-windows10compliancepolicy.md)
- [Configuración personalizada de Windows 10](intune-deviceconfig-windows10customconfiguration.md)
- [Tipo de edición del 10 de Windows](intune-deviceconfig-windows10editiontype.md)
- [Configuración de Windows 10 Endpoint Protection](intune-deviceconfig-windows10endpointprotectionconfiguration.md)
- [Configuración de administración de aplicaciones modernas de Windows 10 Enterprise](intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md)
- [Configuración general de Windows 10](intune-deviceconfig-windows10generalconfiguration.md)
- [Directiva de cumplimiento de dispositivos móviles de Windows 10](intune-deviceconfig-windows10mobilecompliancepolicy.md)
- [Servidor proxy de red de Windows 10](intune-deviceconfig-windows10networkproxyserver.md)
- [Configuración de la evaluación segura de Windows 10](intune-deviceconfig-windows10secureassessmentconfiguration.md)
- [Configuración general de Windows 10 Team](intune-deviceconfig-windows10teamgeneralconfiguration.md)
- [Directiva de cumplimiento de Windows 8.1](intune-deviceconfig-windows81compliancepolicy.md)
- [Configuración general de Windows 8.1](intune-deviceconfig-windows81generalconfiguration.md)
- [Configuración de Protección contra amenazas avanzada de Windows Defender](intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md)
- [Modo de optimización de entrega de Windows](intune-deviceconfig-windowsdeliveryoptimizationmode.md)
- [Perfil de red del Firewall de Windows](intune-deviceconfig-windowsfirewallnetworkprofile.md)
- [Directiva de cumplimiento de Windows Phone 8.1](intune-deviceconfig-windowsphone81compliancepolicy.md)
- [Configuración personalizada de Windows Phone 8.1](intune-deviceconfig-windowsphone81customconfiguration.md)
- [Configuración general de Windows Phone 8.1](intune-deviceconfig-windowsphone81generalconfiguration.md)
- [Configuración de la habilitación de foco de Windows](intune-deviceconfig-windowsspotlightenablementsettings.md)
- [Tipo de visibilidad de lista de aplicación de menú de inicio de Windows](intune-deviceconfig-windowsstartmenuapplistvisibilitytype.md)
- [Tipo de modo de menú de inicio de Windows](intune-deviceconfig-windowsstartmenumodetype.md)
- [Instalación de horas activas de actualización de Windows](intune-deviceconfig-windowsupdateactivehoursinstall.md)
- [Configuración de actualización de Windows para empresas.](intune-deviceconfig-windowsupdateforbusinessconfiguration.md)
- [Tipo de programación de la instalación de actualizaciones de Windows](intune-deviceconfig-windowsupdateinstallscheduletype.md)
- [Instalación programada de actualizaciones de Windows](intune-deviceconfig-windowsupdatescheduledinstall.md)
- [Tipo de actualización de Windows](intune-deviceconfig-windowsupdatetype.md)
- [Configuración de control de cuentas de usuario de Windows](intune-deviceconfig-windowsuseraccountcontrolsettings.md)
