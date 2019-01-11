---
title: Actualizar managedAppPolicyDeploymentSummary
description: Actualice las propiedades de un objeto managedAppPolicyDeploymentSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e1d0c06a3a7bcb2e909cc3a0f0195342a5038d42
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825294"
---
# <a name="update-managedapppolicydeploymentsummary"></a><span data-ttu-id="16692-103">Actualizar managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="16692-103">Update managedAppPolicyDeploymentSummary</span></span>

> <span data-ttu-id="16692-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16692-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16692-105">Actualice las propiedades de un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="16692-105">Update the properties of a [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="16692-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16692-106">Prerequisites</span></span>
<span data-ttu-id="16692-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16692-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16692-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16692-109">Permission type</span></span>|<span data-ttu-id="16692-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16692-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="16692-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16692-111">Delegated (work or school account)</span></span>|<span data-ttu-id="16692-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16692-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="16692-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16692-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="16692-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16692-114">Not supported.</span></span>|
|<span data-ttu-id="16692-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16692-115">Application</span></span>|<span data-ttu-id="16692-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16692-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="16692-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16692-117">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="16692-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16692-118">Request headers</span></span>
|<span data-ttu-id="16692-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16692-119">Header</span></span>|<span data-ttu-id="16692-120">Valor</span><span class="sxs-lookup"><span data-stu-id="16692-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="16692-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="16692-121">Authorization</span></span>|<span data-ttu-id="16692-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="16692-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="16692-123">Accept</span><span class="sxs-lookup"><span data-stu-id="16692-123">Accept</span></span>|<span data-ttu-id="16692-124">application/json</span><span class="sxs-lookup"><span data-stu-id="16692-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="16692-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16692-125">Request body</span></span>
<span data-ttu-id="16692-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="16692-126">In the request body, supply a JSON representation for the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>

<span data-ttu-id="16692-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="16692-127">The following table shows the properties that are required when you create the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span></span>

|<span data-ttu-id="16692-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16692-128">Property</span></span>|<span data-ttu-id="16692-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="16692-129">Type</span></span>|<span data-ttu-id="16692-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="16692-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16692-131">displayName</span><span class="sxs-lookup"><span data-stu-id="16692-131">displayName</span></span>|<span data-ttu-id="16692-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="16692-132">String</span></span>|<span data-ttu-id="16692-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16692-133">Not yet documented</span></span>|
|<span data-ttu-id="16692-134">configurationDeployedUserCount</span><span class="sxs-lookup"><span data-stu-id="16692-134">configurationDeployedUserCount</span></span>|<span data-ttu-id="16692-135">Int32</span><span class="sxs-lookup"><span data-stu-id="16692-135">Int32</span></span>|<span data-ttu-id="16692-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16692-136">Not yet documented</span></span>|
|<span data-ttu-id="16692-137">lastRefreshTime</span><span class="sxs-lookup"><span data-stu-id="16692-137">lastRefreshTime</span></span>|<span data-ttu-id="16692-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16692-138">DateTimeOffset</span></span>|<span data-ttu-id="16692-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16692-139">Not yet documented</span></span>|
|<span data-ttu-id="16692-140">configurationDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="16692-140">configurationDeploymentSummaryPerApp</span></span>|<span data-ttu-id="16692-141">Colección [managedAppPolicyDeploymentSummaryPerApp](../resources/intune-mam-managedapppolicydeploymentsummaryperapp.md)</span><span class="sxs-lookup"><span data-stu-id="16692-141">[managedAppPolicyDeploymentSummaryPerApp](../resources/intune-mam-managedapppolicydeploymentsummaryperapp.md) collection</span></span>|<span data-ttu-id="16692-142">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="16692-142">Not yet documented</span></span>|
|<span data-ttu-id="16692-143">id</span><span class="sxs-lookup"><span data-stu-id="16692-143">id</span></span>|<span data-ttu-id="16692-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="16692-144">String</span></span>|<span data-ttu-id="16692-145">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="16692-145">Key of the entity.</span></span>|
|<span data-ttu-id="16692-146">version</span><span class="sxs-lookup"><span data-stu-id="16692-146">version</span></span>|<span data-ttu-id="16692-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="16692-147">String</span></span>|<span data-ttu-id="16692-148">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="16692-148">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="16692-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16692-149">Response</span></span>
<span data-ttu-id="16692-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16692-150">If successful, this method returns a `200 OK` response code and an updated [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16692-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16692-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="16692-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16692-152">Request</span></span>
<span data-ttu-id="16692-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16692-153">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="16692-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16692-154">Response</span></span>
<span data-ttu-id="16692-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16692-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



