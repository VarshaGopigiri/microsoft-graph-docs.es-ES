---
title: Crear mobileThreatDefenseConnector
description: Cree un objeto mobileThreatDefenseConnector.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 056e732835fc14a56381796d7a42195300175b99
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934201"
---
# <a name="create-mobilethreatdefenseconnector"></a><span data-ttu-id="85c9c-103">Crear mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="85c9c-103">Create mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="85c9c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="85c9c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="85c9c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="85c9c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="85c9c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="85c9c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="85c9c-107">Crear un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="85c9c-107">Create a new [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="85c9c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="85c9c-108">Prerequisites</span></span>
<span data-ttu-id="85c9c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="85c9c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="85c9c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="85c9c-111">Permission type</span></span>|<span data-ttu-id="85c9c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="85c9c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="85c9c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="85c9c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="85c9c-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="85c9c-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="85c9c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="85c9c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="85c9c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85c9c-116">Not supported.</span></span>|
|<span data-ttu-id="85c9c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="85c9c-117">Application</span></span>|<span data-ttu-id="85c9c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85c9c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="85c9c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="85c9c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/mobileThreatDefenseConnectors
```

## <a name="request-headers"></a><span data-ttu-id="85c9c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="85c9c-120">Request headers</span></span>
|<span data-ttu-id="85c9c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85c9c-121">Header</span></span>|<span data-ttu-id="85c9c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="85c9c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="85c9c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="85c9c-123">Authorization</span></span>|<span data-ttu-id="85c9c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="85c9c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="85c9c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="85c9c-125">Accept</span></span>|<span data-ttu-id="85c9c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="85c9c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="85c9c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="85c9c-127">Request body</span></span>
<span data-ttu-id="85c9c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="85c9c-128">In the request body, supply a JSON representation for the mobileThreatDefenseConnector object.</span></span>

<span data-ttu-id="85c9c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="85c9c-129">The following table shows the properties that are required when you create the mobileThreatDefenseConnector.</span></span>

|<span data-ttu-id="85c9c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="85c9c-130">Property</span></span>|<span data-ttu-id="85c9c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="85c9c-131">Type</span></span>|<span data-ttu-id="85c9c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c9c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="85c9c-133">id</span><span class="sxs-lookup"><span data-stu-id="85c9c-133">id</span></span>|<span data-ttu-id="85c9c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="85c9c-134">String</span></span>|<span data-ttu-id="85c9c-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="85c9c-135">Not yet documented</span></span>|
|<span data-ttu-id="85c9c-136">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="85c9c-136">lastHeartbeatDateTime</span></span>|<span data-ttu-id="85c9c-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="85c9c-137">DateTimeOffset</span></span>|<span data-ttu-id="85c9c-138">Fecha y hora del último latido recibido del Partner de sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="85c9c-138">DateTime of last Heartbeat recieved from the Data Sync Partner</span></span>|
|<span data-ttu-id="85c9c-139">partnerState</span><span class="sxs-lookup"><span data-stu-id="85c9c-139">partnerState</span></span>|[<span data-ttu-id="85c9c-140">mobileThreatPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="85c9c-140">mobileThreatPartnerTenantState</span></span>](../resources/intune-onboarding-mobilethreatpartnertenantstate.md)|<span data-ttu-id="85c9c-141">Estado de socio de sincronización de datos para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="85c9c-141">Data Sync Partner state for this account.</span></span> <span data-ttu-id="85c9c-142">Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="85c9c-142">Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="85c9c-143">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="85c9c-143">androidEnabled</span></span>|<span data-ttu-id="85c9c-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c9c-144">Boolean</span></span>|<span data-ttu-id="85c9c-145">Para Android, establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="85c9c-145">For Android, set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="85c9c-146">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="85c9c-146">iosEnabled</span></span>|<span data-ttu-id="85c9c-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c9c-147">Boolean</span></span>|<span data-ttu-id="85c9c-148">Para iOS, obtiene o establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="85c9c-148">For IOS, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="85c9c-149">windowsEnabled</span><span class="sxs-lookup"><span data-stu-id="85c9c-149">windowsEnabled</span></span>|<span data-ttu-id="85c9c-150">Booleano</span><span class="sxs-lookup"><span data-stu-id="85c9c-150">Boolean</span></span>|<span data-ttu-id="85c9c-151">Para Windows, obtener o establecer si se deben usar datos desde el asociado de sincronización de datos durante las evaluaciones de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="85c9c-151">For Windows, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="85c9c-152">macEnabled</span><span class="sxs-lookup"><span data-stu-id="85c9c-152">macEnabled</span></span>|<span data-ttu-id="85c9c-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="85c9c-153">Boolean</span></span>|<span data-ttu-id="85c9c-154">Para Mac, obtener o establecer si se deben usar datos desde el asociado de sincronización de datos durante las evaluaciones de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="85c9c-154">For Mac, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="85c9c-155">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="85c9c-155">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="85c9c-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c9c-156">Boolean</span></span>|<span data-ttu-id="85c9c-157">Para Android, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="85c9c-157">For Android, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="85c9c-158">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="85c9c-158">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="85c9c-159">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c9c-159">Boolean</span></span>|<span data-ttu-id="85c9c-160">Para iOS, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="85c9c-160">For IOS, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="85c9c-161">windowsDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="85c9c-161">windowsDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="85c9c-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="85c9c-162">Boolean</span></span>|<span data-ttu-id="85c9c-163">Para Windows, establecer si Intune debe recibir datos desde el asociado de sincronización de datos antes de marcar un dispositivo compatible con</span><span class="sxs-lookup"><span data-stu-id="85c9c-163">For Windows, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="85c9c-164">macDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="85c9c-164">macDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="85c9c-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="85c9c-165">Boolean</span></span>|<span data-ttu-id="85c9c-166">Para Mac, obtener o establecer si Intune debe recibir datos desde el asociado de sincronización de datos antes de marcar un dispositivo compatible con</span><span class="sxs-lookup"><span data-stu-id="85c9c-166">For Mac, get or set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="85c9c-167">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="85c9c-167">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="85c9c-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="85c9c-168">Boolean</span></span>|<span data-ttu-id="85c9c-169">Obtiene o establece si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="85c9c-169">Get or set whether to block devices on the enabled platforms that do not meet the minimum version requirements of the Data Sync Partner</span></span>|
|<span data-ttu-id="85c9c-170">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="85c9c-170">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="85c9c-171">Int32</span><span class="sxs-lookup"><span data-stu-id="85c9c-171">Int32</span></span>|<span data-ttu-id="85c9c-172">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="85c9c-172">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|
|<span data-ttu-id="85c9c-173">allowPartnerToCollectIOSApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="85c9c-173">allowPartnerToCollectIOSApplicationMetadata</span></span>|<span data-ttu-id="85c9c-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="85c9c-174">Boolean</span></span>|<span data-ttu-id="85c9c-175">Para los dispositivos IOS, permite que el Administrador de configuración si el socio de sincronización de datos también puede recopilar los metadatos sobre las aplicaciones instaladas desde Intune</span><span class="sxs-lookup"><span data-stu-id="85c9c-175">For IOS devices, allows the admin to configure whether the data sync partner may also collect metadata about installed applications from Intune</span></span>|



## <a name="response"></a><span data-ttu-id="85c9c-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85c9c-176">Response</span></span>
<span data-ttu-id="85c9c-177">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85c9c-177">If successful, this method returns a `201 Created` response code and a [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="85c9c-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85c9c-178">Example</span></span>
### <a name="request"></a><span data-ttu-id="85c9c-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="85c9c-179">Request</span></span>
<span data-ttu-id="85c9c-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85c9c-180">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/mobileThreatDefenseConnectors
Content-type: application/json
Content-length: 622

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "windowsEnabled": true,
  "macEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "windowsDeviceBlockedOnMissingPartnerData": true,
  "macDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6,
  "allowPartnerToCollectIOSApplicationMetadata": true
}
```

### <a name="response"></a><span data-ttu-id="85c9c-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85c9c-181">Response</span></span>
<span data-ttu-id="85c9c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="85c9c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 671

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "e4bede14-de14-e4be-14de-bee414debee4",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "windowsEnabled": true,
  "macEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "windowsDeviceBlockedOnMissingPartnerData": true,
  "macDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6,
  "allowPartnerToCollectIOSApplicationMetadata": true
}
```





