---
title: Obtener managedAppPolicyDeploymentSummary
description: Lea las propiedades y las relaciones del objeto managedAppPolicyDeploymentSummary.
author: tfitzmac
ms.openlocfilehash: 7c33021c0bfa31f6a562bfc54efb4d8d195dadd8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334884"
---
# <a name="get-managedapppolicydeploymentsummary"></a><span data-ttu-id="361f5-103">Obtener managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="361f5-103">Get managedAppPolicyDeploymentSummary</span></span>

> <span data-ttu-id="361f5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="361f5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="361f5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="361f5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="361f5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="361f5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="361f5-107">Lea las propiedades y las relaciones del objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="361f5-107">Read properties and relationships of the [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="361f5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="361f5-108">Prerequisites</span></span>
<span data-ttu-id="361f5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="361f5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="361f5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="361f5-111">Permission type</span></span>|<span data-ttu-id="361f5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="361f5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="361f5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="361f5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="361f5-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="361f5-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="361f5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="361f5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="361f5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="361f5-116">Not supported.</span></span>|
|<span data-ttu-id="361f5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="361f5-117">Application</span></span>|<span data-ttu-id="361f5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="361f5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="361f5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="361f5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
GET /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/deploymentSummary
GET /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/deploymentSummary
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/deploymentSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="361f5-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="361f5-120">Optional query parameters</span></span>
<span data-ttu-id="361f5-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="361f5-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="361f5-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="361f5-122">Request headers</span></span>
|<span data-ttu-id="361f5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="361f5-123">Header</span></span>|<span data-ttu-id="361f5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="361f5-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="361f5-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="361f5-125">Authorization</span></span>|<span data-ttu-id="361f5-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="361f5-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="361f5-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="361f5-127">Accept</span></span>|<span data-ttu-id="361f5-128">application/json</span><span class="sxs-lookup"><span data-stu-id="361f5-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="361f5-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="361f5-129">Request body</span></span>
<span data-ttu-id="361f5-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="361f5-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="361f5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="361f5-131">Response</span></span>
<span data-ttu-id="361f5-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="361f5-132">If successful, this method returns a `200 OK` response code and [managedAppPolicyDeploymentSummary](../resources/intune-mam-managedapppolicydeploymentsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="361f5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="361f5-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="361f5-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="361f5-134">Request</span></span>
<span data-ttu-id="361f5-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="361f5-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
```

### <a name="response"></a><span data-ttu-id="361f5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="361f5-136">Response</span></span>
<span data-ttu-id="361f5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="361f5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 688

{
  "value": {
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
}
```





