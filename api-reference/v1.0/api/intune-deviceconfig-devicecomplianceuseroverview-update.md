---
title: Actualizar deviceComplianceUserOverview
description: Actualice las propiedades de un objeto deviceComplianceUserOverview.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d173a8194457c068d038ac377d06928849101c36
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855611"
---
# <a name="update-devicecomplianceuseroverview"></a><span data-ttu-id="d033a-103">Actualizar deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="d033a-103">Update deviceComplianceUserOverview</span></span>

> <span data-ttu-id="d033a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d033a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d033a-105">Actualice las propiedades de un objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="d033a-105">Update the properties of a [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d033a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d033a-106">Prerequisites</span></span>
<span data-ttu-id="d033a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d033a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d033a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d033a-109">Permission type</span></span>|<span data-ttu-id="d033a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d033a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d033a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d033a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d033a-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d033a-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d033a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d033a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d033a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d033a-114">Not supported.</span></span>|
|<span data-ttu-id="d033a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d033a-115">Application</span></span>|<span data-ttu-id="d033a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d033a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d033a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d033a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="d033a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d033a-118">Request headers</span></span>
|<span data-ttu-id="d033a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d033a-119">Header</span></span>|<span data-ttu-id="d033a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d033a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d033a-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d033a-121">Authorization</span></span>|<span data-ttu-id="d033a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d033a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d033a-123">Accept</span><span class="sxs-lookup"><span data-stu-id="d033a-123">Accept</span></span>|<span data-ttu-id="d033a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d033a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d033a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d033a-125">Request body</span></span>
<span data-ttu-id="d033a-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="d033a-126">In the request body, supply a JSON representation for the [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object.</span></span>

<span data-ttu-id="d033a-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="d033a-127">The following table shows the properties that are required when you create the [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span></span>

|<span data-ttu-id="d033a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d033a-128">Property</span></span>|<span data-ttu-id="d033a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d033a-129">Type</span></span>|<span data-ttu-id="d033a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d033a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d033a-131">id</span><span class="sxs-lookup"><span data-stu-id="d033a-131">id</span></span>|<span data-ttu-id="d033a-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="d033a-132">String</span></span>|<span data-ttu-id="d033a-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d033a-133">Key of the entity.</span></span>|
|<span data-ttu-id="d033a-134">pendingCount</span><span class="sxs-lookup"><span data-stu-id="d033a-134">pendingCount</span></span>|<span data-ttu-id="d033a-135">Int32</span><span class="sxs-lookup"><span data-stu-id="d033a-135">Int32</span></span>|<span data-ttu-id="d033a-136">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="d033a-136">Number of pending Users</span></span>|
|<span data-ttu-id="d033a-137">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="d033a-137">notApplicableCount</span></span>|<span data-ttu-id="d033a-138">Int32</span><span class="sxs-lookup"><span data-stu-id="d033a-138">Int32</span></span>|<span data-ttu-id="d033a-139">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="d033a-139">Number of not applicable users</span></span>|
|<span data-ttu-id="d033a-140">successCount</span><span class="sxs-lookup"><span data-stu-id="d033a-140">successCount</span></span>|<span data-ttu-id="d033a-141">Int32</span><span class="sxs-lookup"><span data-stu-id="d033a-141">Int32</span></span>|<span data-ttu-id="d033a-142">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="d033a-142">Number of succeeded Users</span></span>|
|<span data-ttu-id="d033a-143">errorCount</span><span class="sxs-lookup"><span data-stu-id="d033a-143">errorCount</span></span>|<span data-ttu-id="d033a-144">Int32</span><span class="sxs-lookup"><span data-stu-id="d033a-144">Int32</span></span>|<span data-ttu-id="d033a-145">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="d033a-145">Number of error Users</span></span>|
|<span data-ttu-id="d033a-146">failedCount</span><span class="sxs-lookup"><span data-stu-id="d033a-146">failedCount</span></span>|<span data-ttu-id="d033a-147">Int32</span><span class="sxs-lookup"><span data-stu-id="d033a-147">Int32</span></span>|<span data-ttu-id="d033a-148">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="d033a-148">Number of failed Users</span></span>|
|<span data-ttu-id="d033a-149">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="d033a-149">lastUpdateDateTime</span></span>|<span data-ttu-id="d033a-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d033a-150">DateTimeOffset</span></span>|<span data-ttu-id="d033a-151">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="d033a-151">Last update time</span></span>|
|<span data-ttu-id="d033a-152">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="d033a-152">configurationVersion</span></span>|<span data-ttu-id="d033a-153">Int32</span><span class="sxs-lookup"><span data-stu-id="d033a-153">Int32</span></span>|<span data-ttu-id="d033a-154">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="d033a-154">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="d033a-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d033a-155">Response</span></span>
<span data-ttu-id="d033a-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d033a-156">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d033a-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d033a-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="d033a-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d033a-158">Request</span></span>
<span data-ttu-id="d033a-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d033a-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
Content-type: application/json
Content-length: 279

{
  "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="d033a-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d033a-160">Response</span></span>
<span data-ttu-id="d033a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d033a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 328

{
  "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
  "id": "2d4f5bf4-5bf4-2d4f-f45b-4f2df45b4f2d",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```



