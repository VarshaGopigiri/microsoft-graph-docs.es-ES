---
title: Actualizar mobileThreatDefenseConnector
description: Actualice las propiedades de un objeto mobileThreatDefenseConnector.
ms.openlocfilehash: 0a7518c2c751c55a89d02c3d67f87d7a272f895d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088831"
---
# <a name="update-mobilethreatdefenseconnector"></a><span data-ttu-id="def7e-103">Actualizar mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="def7e-103">Update mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="def7e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="def7e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="def7e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="def7e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="def7e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="def7e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="def7e-107">Actualice las propiedades de un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="def7e-107">Update the properties of a [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="def7e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="def7e-108">Prerequisites</span></span>
<span data-ttu-id="def7e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="def7e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="def7e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="def7e-111">Permission type</span></span>|<span data-ttu-id="def7e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="def7e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="def7e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="def7e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="def7e-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="def7e-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="def7e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="def7e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="def7e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="def7e-116">Not supported.</span></span>|
|<span data-ttu-id="def7e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="def7e-117">Application</span></span>|<span data-ttu-id="def7e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="def7e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="def7e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="def7e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="def7e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="def7e-120">Request headers</span></span>
|<span data-ttu-id="def7e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="def7e-121">Header</span></span>|<span data-ttu-id="def7e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="def7e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="def7e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="def7e-123">Authorization</span></span>|<span data-ttu-id="def7e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="def7e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="def7e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="def7e-125">Accept</span></span>|<span data-ttu-id="def7e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="def7e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="def7e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="def7e-127">Request body</span></span>
<span data-ttu-id="def7e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="def7e-128">In the request body, supply a JSON representation for the [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object.</span></span>

<span data-ttu-id="def7e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="def7e-129">The following table shows the properties that are required when you create the [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span></span>

