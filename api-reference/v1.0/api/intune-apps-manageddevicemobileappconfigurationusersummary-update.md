---
title: Actualizar managedDeviceMobileAppConfigurationUserSummary
description: Actualice las propiedades de un objeto managedDeviceMobileAppConfigurationUserSummary.
author: tfitzmac
ms.openlocfilehash: 35bcbfd5970b263b6fc0b76b0624361466dbbd68
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359468"
---
# <a name="update-manageddevicemobileappconfigurationusersummary"></a><span data-ttu-id="49743-103">Actualizar managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="49743-103">Update managedDeviceMobileAppConfigurationUserSummary</span></span>

> <span data-ttu-id="49743-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="49743-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="49743-105">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="49743-105">Update the properties of a [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="49743-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="49743-106">Prerequisites</span></span>
<span data-ttu-id="49743-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49743-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49743-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49743-109">Permission type</span></span>|<span data-ttu-id="49743-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49743-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="49743-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49743-111">Delegated (work or school account)</span></span>|<span data-ttu-id="49743-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49743-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="49743-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49743-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="49743-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49743-114">Not supported.</span></span>|
|<span data-ttu-id="49743-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49743-115">Application</span></span>|<span data-ttu-id="49743-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49743-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="49743-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49743-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="49743-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49743-118">Request headers</span></span>
|<span data-ttu-id="49743-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49743-119">Header</span></span>|<span data-ttu-id="49743-120">Valor</span><span class="sxs-lookup"><span data-stu-id="49743-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="49743-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="49743-121">Authorization</span></span>|<span data-ttu-id="49743-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="49743-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="49743-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="49743-123">Accept</span></span>|<span data-ttu-id="49743-124">application/json</span><span class="sxs-lookup"><span data-stu-id="49743-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="49743-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49743-125">Request body</span></span>
<span data-ttu-id="49743-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="49743-126">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object.</span></span>

<span data-ttu-id="49743-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="49743-127">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md).</span></span>

|<span data-ttu-id="49743-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49743-128">Property</span></span>|<span data-ttu-id="49743-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="49743-129">Type</span></span>|<span data-ttu-id="49743-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="49743-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="49743-131">id</span><span class="sxs-lookup"><span data-stu-id="49743-131">id</span></span>|<span data-ttu-id="49743-132">String</span><span class="sxs-lookup"><span data-stu-id="49743-132">String</span></span>|<span data-ttu-id="49743-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="49743-133">Key of the entity.</span></span>|
|<span data-ttu-id="49743-134">pendingCount</span><span class="sxs-lookup"><span data-stu-id="49743-134">pendingCount</span></span>|<span data-ttu-id="49743-135">Int32</span><span class="sxs-lookup"><span data-stu-id="49743-135">Int32</span></span>|<span data-ttu-id="49743-136">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="49743-136">Number of pending Users</span></span>|
|<span data-ttu-id="49743-137">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="49743-137">notApplicableCount</span></span>|<span data-ttu-id="49743-138">Int32</span><span class="sxs-lookup"><span data-stu-id="49743-138">Int32</span></span>|<span data-ttu-id="49743-139">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="49743-139">Number of not applicable users</span></span>|
|<span data-ttu-id="49743-140">successCount</span><span class="sxs-lookup"><span data-stu-id="49743-140">successCount</span></span>|<span data-ttu-id="49743-141">Int32</span><span class="sxs-lookup"><span data-stu-id="49743-141">Int32</span></span>|<span data-ttu-id="49743-142">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="49743-142">Number of succeeded Users</span></span>|
|<span data-ttu-id="49743-143">errorCount</span><span class="sxs-lookup"><span data-stu-id="49743-143">errorCount</span></span>|<span data-ttu-id="49743-144">Int32</span><span class="sxs-lookup"><span data-stu-id="49743-144">Int32</span></span>|<span data-ttu-id="49743-145">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="49743-145">Number of error Users</span></span>|
|<span data-ttu-id="49743-146">failedCount</span><span class="sxs-lookup"><span data-stu-id="49743-146">failedCount</span></span>|<span data-ttu-id="49743-147">Int32</span><span class="sxs-lookup"><span data-stu-id="49743-147">Int32</span></span>|<span data-ttu-id="49743-148">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="49743-148">Number of failed Users</span></span>|
|<span data-ttu-id="49743-149">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="49743-149">lastUpdateDateTime</span></span>|<span data-ttu-id="49743-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="49743-150">DateTimeOffset</span></span>|<span data-ttu-id="49743-151">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="49743-151">Last update time</span></span>|
|<span data-ttu-id="49743-152">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="49743-152">configurationVersion</span></span>|<span data-ttu-id="49743-153">Int32</span><span class="sxs-lookup"><span data-stu-id="49743-153">Int32</span></span>|<span data-ttu-id="49743-154">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="49743-154">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="49743-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49743-155">Response</span></span>
<span data-ttu-id="49743-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49743-156">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="49743-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49743-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="49743-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49743-158">Request</span></span>
<span data-ttu-id="49743-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49743-159">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="49743-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49743-160">Response</span></span>
<span data-ttu-id="49743-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49743-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



