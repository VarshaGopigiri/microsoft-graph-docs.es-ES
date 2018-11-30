---
title: Actualizar deviceComplianceUserOverview
description: Actualice las propiedades de un objeto deviceComplianceUserOverview.
ms.openlocfilehash: b00c5576506aad566872dbf3477c643cd411782b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090150"
---
# <a name="update-devicecomplianceuseroverview"></a><span data-ttu-id="ae70b-103">Actualizar deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="ae70b-103">Update deviceComplianceUserOverview</span></span>

> <span data-ttu-id="ae70b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ae70b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ae70b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ae70b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ae70b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ae70b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ae70b-107">Actualice las propiedades de un objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="ae70b-107">Update the properties of a [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ae70b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae70b-108">Prerequisites</span></span>
<span data-ttu-id="ae70b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae70b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ae70b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae70b-111">Permission type</span></span>|<span data-ttu-id="ae70b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae70b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ae70b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae70b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ae70b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ae70b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ae70b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae70b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ae70b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae70b-116">Not supported.</span></span>|
|<span data-ttu-id="ae70b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae70b-117">Application</span></span>|<span data-ttu-id="ae70b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae70b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ae70b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae70b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="ae70b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae70b-120">Request headers</span></span>
|<span data-ttu-id="ae70b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae70b-121">Header</span></span>|<span data-ttu-id="ae70b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ae70b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ae70b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae70b-123">Authorization</span></span>|<span data-ttu-id="ae70b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ae70b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ae70b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ae70b-125">Accept</span></span>|<span data-ttu-id="ae70b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ae70b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ae70b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae70b-127">Request body</span></span>
<span data-ttu-id="ae70b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="ae70b-128">In the request body, supply a JSON representation for the [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object.</span></span>

<span data-ttu-id="ae70b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="ae70b-129">The following table shows the properties that are required when you create the [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span></span>

|<span data-ttu-id="ae70b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae70b-130">Property</span></span>|<span data-ttu-id="ae70b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae70b-131">Type</span></span>|<span data-ttu-id="ae70b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae70b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ae70b-133">id</span><span class="sxs-lookup"><span data-stu-id="ae70b-133">id</span></span>|<span data-ttu-id="ae70b-134">String</span><span class="sxs-lookup"><span data-stu-id="ae70b-134">String</span></span>|<span data-ttu-id="ae70b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ae70b-135">Key of the entity.</span></span>|
|<span data-ttu-id="ae70b-136">pendingCount</span><span class="sxs-lookup"><span data-stu-id="ae70b-136">pendingCount</span></span>|<span data-ttu-id="ae70b-137">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-137">Int32</span></span>|<span data-ttu-id="ae70b-138">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="ae70b-138">Number of pending Users</span></span>|
|<span data-ttu-id="ae70b-139">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="ae70b-139">notApplicableCount</span></span>|<span data-ttu-id="ae70b-140">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-140">Int32</span></span>|<span data-ttu-id="ae70b-141">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="ae70b-141">Number of not applicable users</span></span>|
|<span data-ttu-id="ae70b-142">successCount</span><span class="sxs-lookup"><span data-stu-id="ae70b-142">successCount</span></span>|<span data-ttu-id="ae70b-143">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-143">Int32</span></span>|<span data-ttu-id="ae70b-144">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="ae70b-144">Number of succeeded Users</span></span>|
|<span data-ttu-id="ae70b-145">errorCount</span><span class="sxs-lookup"><span data-stu-id="ae70b-145">errorCount</span></span>|<span data-ttu-id="ae70b-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-146">Int32</span></span>|<span data-ttu-id="ae70b-147">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="ae70b-147">Number of error Users</span></span>|
|<span data-ttu-id="ae70b-148">failedCount</span><span class="sxs-lookup"><span data-stu-id="ae70b-148">failedCount</span></span>|<span data-ttu-id="ae70b-149">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-149">Int32</span></span>|<span data-ttu-id="ae70b-150">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="ae70b-150">Number of failed Users</span></span>|
|<span data-ttu-id="ae70b-151">conflictCount</span><span class="sxs-lookup"><span data-stu-id="ae70b-151">conflictCount</span></span>|<span data-ttu-id="ae70b-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-152">Int32</span></span>|<span data-ttu-id="ae70b-153">Número de usuarios en conflicto</span><span class="sxs-lookup"><span data-stu-id="ae70b-153">Number of users in conflict</span></span>|
|<span data-ttu-id="ae70b-154">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="ae70b-154">lastUpdateDateTime</span></span>|<span data-ttu-id="ae70b-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ae70b-155">DateTimeOffset</span></span>|<span data-ttu-id="ae70b-156">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="ae70b-156">Last update time</span></span>|
|<span data-ttu-id="ae70b-157">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="ae70b-157">configurationVersion</span></span>|<span data-ttu-id="ae70b-158">Int32</span><span class="sxs-lookup"><span data-stu-id="ae70b-158">Int32</span></span>|<span data-ttu-id="ae70b-159">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="ae70b-159">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="ae70b-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae70b-160">Response</span></span>
<span data-ttu-id="ae70b-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae70b-161">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ae70b-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae70b-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="ae70b-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae70b-163">Request</span></span>
<span data-ttu-id="ae70b-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae70b-164">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
Content-type: application/json
Content-length: 236

{
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="ae70b-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae70b-165">Response</span></span>
<span data-ttu-id="ae70b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ae70b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 352

{
  "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
  "id": "2d4f5bf4-5bf4-2d4f-f45b-4f2df45b4f2d",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```





