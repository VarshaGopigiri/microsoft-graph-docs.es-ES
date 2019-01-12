---
title: Crear deviceManagementPartner
description: Cree un objeto deviceManagementPartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b9ff6eab5bf04277d89616765fb14855d047450c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991087"
---
# <a name="create-devicemanagementpartner"></a><span data-ttu-id="5ca55-103">Crear deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="5ca55-103">Create deviceManagementPartner</span></span>

> <span data-ttu-id="5ca55-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ca55-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ca55-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ca55-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5ca55-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5ca55-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5ca55-107">Cree un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="5ca55-107">Create a new [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5ca55-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5ca55-108">Prerequisites</span></span>
<span data-ttu-id="5ca55-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5ca55-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5ca55-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5ca55-111">Permission type</span></span>|<span data-ttu-id="5ca55-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5ca55-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5ca55-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5ca55-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5ca55-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ca55-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="5ca55-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5ca55-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5ca55-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5ca55-116">Not supported.</span></span>|
|<span data-ttu-id="5ca55-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5ca55-117">Application</span></span>|<span data-ttu-id="5ca55-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5ca55-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5ca55-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5ca55-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementPartners
```

## <a name="request-headers"></a><span data-ttu-id="5ca55-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5ca55-120">Request headers</span></span>
|<span data-ttu-id="5ca55-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ca55-121">Header</span></span>|<span data-ttu-id="5ca55-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5ca55-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5ca55-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5ca55-123">Authorization</span></span>|<span data-ttu-id="5ca55-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5ca55-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5ca55-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5ca55-125">Accept</span></span>|<span data-ttu-id="5ca55-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5ca55-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5ca55-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5ca55-127">Request body</span></span>
<span data-ttu-id="5ca55-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="5ca55-128">In the request body, supply a JSON representation for the deviceManagementPartner object.</span></span>

<span data-ttu-id="5ca55-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementPartner.</span><span class="sxs-lookup"><span data-stu-id="5ca55-129">The following table shows the properties that are required when you create the deviceManagementPartner.</span></span>

|<span data-ttu-id="5ca55-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ca55-130">Property</span></span>|<span data-ttu-id="5ca55-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ca55-131">Type</span></span>|<span data-ttu-id="5ca55-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ca55-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5ca55-133">id</span><span class="sxs-lookup"><span data-stu-id="5ca55-133">id</span></span>|<span data-ttu-id="5ca55-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5ca55-134">String</span></span>|<span data-ttu-id="5ca55-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5ca55-135">Not yet documented</span></span>|
|<span data-ttu-id="5ca55-136">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="5ca55-136">lastHeartbeatDateTime</span></span>|<span data-ttu-id="5ca55-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ca55-137">DateTimeOffset</span></span>|<span data-ttu-id="5ca55-138">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="5ca55-138">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="5ca55-139">partnerState</span><span class="sxs-lookup"><span data-stu-id="5ca55-139">partnerState</span></span>|[<span data-ttu-id="5ca55-140">deviceManagementPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="5ca55-140">deviceManagementPartnerTenantState</span></span>](../resources/intune-onboarding-devicemanagementpartnertenantstate.md)|<span data-ttu-id="5ca55-141">Estado de socio de este inquilino.</span><span class="sxs-lookup"><span data-stu-id="5ca55-141">Partner state of this tenant.</span></span> <span data-ttu-id="5ca55-142">Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="5ca55-142">Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="5ca55-143">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="5ca55-143">partnerAppType</span></span>|[<span data-ttu-id="5ca55-144">deviceManagementPartnerAppType</span><span class="sxs-lookup"><span data-stu-id="5ca55-144">deviceManagementPartnerAppType</span></span>](../resources/intune-onboarding-devicemanagementpartnerapptype.md)|<span data-ttu-id="5ca55-145">Tipo de aplicación de socio.</span><span class="sxs-lookup"><span data-stu-id="5ca55-145">Partner App type.</span></span> <span data-ttu-id="5ca55-146">Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="5ca55-146">Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="5ca55-147">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="5ca55-147">singleTenantAppId</span></span>|<span data-ttu-id="5ca55-148">String</span><span class="sxs-lookup"><span data-stu-id="5ca55-148">String</span></span>|<span data-ttu-id="5ca55-149">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="5ca55-149">Partner Single tenant App id</span></span>|
|<span data-ttu-id="5ca55-150">displayName</span><span class="sxs-lookup"><span data-stu-id="5ca55-150">displayName</span></span>|<span data-ttu-id="5ca55-151">String</span><span class="sxs-lookup"><span data-stu-id="5ca55-151">String</span></span>|<span data-ttu-id="5ca55-152">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="5ca55-152">Partner display name</span></span>|
|<span data-ttu-id="5ca55-153">isConfigured</span><span class="sxs-lookup"><span data-stu-id="5ca55-153">isConfigured</span></span>|<span data-ttu-id="5ca55-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="5ca55-154">Boolean</span></span>|<span data-ttu-id="5ca55-155">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="5ca55-155">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="5ca55-156">whenPartnerDevicesWillBeRemoved</span><span class="sxs-lookup"><span data-stu-id="5ca55-156">whenPartnerDevicesWillBeRemoved</span></span>|<span data-ttu-id="5ca55-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ca55-157">DateTimeOffset</span></span>|<span data-ttu-id="5ca55-158">Fecha y hora en UTC cuando se quitará PartnerDevices.</span><span class="sxs-lookup"><span data-stu-id="5ca55-158">DateTime in UTC when PartnerDevices will be removed.</span></span> <span data-ttu-id="5ca55-159">Esto se convertirá en obsoleta pronto.</span><span class="sxs-lookup"><span data-stu-id="5ca55-159">This will become obselete soon.</span></span>|
|<span data-ttu-id="5ca55-160">whenPartnerDevicesWillBeMarkedAsNonCompliant</span><span class="sxs-lookup"><span data-stu-id="5ca55-160">whenPartnerDevicesWillBeMarkedAsNonCompliant</span></span>|<span data-ttu-id="5ca55-161">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ca55-161">DateTimeOffset</span></span>|<span data-ttu-id="5ca55-162">Fecha y hora en UTC cuando PartnerDevices se marcarán como no compatible.</span><span class="sxs-lookup"><span data-stu-id="5ca55-162">DateTime in UTC when PartnerDevices will be marked as NonCompliant.</span></span> <span data-ttu-id="5ca55-163">Esto se convertirá en obsoleta pronto.</span><span class="sxs-lookup"><span data-stu-id="5ca55-163">This will become obselete soon.</span></span>|
|<span data-ttu-id="5ca55-164">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="5ca55-164">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="5ca55-165">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ca55-165">DateTimeOffset</span></span>|<span data-ttu-id="5ca55-166">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="5ca55-166">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="5ca55-167">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="5ca55-167">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="5ca55-168">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5ca55-168">DateTimeOffset</span></span>|<span data-ttu-id="5ca55-169">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="5ca55-169">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="5ca55-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ca55-170">Response</span></span>
<span data-ttu-id="5ca55-171">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ca55-171">If successful, this method returns a `201 Created` response code and a [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5ca55-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ca55-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="5ca55-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ca55-173">Request</span></span>
<span data-ttu-id="5ca55-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5ca55-174">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceManagementPartners
Content-type: application/json
Content-length: 664

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
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

### <a name="response"></a><span data-ttu-id="5ca55-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ca55-175">Response</span></span>
<span data-ttu-id="5ca55-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5ca55-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





