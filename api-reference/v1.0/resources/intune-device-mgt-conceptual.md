---
title: Administración de dispositivos en Microsoft Intune
description: ''
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 72ff8234696c8a6d1f74bd7468d24e98c54e5052
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868365"
---
# <a name="device-management-in-microsoft-intune"></a><span data-ttu-id="ce662-102">Administración de dispositivos en Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ce662-102">Device management in Microsoft Intune</span></span>

> <span data-ttu-id="ce662-103">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce662-103">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

- [<span data-ttu-id="ce662-104">Estado de acción</span><span class="sxs-lookup"><span data-stu-id="ce662-104">Action state</span></span>](intune-devices-actionstate.md)
- [<span data-ttu-id="ce662-105">Certificado de notificación de inserción de Apple</span><span class="sxs-lookup"><span data-stu-id="ce662-105">Apple push notification certificate</span></span>](intune-devices-applepushnotificationcertificate.md)
- [<span data-ttu-id="ce662-106">Actor de auditoría</span><span class="sxs-lookup"><span data-stu-id="ce662-106">Audit actor</span></span>](intune-auditing-auditactor.md)
- [<span data-ttu-id="ce662-107">Evento de auditoría</span><span class="sxs-lookup"><span data-stu-id="ce662-107">Audit event</span></span>](intune-auditing-auditevent.md)
- [<span data-ttu-id="ce662-108">Propiedad de auditoría</span><span class="sxs-lookup"><span data-stu-id="ce662-108">Audit property</span></span>](intune-auditing-auditproperty.md)
- [<span data-ttu-id="ce662-109">Recurso de auditoría</span><span class="sxs-lookup"><span data-stu-id="ce662-109">Audit resource</span></span>](intune-auditing-auditresource.md)
- [<span data-ttu-id="ce662-110">Estado de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="ce662-110">Compliance state</span></span>](intune-devices-compliancestate.md)
- [<span data-ttu-id="ce662-111">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ce662-111">Configuration manager client enabled features</span></span>](intune-devices-configurationmanagerclientenabledfeatures.md)
- [<span data-ttu-id="ce662-112">Resultado de la acción Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="ce662-112">Delete user from shared Apple device action result</span></span>](intune-devices-deleteuserfromsharedappledeviceactionresult.md)
- [<span data-ttu-id="ce662-113">Aplicación detectada</span><span class="sxs-lookup"><span data-stu-id="ce662-113">Detected app</span></span>](intune-devices-detectedapp.md)
- [<span data-ttu-id="ce662-114">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce662-114">Device action result</span></span>](intune-devices-deviceactionresult.md)
- [<span data-ttu-id="ce662-115">Motivo del error de inscripción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce662-115">Device enrollment failure reason</span></span>](intune-troubleshooting-deviceenrollmentfailurereason.md)
- [<span data-ttu-id="ce662-116">Tipo de dispositivo de inscripción</span><span class="sxs-lookup"><span data-stu-id="ce662-116">Device enrollment type</span></span>](intune-devices-deviceenrollmenttype.md)
- [<span data-ttu-id="ce662-117">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="ce662-117">Device exchange access state summary</span></span>](intune-devices-deviceexchangeaccessstatesummary.md)
- [<span data-ttu-id="ce662-118">Geolocalización de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce662-118">Device geolocation</span></span>](intune-devices-devicegeolocation.md)
- [<span data-ttu-id="ce662-119">Estado de la atestación de estado del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce662-119">Device health attestation state</span></span>](intune-devices-devicehealthattestationstate.md)
- [<span data-ttu-id="ce662-120">Estado de acceso de exchange de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce662-120">Device management exchange access state</span></span>](intune-devices-devicemanagementexchangeaccessstate.md)
- [<span data-ttu-id="ce662-121">Motivo del estado de acceso de dispositivo administración exchange</span><span class="sxs-lookup"><span data-stu-id="ce662-121">Device management exchange access state reason</span></span>](intune-devices-devicemanagementexchangeaccessstatereason.md)
- [<span data-ttu-id="ce662-122">Estado de suscripción de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce662-122">Device management subscription state</span></span>](intune-devices-devicemanagementsubscriptionstate.md)
- [<span data-ttu-id="ce662-123">Evento de solución de problemas de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce662-123">Device management troubleshooting event</span></span>](intune-troubleshooting-devicemanagementtroubleshootingevent.md)
- [<span data-ttu-id="ce662-124">Resumen de sistemas operativos de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ce662-124">Device operating system summary</span></span>](intune-devices-deviceoperatingsystemsummary.md)
- [<span data-ttu-id="ce662-125">Estado de registro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce662-125">Device registration state</span></span>](intune-devices-deviceregistrationstate.md)
- [<span data-ttu-id="ce662-126">Evento de solución de problemas de inscripción</span><span class="sxs-lookup"><span data-stu-id="ce662-126">Enrollment troubleshooting event</span></span>](intune-troubleshooting-enrollmenttroubleshootingevent.md)
- [<span data-ttu-id="ce662-127">Mensaje de notificación localizado</span><span class="sxs-lookup"><span data-stu-id="ce662-127">Localized notification message</span></span>](intune-notification-localizednotificationmessage.md)
- [<span data-ttu-id="ce662-128">Resultado de la acción Buscar dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce662-128">Locate device action result</span></span>](intune-devices-locatedeviceactionresult.md)
- [<span data-ttu-id="ce662-129">Dispositivo administrado</span><span class="sxs-lookup"><span data-stu-id="ce662-129">Managed device</span></span>](intune-devices-manageddevice.md)
- [<span data-ttu-id="ce662-130">Resumen de dispositivos administrados</span><span class="sxs-lookup"><span data-stu-id="ce662-130">Managed device overview</span></span>](intune-devices-manageddeviceoverview.md)
- [<span data-ttu-id="ce662-131">El tipo de propietario de dispositivo administrado</span><span class="sxs-lookup"><span data-stu-id="ce662-131">Managed device owner type</span></span>](intune-devices-manageddeviceownertype.md)
- [<span data-ttu-id="ce662-132">Socio de dispositivos administrados notifiquen el estado de mantenimiento</span><span class="sxs-lookup"><span data-stu-id="ce662-132">Managed device partner reported health state</span></span>](intune-devices-manageddevicepartnerreportedhealthstate.md)
- [<span data-ttu-id="ce662-133">Tipo de agente de administración</span><span class="sxs-lookup"><span data-stu-id="ce662-133">Management agent type</span></span>](intune-devices-managementagenttype.md)
- [<span data-ttu-id="ce662-134">Plantilla de mensaje de notificación</span><span class="sxs-lookup"><span data-stu-id="ce662-134">Notification message template</span></span>](intune-notification-notificationmessagetemplate.md)
- [<span data-ttu-id="ce662-135">Opciones de personalización de marca de plantilla de notificación</span><span class="sxs-lookup"><span data-stu-id="ce662-135">Notification template branding options</span></span>](intune-notification-notificationtemplatebrandingoptions.md)
- [<span data-ttu-id="ce662-136">Estado de la incorporación de asistencia remota</span><span class="sxs-lookup"><span data-stu-id="ce662-136">Remote assistance on-boarding status</span></span>](intune-remoteassistance-remoteassistanceonboardingstatus.md)
- [<span data-ttu-id="ce662-137">Asociado de asistencia remota</span><span class="sxs-lookup"><span data-stu-id="ce662-137">Remote assistance partner</span></span>](intune-remoteassistance-remoteassistancepartner.md)
- [<span data-ttu-id="ce662-138">Resultado de la acción Bloqueo remoto</span><span class="sxs-lookup"><span data-stu-id="ce662-138">Remote lock action result</span></span>](intune-devices-remotelockactionresult.md)
- [<span data-ttu-id="ce662-139">Resultado de la acción Restablecer código de acceso</span><span class="sxs-lookup"><span data-stu-id="ce662-139">Reset passcode action result</span></span>](intune-devices-resetpasscodeactionresult.md)
- [<span data-ttu-id="ce662-140">Parámetro de la acción Actualizar la cuenta del dispositivo Windows</span><span class="sxs-lookup"><span data-stu-id="ce662-140">Update windows device account action parameter</span></span>](intune-devices-updatewindowsdeviceaccountactionparameter.md)
- [<span data-ttu-id="ce662-141">Resultado de la acción Examinar de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="ce662-141">Windows defender scan action result</span></span>](intune-devices-windowsdefenderscanactionresult.md)
- [<span data-ttu-id="ce662-142">Cuenta del dispositivo Windows</span><span class="sxs-lookup"><span data-stu-id="ce662-142">Windows device account</span></span>](intune-devices-windowsdeviceaccount.md)
- [<span data-ttu-id="ce662-143">Cuenta de AD del dispositivo Windows</span><span class="sxs-lookup"><span data-stu-id="ce662-143">Windows device AD account</span></span>](intune-devices-windowsdeviceadaccount.md)
- [<span data-ttu-id="ce662-144">Cuenta de Azure AD del dispositivo Windows</span><span class="sxs-lookup"><span data-stu-id="ce662-144">Windows device Azure AD account</span></span>](intune-devices-windowsdeviceazureadaccount.md)
