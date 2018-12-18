---
title: Obtener sharedPCConfiguration
description: Lea las propiedades y las relaciones del objeto sharedPCConfiguration.
author: tfitzmac
ms.openlocfilehash: 477103638c0d0315ee285c21b4572328038759fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344761"
---
# <a name="get-sharedpcconfiguration"></a><span data-ttu-id="a87ff-103">Obtener sharedPCConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87ff-103">Get sharedPCConfiguration</span></span>

> <span data-ttu-id="a87ff-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a87ff-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a87ff-105">Lea las propiedades y las relaciones del objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a87ff-105">Read properties and relationships of the [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a87ff-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a87ff-106">Prerequisites</span></span>
<span data-ttu-id="a87ff-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a87ff-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a87ff-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a87ff-109">Permission type</span></span>|<span data-ttu-id="a87ff-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a87ff-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a87ff-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a87ff-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a87ff-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a87ff-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a87ff-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a87ff-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a87ff-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a87ff-114">Not supported.</span></span>|
|<span data-ttu-id="a87ff-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a87ff-115">Application</span></span>|<span data-ttu-id="a87ff-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a87ff-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a87ff-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a87ff-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a87ff-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a87ff-118">Optional query parameters</span></span>
<span data-ttu-id="a87ff-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a87ff-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a87ff-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a87ff-120">Request headers</span></span>
|<span data-ttu-id="a87ff-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a87ff-121">Header</span></span>|<span data-ttu-id="a87ff-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a87ff-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a87ff-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a87ff-123">Authorization</span></span>|<span data-ttu-id="a87ff-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a87ff-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a87ff-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a87ff-125">Accept</span></span>|<span data-ttu-id="a87ff-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a87ff-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a87ff-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a87ff-127">Request body</span></span>
<span data-ttu-id="a87ff-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a87ff-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a87ff-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a87ff-129">Response</span></span>
<span data-ttu-id="a87ff-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a87ff-130">If successful, this method returns a `200 OK` response code and [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a87ff-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a87ff-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a87ff-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a87ff-132">Request</span></span>
<span data-ttu-id="a87ff-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a87ff-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="a87ff-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a87ff-134">Response</span></span>
<span data-ttu-id="a87ff-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a87ff-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1101

{
  "value": {
    "@odata.type": "#microsoft.graph.sharedPCConfiguration",
    "id": "5206be3b-be3b-5206-3bbe-06523bbe0652",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "accountManagerPolicy": {
      "@odata.type": "microsoft.graph.sharedPCAccountManagerPolicy",
      "accountDeletionPolicy": "diskSpaceThreshold",
      "cacheAccountsAboveDiskFreePercentage": 4,
      "inactiveThresholdDays": 5,
      "removeAccountsBelowDiskFreePercentage": 5
    },
    "allowedAccounts": "domain",
    "allowLocalStorage": true,
    "disableAccountManager": true,
    "disableEduPolicies": true,
    "disablePowerPolicies": true,
    "disableSignInOnResume": true,
    "enabled": true,
    "idleTimeBeforeSleepInSeconds": 12,
    "kioskAppDisplayName": "Kiosk App Display Name value",
    "kioskAppUserModelId": "Kiosk App User Model Id value",
    "maintenanceStartTime": "11:59:24.7240000"
  }
}
```



