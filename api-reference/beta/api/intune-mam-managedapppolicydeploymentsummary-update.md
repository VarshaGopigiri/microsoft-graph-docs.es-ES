---
title: Actualizar managedAppPolicyDeploymentSummary
description: Actualice las propiedades de un objeto managedAppPolicyDeploymentSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 36f7cfb3607d34924f4b410a72310c88da4b220a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948754"
---
# <a name="update-managedapppolicydeploymentsummary"></a><span data-ttu-id="b95b3-103">Actualizar managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="b95b3-103">Update managedAppPolicyDeploymentSummary</span></span>

> <span data-ttu-id="b95b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b95b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b95b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b95b3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b95b3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b95b3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b95b3-107">Actualice las propiedades de un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="b95b3-107">Update the properties of a [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b95b3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b95b3-108">Prerequisites</span></span>
<span data-ttu-id="b95b3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b95b3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b95b3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b95b3-111">Permission type</span></span>|<span data-ttu-id="b95b3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b95b3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b95b3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b95b3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b95b3-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b95b3-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b95b3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b95b3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b95b3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b95b3-116">Not supported.</span></span>|
|<span data-ttu-id="b95b3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b95b3-117">Application</span></span>|<span data-ttu-id="b95b3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b95b3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b95b3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b95b3-119">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="b95b3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b95b3-120">Request headers</span></span>
|<span data-ttu-id="b95b3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b95b3-121">Header</span></span>|<span data-ttu-id="b95b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b95b3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b95b3-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b95b3-123">Authorization</span></span>|<span data-ttu-id="b95b3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b95b3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b95b3-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b95b3-125">Accept</span></span>|<span data-ttu-id="b95b3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b95b3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b95b3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b95b3-127">Request body</span></span>
<span data-ttu-id="b95b3-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="b95b3-128">In the request body, supply a JSON representation for the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>

<span data-ttu-id="b95b3-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="b95b3-129">The following table shows the properties that are required when you create the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span></span>

|<span data-ttu-id="b95b3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b95b3-130">Property</span></span>|<span data-ttu-id="b95b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b95b3-131">Type</span></span>|<span data-ttu-id="b95b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b95b3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b95b3-133">displayName</span><span class="sxs-lookup"><span data-stu-id="b95b3-133">displayName</span></span>|<span data-ttu-id="b95b3-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="b95b3-134">String</span></span>|<span data-ttu-id="b95b3-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b95b3-135">Not yet documented</span></span>|
|<span data-ttu-id="b95b3-136">configurationDeployedUserCount</span><span class="sxs-lookup"><span data-stu-id="b95b3-136">configurationDeployedUserCount</span></span>|<span data-ttu-id="b95b3-137">Int32</span><span class="sxs-lookup"><span data-stu-id="b95b3-137">Int32</span></span>|<span data-ttu-id="b95b3-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b95b3-138">Not yet documented</span></span>|
|<span data-ttu-id="b95b3-139">lastRefreshTime</span><span class="sxs-lookup"><span data-stu-id="b95b3-139">lastRefreshTime</span></span>|<span data-ttu-id="b95b3-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b95b3-140">DateTimeOffset</span></span>|<span data-ttu-id="b95b3-141">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b95b3-141">Not yet documented</span></span>|
|<span data-ttu-id="b95b3-142">configurationDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="b95b3-142">configurationDeploymentSummaryPerApp</span></span>|<span data-ttu-id="b95b3-143">Colección [managedAppPolicyDeploymentSummaryPerApp](../resources/intune-mam-managedapppolicydeploymentsummaryperapp.md)</span><span class="sxs-lookup"><span data-stu-id="b95b3-143">[managedAppPolicyDeploymentSummaryPerApp](../resources/intune-mam-managedapppolicydeploymentsummaryperapp.md) collection</span></span>|<span data-ttu-id="b95b3-144">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b95b3-144">Not yet documented</span></span>|
|<span data-ttu-id="b95b3-145">id</span><span class="sxs-lookup"><span data-stu-id="b95b3-145">id</span></span>|<span data-ttu-id="b95b3-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="b95b3-146">String</span></span>|<span data-ttu-id="b95b3-147">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b95b3-147">Key of the entity.</span></span>|
|<span data-ttu-id="b95b3-148">version</span><span class="sxs-lookup"><span data-stu-id="b95b3-148">version</span></span>|<span data-ttu-id="b95b3-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="b95b3-149">String</span></span>|<span data-ttu-id="b95b3-150">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b95b3-150">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="b95b3-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b95b3-151">Response</span></span>
<span data-ttu-id="b95b3-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b95b3-152">If successful, this method returns a `200 OK` response code and an updated [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b95b3-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b95b3-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="b95b3-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b95b3-154">Request</span></span>
<span data-ttu-id="b95b3-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b95b3-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
Content-type: application/json
Content-length: 516

{
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

### <a name="response"></a><span data-ttu-id="b95b3-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b95b3-156">Response</span></span>
<span data-ttu-id="b95b3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b95b3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