|<span data-ttu-id="def7e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="def7e-130">Property</span></span>|<span data-ttu-id="def7e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="def7e-131">Type</span></span>|<span data-ttu-id="def7e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="def7e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="def7e-133">id</span><span class="sxs-lookup"><span data-stu-id="def7e-133">id</span></span>|<span data-ttu-id="def7e-134">String</span><span class="sxs-lookup"><span data-stu-id="def7e-134">String</span></span>|<span data-ttu-id="def7e-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="def7e-135">Not yet documented</span></span>|
|<span data-ttu-id="def7e-136">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="def7e-136">lastHeartbeatDateTime</span></span>|<span data-ttu-id="def7e-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="def7e-137">DateTimeOffset</span></span>|<span data-ttu-id="def7e-138">Fecha y hora del último latido recibido del Partner de sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="def7e-138">DateTime of last Heartbeat recieved from the Data Sync Partner</span></span>|
|<span data-ttu-id="def7e-139">partnerState</span><span class="sxs-lookup"><span data-stu-id="def7e-139">partnerState</span></span>|[<span data-ttu-id="def7e-140">mobileThreatPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="def7e-140">mobileThreatPartnerTenantState</span></span>](../resources/intune-onboarding-mobilethreatpartnertenantstate.md)|<span data-ttu-id="def7e-141">Estado de socio de sincronización de datos para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="def7e-141">Data Sync Partner state for this account.</span></span> <span data-ttu-id="def7e-142">Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="def7e-142">Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="def7e-143">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="def7e-143">androidEnabled</span></span>|<span data-ttu-id="def7e-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="def7e-144">Boolean</span></span>|<span data-ttu-id="def7e-145">Para Android, establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="def7e-145">For Android, set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="def7e-146">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="def7e-146">iosEnabled</span></span>|<span data-ttu-id="def7e-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="def7e-147">Boolean</span></span>|<span data-ttu-id="def7e-148">Para iOS, obtiene o establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="def7e-148">For IOS, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="def7e-149">windowsEnabled</span><span class="sxs-lookup"><span data-stu-id="def7e-149">windowsEnabled</span></span>|<span data-ttu-id="def7e-150">Booleano</span><span class="sxs-lookup"><span data-stu-id="def7e-150">Boolean</span></span>|<span data-ttu-id="def7e-151">Para Windows, obtener o establecer si se deben usar datos desde el asociado de sincronización de datos durante las evaluaciones de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="def7e-151">For Windows, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="def7e-152">macEnabled</span><span class="sxs-lookup"><span data-stu-id="def7e-152">macEnabled</span></span>|<span data-ttu-id="def7e-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="def7e-153">Boolean</span></span>|<span data-ttu-id="def7e-154">Para Mac, obtener o establecer si se deben usar datos desde el asociado de sincronización de datos durante las evaluaciones de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="def7e-154">For Mac, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="def7e-155">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="def7e-155">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="def7e-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="def7e-156">Boolean</span></span>|<span data-ttu-id="def7e-157">Para Android, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="def7e-157">For Android, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="def7e-158">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="def7e-158">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="def7e-159">Boolean</span><span class="sxs-lookup"><span data-stu-id="def7e-159">Boolean</span></span>|<span data-ttu-id="def7e-160">Para iOS, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="def7e-160">For IOS, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="def7e-161">windowsDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="def7e-161">windowsDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="def7e-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="def7e-162">Boolean</span></span>|<span data-ttu-id="def7e-163">Para Windows, establecer si Intune debe recibir datos desde el asociado de sincronización de datos antes de marcar un dispositivo compatible con</span><span class="sxs-lookup"><span data-stu-id="def7e-163">For Windows, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="def7e-164">macDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="def7e-164">macDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="def7e-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="def7e-165">Boolean</span></span>|<span data-ttu-id="def7e-166">Para Mac, obtener o establecer si Intune debe recibir datos desde el asociado de sincronización de datos antes de marcar un dispositivo compatible con</span><span class="sxs-lookup"><span data-stu-id="def7e-166">For Mac, get or set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="def7e-167">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="def7e-167">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="def7e-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="def7e-168">Boolean</span></span>|<span data-ttu-id="def7e-169">Obtiene o establece si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="def7e-169">Get or set whether to block devices on the enabled platforms that do not meet the minimum version requirements of the Data Sync Partner</span></span>|
|<span data-ttu-id="def7e-170">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="def7e-170">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="def7e-171">Int32</span><span class="sxs-lookup"><span data-stu-id="def7e-171">Int32</span></span>|<span data-ttu-id="def7e-172">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="def7e-172">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|
|<span data-ttu-id="def7e-173">allowPartnerToCollectIOSApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="def7e-173">allowPartnerToCollectIOSApplicationMetadata</span></span>|<span data-ttu-id="def7e-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="def7e-174">Boolean</span></span>|<span data-ttu-id="def7e-175">Para los dispositivos IOS, permite que el Administrador de configuración si el socio de sincronización de datos también puede recopilar los metadatos sobre las aplicaciones instaladas desde Intune</span><span class="sxs-lookup"><span data-stu-id="def7e-175">For IOS devices, allows the admin to configure whether the data sync partner may also collect metadata about installed applications from Intune</span></span>|



## <a name="response"></a><span data-ttu-id="def7e-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="def7e-176">Response</span></span>
<span data-ttu-id="def7e-177">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="def7e-177">If successful, this method returns a `200 OK` response code and an updated [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="def7e-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="def7e-178">Example</span></span>
### <a name="request"></a><span data-ttu-id="def7e-179">Solicitud</span><span class="sxs-lookup"><span data-stu-id="def7e-179">Request</span></span>
<span data-ttu-id="def7e-180">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="def7e-180">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/mobileThreatDefenseConnectors/{mobileThreatDefenseConnectorId}
Content-type: application/json
Content-length: 555

{
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

### <a name="response"></a><span data-ttu-id="def7e-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="def7e-181">Response</span></span>
<span data-ttu-id="def7e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="def7e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




