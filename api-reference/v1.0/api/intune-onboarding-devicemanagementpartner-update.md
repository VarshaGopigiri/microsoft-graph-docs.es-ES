---
title: Actualizar deviceManagementPartner
description: Actualice las propiedades de un objeto deviceManagementPartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 068a0ffb3c0411a238a803f3876874f8902e3b35
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981864"
---
# <a name="update-devicemanagementpartner"></a><span data-ttu-id="f223c-103">Actualizar deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f223c-103">Update deviceManagementPartner</span></span>

> <span data-ttu-id="f223c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f223c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f223c-105">Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="f223c-105">Update the properties of a [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f223c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f223c-106">Prerequisites</span></span>
<span data-ttu-id="f223c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f223c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f223c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f223c-109">Permission type</span></span>|<span data-ttu-id="f223c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f223c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f223c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f223c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f223c-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f223c-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f223c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f223c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f223c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f223c-114">Not supported.</span></span>|
|<span data-ttu-id="f223c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f223c-115">Application</span></span>|<span data-ttu-id="f223c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f223c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f223c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f223c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="f223c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f223c-118">Request headers</span></span>
|<span data-ttu-id="f223c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f223c-119">Header</span></span>|<span data-ttu-id="f223c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f223c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f223c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f223c-121">Authorization</span></span>|<span data-ttu-id="f223c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f223c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f223c-123">Accept</span><span class="sxs-lookup"><span data-stu-id="f223c-123">Accept</span></span>|<span data-ttu-id="f223c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f223c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f223c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f223c-125">Request body</span></span>
<span data-ttu-id="f223c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="f223c-126">In the request body, supply a JSON representation for the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>

<span data-ttu-id="f223c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="f223c-127">The following table shows the properties that are required when you create the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span></span>

|<span data-ttu-id="f223c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f223c-128">Property</span></span>|<span data-ttu-id="f223c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f223c-129">Type</span></span>|<span data-ttu-id="f223c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f223c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f223c-131">id</span><span class="sxs-lookup"><span data-stu-id="f223c-131">id</span></span>|<span data-ttu-id="f223c-132">String</span><span class="sxs-lookup"><span data-stu-id="f223c-132">String</span></span>|<span data-ttu-id="f223c-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f223c-133">Not yet documented</span></span>|
|<span data-ttu-id="f223c-134">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="f223c-134">lastHeartbeatDateTime</span></span>|<span data-ttu-id="f223c-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f223c-135">DateTimeOffset</span></span>|<span data-ttu-id="f223c-136">Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f223c-136">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="f223c-137">partnerState</span><span class="sxs-lookup"><span data-stu-id="f223c-137">partnerState</span></span>|[<span data-ttu-id="f223c-138">deviceManagementPartnerTenantState</span><span class="sxs-lookup"><span data-stu-id="f223c-138">deviceManagementPartnerTenantState</span></span>](../resources/intune-onboarding-devicemanagementpartnertenantstate.md)|<span data-ttu-id="f223c-139">Estado de socio de este inquilino.</span><span class="sxs-lookup"><span data-stu-id="f223c-139">Partner state of this tenant.</span></span> <span data-ttu-id="f223c-140">Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span><span class="sxs-lookup"><span data-stu-id="f223c-140">Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="f223c-141">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="f223c-141">partnerAppType</span></span>|[<span data-ttu-id="f223c-142">deviceManagementPartnerAppType</span><span class="sxs-lookup"><span data-stu-id="f223c-142">deviceManagementPartnerAppType</span></span>](../resources/intune-onboarding-devicemanagementpartnerapptype.md)|<span data-ttu-id="f223c-143">Tipo de aplicación de socio.</span><span class="sxs-lookup"><span data-stu-id="f223c-143">Partner App type.</span></span> <span data-ttu-id="f223c-144">Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.</span><span class="sxs-lookup"><span data-stu-id="f223c-144">Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="f223c-145">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="f223c-145">singleTenantAppId</span></span>|<span data-ttu-id="f223c-146">String</span><span class="sxs-lookup"><span data-stu-id="f223c-146">String</span></span>|<span data-ttu-id="f223c-147">Identificador de aplicación de espacio empresarial único de partner</span><span class="sxs-lookup"><span data-stu-id="f223c-147">Partner Single tenant App id</span></span>|
|<span data-ttu-id="f223c-148">displayName</span><span class="sxs-lookup"><span data-stu-id="f223c-148">displayName</span></span>|<span data-ttu-id="f223c-149">String</span><span class="sxs-lookup"><span data-stu-id="f223c-149">String</span></span>|<span data-ttu-id="f223c-150">Nombre para mostrar del partner</span><span class="sxs-lookup"><span data-stu-id="f223c-150">Partner display name</span></span>|
|<span data-ttu-id="f223c-151">isConfigured</span><span class="sxs-lookup"><span data-stu-id="f223c-151">isConfigured</span></span>|<span data-ttu-id="f223c-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="f223c-152">Boolean</span></span>|<span data-ttu-id="f223c-153">Si el partner de administración de dispositivos está configurado o no</span><span class="sxs-lookup"><span data-stu-id="f223c-153">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="f223c-154">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="f223c-154">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="f223c-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f223c-155">DateTimeOffset</span></span>|<span data-ttu-id="f223c-156">Fecha y hora en UTC de cuándo se quitará PartnerDevices</span><span class="sxs-lookup"><span data-stu-id="f223c-156">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="f223c-157">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="f223c-157">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="f223c-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f223c-158">DateTimeOffset</span></span>|<span data-ttu-id="f223c-159">Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible</span><span class="sxs-lookup"><span data-stu-id="f223c-159">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="f223c-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f223c-160">Response</span></span>
<span data-ttu-id="f223c-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f223c-161">If successful, this method returns a `200 OK` response code and an updated [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f223c-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f223c-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="f223c-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f223c-163">Request</span></span>
<span data-ttu-id="f223c-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f223c-164">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f223c-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f223c-165">Response</span></span>
<span data-ttu-id="f223c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f223c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



