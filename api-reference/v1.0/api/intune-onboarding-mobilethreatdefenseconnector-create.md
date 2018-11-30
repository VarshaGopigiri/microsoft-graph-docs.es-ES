---
title: Crear mobileThreatDefenseConnector
description: Cree un objeto mobileThreatDefenseConnector.
ms.openlocfilehash: f7ed9c8175eec263b8b9b08d541cfedc7edd7d59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029212"
---
# <a name="create-mobilethreatdefenseconnector"></a><span data-ttu-id="5474d-103">Crear mobileThreatDefenseConnector</span><span class="sxs-lookup"><span data-stu-id="5474d-103">Create mobileThreatDefenseConnector</span></span>

> <span data-ttu-id="5474d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5474d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5474d-105">Crear un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="5474d-105">Create a new [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5474d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5474d-106">Prerequisites</span></span>
<span data-ttu-id="5474d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5474d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5474d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5474d-109">Permission type</span></span>|<span data-ttu-id="5474d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5474d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5474d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5474d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5474d-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5474d-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="5474d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5474d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5474d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5474d-114">Not supported.</span></span>|
|<span data-ttu-id="5474d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5474d-115">Application</span></span>|<span data-ttu-id="5474d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5474d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5474d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5474d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/mobileThreatDefenseConnectors
```

## <a name="request-headers"></a><span data-ttu-id="5474d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5474d-118">Request headers</span></span>
|<span data-ttu-id="5474d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5474d-119">Header</span></span>|<span data-ttu-id="5474d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5474d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5474d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="5474d-121">Authorization</span></span>|<span data-ttu-id="5474d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5474d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5474d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5474d-123">Accept</span></span>|<span data-ttu-id="5474d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5474d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5474d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5474d-125">Request body</span></span>
<span data-ttu-id="5474d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="5474d-126">In the request body, supply a JSON representation for the mobileThreatDefenseConnector object.</span></span>

<span data-ttu-id="5474d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileThreatDefenseConnector.</span><span class="sxs-lookup"><span data-stu-id="5474d-127">The following table shows the properties that are required when you create the mobileThreatDefenseConnector.</span></span>

|<span data-ttu-id="5474d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5474d-128">Property</span></span>|<span data-ttu-id="5474d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5474d-129">Type</span></span>|<span data-ttu-id="5474d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5474d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5474d-131">id</span><span class="sxs-lookup"><span data-stu-id="5474d-131">id</span></span>|<span data-ttu-id="5474d-132">String</span><span class="sxs-lookup"><span data-stu-id="5474d-132">String</span></span>|<span data-ttu-id="5474d-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5474d-133">Not yet documented</span></span>|
|<span data-ttu-id="5474d-134">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="5474d-134">lastHeartbeatDateTime</span></span>|<span data-ttu-id="5474d-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5474d-135">DateTimeOffset</span></span>|<span data-ttu-id="5474d-136">Fecha y hora del último latido recibido del Partner de sincronización de datos</span><span class="sxs-lookup"><span data-stu-id="5474d-136">DateTime of last Heartbeat recieved from the Data Sync Partner</span></span>|
|<span data-ttu-id="5474d-137">partnerState</span><span class="sxs-lookup"><span data-stu-id="5474d-137">partnerState</span></span>|[<span data-ttu-id="5474d-138">mobileThreatPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="5474d-138">mobileThreatPartnerTenantState</span></span>](../resources/intune-onboarding-mobilethreatpartnertenantstate.md)|<span data-ttu-id="5474d-139">Estado de socio de sincronización de datos para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="5474d-139">Data Sync Partner state for this account.</span></span> <span data-ttu-id="5474d-140">Los valores posibles son: `unavailable`, `available`, `enabled` y `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="5474d-140">Possible values are: `unavailable`, `available`, `enabled`, `unresponsive`.</span></span>|
|<span data-ttu-id="5474d-141">androidEnabled</span><span class="sxs-lookup"><span data-stu-id="5474d-141">androidEnabled</span></span>|<span data-ttu-id="5474d-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="5474d-142">Boolean</span></span>|<span data-ttu-id="5474d-143">Para Android, establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="5474d-143">For Android, set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="5474d-144">iosEnabled</span><span class="sxs-lookup"><span data-stu-id="5474d-144">iosEnabled</span></span>|<span data-ttu-id="5474d-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="5474d-145">Boolean</span></span>|<span data-ttu-id="5474d-146">Para iOS, obtiene o establece si se deberían utilizar los datos del partner de sincronización de datos durante las evaluaciones de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="5474d-146">For IOS, get or set whether data from the data sync partner should be used during compliance evaluations</span></span>|
|<span data-ttu-id="5474d-147">androidDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="5474d-147">androidDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="5474d-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="5474d-148">Boolean</span></span>|<span data-ttu-id="5474d-149">Para Android, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="5474d-149">For Android, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="5474d-150">iosDeviceBlockedOnMissingPartnerData</span><span class="sxs-lookup"><span data-stu-id="5474d-150">iosDeviceBlockedOnMissingPartnerData</span></span>|<span data-ttu-id="5474d-151">Boolean</span><span class="sxs-lookup"><span data-stu-id="5474d-151">Boolean</span></span>|<span data-ttu-id="5474d-152">Para iOS, establece si Intune debe recibir datos del partner de sincronización de datos antes de marcar un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="5474d-152">For IOS, set whether Intune must receive data from the data sync partner prior to marking a device compliant</span></span>|
|<span data-ttu-id="5474d-153">partnerUnsupportedOsVersionBlocked</span><span class="sxs-lookup"><span data-stu-id="5474d-153">partnerUnsupportedOsVersionBlocked</span></span>|<span data-ttu-id="5474d-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="5474d-154">Boolean</span></span>|<span data-ttu-id="5474d-155">Obtiene o establece si se deben bloquear los dispositivos de las plataformas habilitadas que no cumplan los requisitos de versión mínima.</span><span class="sxs-lookup"><span data-stu-id="5474d-155">Get or set whether to block devices on the enabled platforms that do not meet the minimum version requirements of the Data Sync Partner</span></span>|
|<span data-ttu-id="5474d-156">partnerUnresponsivenessThresholdInDays</span><span class="sxs-lookup"><span data-stu-id="5474d-156">partnerUnresponsivenessThresholdInDays</span></span>|<span data-ttu-id="5474d-157">Int32</span><span class="sxs-lookup"><span data-stu-id="5474d-157">Int32</span></span>|<span data-ttu-id="5474d-158">Obtener o definir los días de tolerancia por espacio empresarial para la falta de respuesta de esta integración de partner.</span><span class="sxs-lookup"><span data-stu-id="5474d-158">Get or Set days the per tenant tolerance to unresponsiveness for this partner integration</span></span>|



## <a name="response"></a><span data-ttu-id="5474d-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5474d-159">Response</span></span>
<span data-ttu-id="5474d-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5474d-160">If successful, this method returns a `201 Created` response code and a [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5474d-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5474d-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="5474d-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5474d-162">Request</span></span>
<span data-ttu-id="5474d-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5474d-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/mobileThreatDefenseConnectors
Content-type: application/json
Content-length: 414

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```

### <a name="response"></a><span data-ttu-id="5474d-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5474d-164">Response</span></span>
<span data-ttu-id="5474d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5474d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 463

{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "e4bede14-de14-e4be-14de-bee414debee4",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "available",
  "androidEnabled": true,
  "iosEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 6
}
```



