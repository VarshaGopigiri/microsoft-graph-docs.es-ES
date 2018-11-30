---
title: Actualizar deviceManagementPartner
description: Actualice las propiedades de un objeto deviceManagementPartner.
ms.openlocfilehash: e47cc1ac3b219af0e1d9b20103fc1ca37410478a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029202"
---
# <a name="update-devicemanagementpartner"></a><span data-ttu-id="c5abb-103">Actualizar deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="c5abb-103">Update deviceManagementPartner</span></span>

> <span data-ttu-id="c5abb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c5abb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c5abb-105">Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="c5abb-105">Update the properties of a [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c5abb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c5abb-106">Prerequisites</span></span>
<span data-ttu-id="c5abb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5abb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c5abb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c5abb-109">Permission type</span></span>|<span data-ttu-id="c5abb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c5abb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c5abb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c5abb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c5abb-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c5abb-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="c5abb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c5abb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c5abb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5abb-114">Not supported.</span></span>|
|<span data-ttu-id="c5abb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c5abb-115">Application</span></span>|<span data-ttu-id="c5abb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5abb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c5abb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5abb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="c5abb-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5abb-118">Request headers</span></span>
|<span data-ttu-id="c5abb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5abb-119">Header</span></span>|<span data-ttu-id="c5abb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c5abb-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c5abb-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5abb-121">Authorization</span></span>|<span data-ttu-id="c5abb-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c5abb-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c5abb-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c5abb-123">Accept</span></span>|<span data-ttu-id="c5abb-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c5abb-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c5abb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5abb-125">Request body</span></span>
<span data-ttu-id="c5abb-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="c5abb-126">In the request body, supply a JSON representation for the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>

<span data-ttu-id="c5abb-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="c5abb-127">The following table shows the properties that are required when you create the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span></span>

|<span data-ttu-id="c5abb-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c5abb-128">Property</span></span>|<span data-ttu-id="c5abb-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5abb-129">Type</span></span>|<span data-ttu-id="c5abb-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5abb-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c5abb-131">id</span><span class="sxs-lookup"><span data-stu-id="c5abb-131">id</span></span>|<span data-ttu-id="c5abb-132">String</span><span class="sxs-lookup"><span data-stu-id="c5abb-132">String</span></span>|<span data-ttu-id="c5abb-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c5abb-133">Not yet documented</span></span>|
|<span data-ttu-id="c5abb-134">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="c5abb-134">lastHeartbeatDateTime</span></span>|<span data-ttu-id="c5abb-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c5abb-135">DateTimeOffset</span></span>|<span data-ttu-id="c5abb-136">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="c5abb-136">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="c5abb-137">partnerState</span><span class="sxs-lookup"><span data-stu-id="c5abb-137">partnerState</span></span>|[<span data-ttu-id="c5abb-138">deviceManagementPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="c5abb-138">deviceManagementPartnerTenantState</span></span>](../resources/intune-onboarding-devicemanagementpartnertenantstate.md)|<span data-ttu-id="c5abb-139">Estado de socio de este inquilino.</span><span class="sxs-lookup"><span data-stu-id="c5abb-139">Partner state of this tenant.</span></span> <span data-ttu-id="c5abb-140">Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="c5abb-140">Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="c5abb-141">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="c5abb-141">partnerAppType</span></span>|[<span data-ttu-id="c5abb-142">deviceManagementPartnerAppType</span><span class="sxs-lookup"><span data-stu-id="c5abb-142">deviceManagementPartnerAppType</span></span>](../resources/intune-onboarding-devicemanagementpartnerapptype.md)|<span data-ttu-id="c5abb-143">Tipo de aplicación de socio.</span><span class="sxs-lookup"><span data-stu-id="c5abb-143">Partner App type.</span></span> <span data-ttu-id="c5abb-144">Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="c5abb-144">Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="c5abb-145">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="c5abb-145">singleTenantAppId</span></span>|<span data-ttu-id="c5abb-146">String</span><span class="sxs-lookup"><span data-stu-id="c5abb-146">String</span></span>|<span data-ttu-id="c5abb-147">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="c5abb-147">Partner Single tenant App id</span></span>|
|<span data-ttu-id="c5abb-148">displayName</span><span class="sxs-lookup"><span data-stu-id="c5abb-148">displayName</span></span>|<span data-ttu-id="c5abb-149">String</span><span class="sxs-lookup"><span data-stu-id="c5abb-149">String</span></span>|<span data-ttu-id="c5abb-150">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="c5abb-150">Partner display name</span></span>|
|<span data-ttu-id="c5abb-151">isConfigured</span><span class="sxs-lookup"><span data-stu-id="c5abb-151">isConfigured</span></span>|<span data-ttu-id="c5abb-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="c5abb-152">Boolean</span></span>|<span data-ttu-id="c5abb-153">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="c5abb-153">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="c5abb-154">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="c5abb-154">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="c5abb-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c5abb-155">DateTimeOffset</span></span>|<span data-ttu-id="c5abb-156">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="c5abb-156">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="c5abb-157">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="c5abb-157">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="c5abb-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c5abb-158">DateTimeOffset</span></span>|<span data-ttu-id="c5abb-159">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="c5abb-159">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="c5abb-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5abb-160">Response</span></span>
<span data-ttu-id="c5abb-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5abb-161">If successful, this method returns a `200 OK` response code and an updated [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c5abb-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5abb-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="c5abb-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5abb-163">Request</span></span>
<span data-ttu-id="c5abb-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5abb-164">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
Content-type: application/json
Content-length: 502

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```

### <a name="response"></a><span data-ttu-id="c5abb-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5abb-165">Response</span></span>
<span data-ttu-id="c5abb-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5abb-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 551

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "d21e377a-377a-d21e-7a37-1ed27a371ed2",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```



