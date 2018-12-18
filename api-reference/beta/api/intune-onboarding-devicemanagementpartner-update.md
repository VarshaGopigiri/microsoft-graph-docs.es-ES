---
title: Actualizar deviceManagementPartner
description: Actualice las propiedades de un objeto deviceManagementPartner.
author: tfitzmac
ms.openlocfilehash: 47aba10ebe744d4f8211081e5c947df4d61599ed
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356325"
---
# <a name="update-devicemanagementpartner"></a><span data-ttu-id="07720-103">Actualizar deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="07720-103">Update deviceManagementPartner</span></span>

> <span data-ttu-id="07720-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="07720-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="07720-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="07720-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="07720-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="07720-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="07720-107">Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="07720-107">Update the properties of a [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="07720-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="07720-108">Prerequisites</span></span>
<span data-ttu-id="07720-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07720-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07720-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07720-111">Permission type</span></span>|<span data-ttu-id="07720-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07720-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="07720-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07720-113">Delegated (work or school account)</span></span>|<span data-ttu-id="07720-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="07720-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="07720-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07720-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="07720-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07720-116">Not supported.</span></span>|
|<span data-ttu-id="07720-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07720-117">Application</span></span>|<span data-ttu-id="07720-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07720-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="07720-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07720-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="07720-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07720-120">Request headers</span></span>
|<span data-ttu-id="07720-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07720-121">Header</span></span>|<span data-ttu-id="07720-122">Valor</span><span class="sxs-lookup"><span data-stu-id="07720-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="07720-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="07720-123">Authorization</span></span>|<span data-ttu-id="07720-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="07720-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="07720-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="07720-125">Accept</span></span>|<span data-ttu-id="07720-126">application/json</span><span class="sxs-lookup"><span data-stu-id="07720-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="07720-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="07720-127">Request body</span></span>
<span data-ttu-id="07720-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="07720-128">In the request body, supply a JSON representation for the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>

<span data-ttu-id="07720-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="07720-129">The following table shows the properties that are required when you create the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span></span>

|<span data-ttu-id="07720-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="07720-130">Property</span></span>|<span data-ttu-id="07720-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="07720-131">Type</span></span>|<span data-ttu-id="07720-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="07720-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="07720-133">id</span><span class="sxs-lookup"><span data-stu-id="07720-133">id</span></span>|<span data-ttu-id="07720-134">String</span><span class="sxs-lookup"><span data-stu-id="07720-134">String</span></span>|<span data-ttu-id="07720-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="07720-135">Not yet documented</span></span>|
|<span data-ttu-id="07720-136">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="07720-136">lastHeartbeatDateTime</span></span>|<span data-ttu-id="07720-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="07720-137">DateTimeOffset</span></span>|<span data-ttu-id="07720-138">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="07720-138">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="07720-139">partnerState</span><span class="sxs-lookup"><span data-stu-id="07720-139">partnerState</span></span>|[<span data-ttu-id="07720-140">deviceManagementPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="07720-140">deviceManagementPartnerTenantState</span></span>](../resources/intune-onboarding-devicemanagementpartnertenantstate.md)|<span data-ttu-id="07720-141">Estado de socio de este inquilino.</span><span class="sxs-lookup"><span data-stu-id="07720-141">Partner state of this tenant.</span></span> <span data-ttu-id="07720-142">Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="07720-142">Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="07720-143">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="07720-143">partnerAppType</span></span>|[<span data-ttu-id="07720-144">deviceManagementPartnerAppType</span><span class="sxs-lookup"><span data-stu-id="07720-144">deviceManagementPartnerAppType</span></span>](../resources/intune-onboarding-devicemanagementpartnerapptype.md)|<span data-ttu-id="07720-145">Tipo de aplicación de socio.</span><span class="sxs-lookup"><span data-stu-id="07720-145">Partner App type.</span></span> <span data-ttu-id="07720-146">Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="07720-146">Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="07720-147">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="07720-147">singleTenantAppId</span></span>|<span data-ttu-id="07720-148">String</span><span class="sxs-lookup"><span data-stu-id="07720-148">String</span></span>|<span data-ttu-id="07720-149">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="07720-149">Partner Single tenant App id</span></span>|
|<span data-ttu-id="07720-150">displayName</span><span class="sxs-lookup"><span data-stu-id="07720-150">displayName</span></span>|<span data-ttu-id="07720-151">String</span><span class="sxs-lookup"><span data-stu-id="07720-151">String</span></span>|<span data-ttu-id="07720-152">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="07720-152">Partner display name</span></span>|
|<span data-ttu-id="07720-153">isConfigured</span><span class="sxs-lookup"><span data-stu-id="07720-153">isConfigured</span></span>|<span data-ttu-id="07720-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="07720-154">Boolean</span></span>|<span data-ttu-id="07720-155">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="07720-155">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="07720-156">whenPartnerDevicesWillBeRemoved</span><span class="sxs-lookup"><span data-stu-id="07720-156">whenPartnerDevicesWillBeRemoved</span></span>|<span data-ttu-id="07720-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="07720-157">DateTimeOffset</span></span>|<span data-ttu-id="07720-158">Fecha y hora en UTC cuando se quitará PartnerDevices.</span><span class="sxs-lookup"><span data-stu-id="07720-158">DateTime in UTC when PartnerDevices will be removed.</span></span> <span data-ttu-id="07720-159">Esto se convertirá en obsoleta pronto.</span><span class="sxs-lookup"><span data-stu-id="07720-159">This will become obselete soon.</span></span>|
|<span data-ttu-id="07720-160">whenPartnerDevicesWillBeMarkedAsNonCompliant</span><span class="sxs-lookup"><span data-stu-id="07720-160">whenPartnerDevicesWillBeMarkedAsNonCompliant</span></span>|<span data-ttu-id="07720-161">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="07720-161">DateTimeOffset</span></span>|<span data-ttu-id="07720-162">Fecha y hora en UTC cuando PartnerDevices se marcarán como no compatible.</span><span class="sxs-lookup"><span data-stu-id="07720-162">DateTime in UTC when PartnerDevices will be marked as NonCompliant.</span></span> <span data-ttu-id="07720-163">Esto se convertirá en obsoleta pronto.</span><span class="sxs-lookup"><span data-stu-id="07720-163">This will become obselete soon.</span></span>|
|<span data-ttu-id="07720-164">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="07720-164">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="07720-165">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="07720-165">DateTimeOffset</span></span>|<span data-ttu-id="07720-166">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="07720-166">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="07720-167">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="07720-167">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="07720-168">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="07720-168">DateTimeOffset</span></span>|<span data-ttu-id="07720-169">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="07720-169">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="07720-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07720-170">Response</span></span>
<span data-ttu-id="07720-171">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07720-171">If successful, this method returns a `200 OK` response code and an updated [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="07720-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07720-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="07720-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07720-173">Request</span></span>
<span data-ttu-id="07720-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07720-174">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
Content-type: application/json
Content-length: 602

{
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemoved": "2017-01-01T00:00:34.890321-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliant": "2017-01-01T00:02:38.9066046-08:00",
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```

### <a name="response"></a><span data-ttu-id="07720-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07720-175">Response</span></span>
<span data-ttu-id="07720-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="07720-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 713

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "d21e377a-377a-d21e-7a37-1ed27a371ed2",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemoved": "2017-01-01T00:00:34.890321-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliant": "2017-01-01T00:02:38.9066046-08:00",
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```





