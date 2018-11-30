---
title: Actualizar managedAppPolicyDeploymentSummary
description: Actualice las propiedades de un objeto managedAppPolicyDeploymentSummary.
ms.openlocfilehash: 66f6e10dda834eca3ffa728ea4cacbbcdd78e9e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030965"
---
# <a name="update-managedapppolicydeploymentsummary"></a><span data-ttu-id="3dab2-103">Actualizar managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="3dab2-103">Update managedAppPolicyDeploymentSummary</span></span>

> <span data-ttu-id="3dab2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3dab2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3dab2-105">Actualice las propiedades de un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="3dab2-105">Update the properties of a [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3dab2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3dab2-106">Prerequisites</span></span>
<span data-ttu-id="3dab2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3dab2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3dab2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3dab2-109">Permission type</span></span>|<span data-ttu-id="3dab2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3dab2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3dab2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3dab2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3dab2-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3dab2-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3dab2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3dab2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3dab2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3dab2-114">Not supported.</span></span>|
|<span data-ttu-id="3dab2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3dab2-115">Application</span></span>|<span data-ttu-id="3dab2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3dab2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3dab2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3dab2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
PATCH /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/deploymentSummary
PATCH /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/deploymentSummary
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/deploymentSummary
```

## <a name="request-headers"></a><span data-ttu-id="3dab2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3dab2-118">Request headers</span></span>
|<span data-ttu-id="3dab2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dab2-119">Header</span></span>|<span data-ttu-id="3dab2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3dab2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3dab2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3dab2-121">Authorization</span></span>|<span data-ttu-id="3dab2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3dab2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3dab2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3dab2-123">Accept</span></span>|<span data-ttu-id="3dab2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3dab2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3dab2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3dab2-125">Request body</span></span>
<span data-ttu-id="3dab2-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="3dab2-126">In the request body, supply a JSON representation for the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>

<span data-ttu-id="3dab2-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="3dab2-127">The following table shows the properties that are required when you create the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span></span>

|<span data-ttu-id="3dab2-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3dab2-128">Property</span></span>|<span data-ttu-id="3dab2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3dab2-129">Type</span></span>|<span data-ttu-id="3dab2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3dab2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3dab2-131">displayName</span><span class="sxs-lookup"><span data-stu-id="3dab2-131">displayName</span></span>|<span data-ttu-id="3dab2-132">String</span><span class="sxs-lookup"><span data-stu-id="3dab2-132">String</span></span>|<span data-ttu-id="3dab2-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3dab2-133">Not yet documented</span></span>|
|<span data-ttu-id="3dab2-134">configurationDeployedUserCount</span><span class="sxs-lookup"><span data-stu-id="3dab2-134">configurationDeployedUserCount</span></span>|<span data-ttu-id="3dab2-135">Int32</span><span class="sxs-lookup"><span data-stu-id="3dab2-135">Int32</span></span>|<span data-ttu-id="3dab2-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3dab2-136">Not yet documented</span></span>|
|<span data-ttu-id="3dab2-137">lastRefreshTime</span><span class="sxs-lookup"><span data-stu-id="3dab2-137">lastRefreshTime</span></span>|<span data-ttu-id="3dab2-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3dab2-138">DateTimeOffset</span></span>|<span data-ttu-id="3dab2-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3dab2-139">Not yet documented</span></span>|
|<span data-ttu-id="3dab2-140">configurationDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="3dab2-140">configurationDeploymentSummaryPerApp</span></span>|<span data-ttu-id="3dab2-141">Colección [managedAppPolicyDeploymentSummaryPerApp](../resources/intune-mam-managedapppolicydeploymentsummaryperapp.md)</span><span class="sxs-lookup"><span data-stu-id="3dab2-141">[managedAppPolicyDeploymentSummaryPerApp](../resources/intune-mam-managedapppolicydeploymentsummaryperapp.md) collection</span></span>|<span data-ttu-id="3dab2-142">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3dab2-142">Not yet documented</span></span>|
|<span data-ttu-id="3dab2-143">id</span><span class="sxs-lookup"><span data-stu-id="3dab2-143">id</span></span>|<span data-ttu-id="3dab2-144">String</span><span class="sxs-lookup"><span data-stu-id="3dab2-144">String</span></span>|<span data-ttu-id="3dab2-145">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3dab2-145">Key of the entity.</span></span>|
|<span data-ttu-id="3dab2-146">version</span><span class="sxs-lookup"><span data-stu-id="3dab2-146">version</span></span>|<span data-ttu-id="3dab2-147">String</span><span class="sxs-lookup"><span data-stu-id="3dab2-147">String</span></span>|<span data-ttu-id="3dab2-148">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3dab2-148">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="3dab2-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3dab2-149">Response</span></span>
<span data-ttu-id="3dab2-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3dab2-150">If successful, this method returns a `200 OK` response code and an updated [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3dab2-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3dab2-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="3dab2-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3dab2-152">Request</span></span>
<span data-ttu-id="3dab2-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3dab2-153">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
Content-type: application/json
Content-length: 588

{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummary",
  "displayName": "Display Name value",
  "configurationDeployedUserCount": 14,
  "lastRefreshTime": "2017-01-01T00:01:30.1240368-08:00",
  "configurationDeploymentSummaryPerApp": [
    {
      "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "Package Id value"
      },
      "configurationAppliedUserCount": 13
    }
  ],
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="3dab2-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3dab2-154">Response</span></span>
<span data-ttu-id="3dab2-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3dab2-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 637

{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummary",
  "displayName": "Display Name value",
  "configurationDeployedUserCount": 14,
  "lastRefreshTime": "2017-01-01T00:01:30.1240368-08:00",
  "configurationDeploymentSummaryPerApp": [
    {
      "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "Package Id value"
      },
      "configurationAppliedUserCount": 13
    }
  ],
  "id": "61f2f688-f688-61f2-88f6-f26188f6f261",
  "version": "Version value"
}
```



