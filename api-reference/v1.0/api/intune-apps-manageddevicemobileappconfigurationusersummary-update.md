---
title: Actualizar managedDeviceMobileAppConfigurationUserSummary
description: Actualice las propiedades de un objeto managedDeviceMobileAppConfigurationUserSummary.
ms.openlocfilehash: 179f2de37fab17a6ef37a60d00c6b2c566906f9c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028898"
---
# <a name="update-manageddevicemobileappconfigurationusersummary"></a><span data-ttu-id="78161-103">Actualizar managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="78161-103">Update managedDeviceMobileAppConfigurationUserSummary</span></span>

> <span data-ttu-id="78161-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78161-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78161-105">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="78161-105">Update the properties of a [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="78161-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="78161-106">Prerequisites</span></span>
<span data-ttu-id="78161-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="78161-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="78161-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78161-109">Permission type</span></span>|<span data-ttu-id="78161-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78161-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="78161-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78161-111">Delegated (work or school account)</span></span>|<span data-ttu-id="78161-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="78161-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="78161-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78161-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="78161-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78161-114">Not supported.</span></span>|
|<span data-ttu-id="78161-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78161-115">Application</span></span>|<span data-ttu-id="78161-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78161-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="78161-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78161-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="78161-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78161-118">Request headers</span></span>
|<span data-ttu-id="78161-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78161-119">Header</span></span>|<span data-ttu-id="78161-120">Valor</span><span class="sxs-lookup"><span data-stu-id="78161-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="78161-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="78161-121">Authorization</span></span>|<span data-ttu-id="78161-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="78161-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="78161-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="78161-123">Accept</span></span>|<span data-ttu-id="78161-124">application/json</span><span class="sxs-lookup"><span data-stu-id="78161-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="78161-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78161-125">Request body</span></span>
<span data-ttu-id="78161-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="78161-126">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>

<span data-ttu-id="78161-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="78161-127">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span></span>

|<span data-ttu-id="78161-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78161-128">Property</span></span>|<span data-ttu-id="78161-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="78161-129">Type</span></span>|<span data-ttu-id="78161-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="78161-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78161-131">id</span><span class="sxs-lookup"><span data-stu-id="78161-131">id</span></span>|<span data-ttu-id="78161-132">String</span><span class="sxs-lookup"><span data-stu-id="78161-132">String</span></span>|<span data-ttu-id="78161-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="78161-133">Key of the entity.</span></span>|
|<span data-ttu-id="78161-134">pendingCount</span><span class="sxs-lookup"><span data-stu-id="78161-134">pendingCount</span></span>|<span data-ttu-id="78161-135">Int32</span><span class="sxs-lookup"><span data-stu-id="78161-135">Int32</span></span>|<span data-ttu-id="78161-136">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="78161-136">Number of pending Users</span></span>|
|<span data-ttu-id="78161-137">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="78161-137">notApplicableCount</span></span>|<span data-ttu-id="78161-138">Int32</span><span class="sxs-lookup"><span data-stu-id="78161-138">Int32</span></span>|<span data-ttu-id="78161-139">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="78161-139">Number of not applicable users</span></span>|
|<span data-ttu-id="78161-140">successCount</span><span class="sxs-lookup"><span data-stu-id="78161-140">successCount</span></span>|<span data-ttu-id="78161-141">Int32</span><span class="sxs-lookup"><span data-stu-id="78161-141">Int32</span></span>|<span data-ttu-id="78161-142">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="78161-142">Number of succeeded Users</span></span>|
|<span data-ttu-id="78161-143">errorCount</span><span class="sxs-lookup"><span data-stu-id="78161-143">errorCount</span></span>|<span data-ttu-id="78161-144">Int32</span><span class="sxs-lookup"><span data-stu-id="78161-144">Int32</span></span>|<span data-ttu-id="78161-145">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="78161-145">Number of error Users</span></span>|
|<span data-ttu-id="78161-146">failedCount</span><span class="sxs-lookup"><span data-stu-id="78161-146">failedCount</span></span>|<span data-ttu-id="78161-147">Int32</span><span class="sxs-lookup"><span data-stu-id="78161-147">Int32</span></span>|<span data-ttu-id="78161-148">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="78161-148">Number of failed Users</span></span>|
|<span data-ttu-id="78161-149">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="78161-149">lastUpdateDateTime</span></span>|<span data-ttu-id="78161-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="78161-150">DateTimeOffset</span></span>|<span data-ttu-id="78161-151">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="78161-151">Last update time</span></span>|
|<span data-ttu-id="78161-152">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="78161-152">configurationVersion</span></span>|<span data-ttu-id="78161-153">Int32</span><span class="sxs-lookup"><span data-stu-id="78161-153">Int32</span></span>|<span data-ttu-id="78161-154">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="78161-154">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="78161-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78161-155">Response</span></span>
<span data-ttu-id="78161-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78161-156">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78161-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78161-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="78161-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78161-158">Request</span></span>
<span data-ttu-id="78161-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78161-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatusSummary
Content-type: application/json
Content-length: 297

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserSummary",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="78161-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78161-160">Response</span></span>
<span data-ttu-id="78161-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78161-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 346

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserSummary",
  "id": "7b953742-3742-7b95-4237-957b4237957b",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```



