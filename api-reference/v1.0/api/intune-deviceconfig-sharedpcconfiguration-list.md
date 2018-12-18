---
title: Enumerar sharedPCConfigurations
description: Enumere las propiedades y las relaciones de los objetos sharedPCConfiguration.
author: tfitzmac
ms.openlocfilehash: 7266db5644b748828889351bd6e1f21d556ba8a5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337677"
---
# <a name="list-sharedpcconfigurations"></a><span data-ttu-id="045af-103">Enumerar sharedPCConfigurations</span><span class="sxs-lookup"><span data-stu-id="045af-103">List sharedPCConfigurations</span></span>

> <span data-ttu-id="045af-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="045af-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="045af-105">Enumere las propiedades y las relaciones de los objetos [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="045af-105">List properties and relationships of the [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="045af-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="045af-106">Prerequisites</span></span>
<span data-ttu-id="045af-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="045af-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="045af-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="045af-109">Permission type</span></span>|<span data-ttu-id="045af-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="045af-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="045af-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="045af-111">Delegated (work or school account)</span></span>|<span data-ttu-id="045af-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="045af-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="045af-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="045af-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="045af-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="045af-114">Not supported.</span></span>|
|<span data-ttu-id="045af-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="045af-115">Application</span></span>|<span data-ttu-id="045af-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="045af-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="045af-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="045af-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="045af-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="045af-118">Request headers</span></span>
|<span data-ttu-id="045af-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="045af-119">Header</span></span>|<span data-ttu-id="045af-120">Valor</span><span class="sxs-lookup"><span data-stu-id="045af-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="045af-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="045af-121">Authorization</span></span>|<span data-ttu-id="045af-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="045af-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="045af-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="045af-123">Accept</span></span>|<span data-ttu-id="045af-124">application/json</span><span class="sxs-lookup"><span data-stu-id="045af-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="045af-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="045af-125">Request body</span></span>
<span data-ttu-id="045af-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="045af-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="045af-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="045af-127">Response</span></span>
<span data-ttu-id="045af-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="045af-128">If successful, this method returns a `200 OK` response code and a collection of [sharedPCConfiguration](../resources/intune-deviceconfig-sharedpcconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="045af-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="045af-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="045af-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="045af-130">Request</span></span>
<span data-ttu-id="045af-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="045af-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="045af-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="045af-132">Response</span></span>
<span data-ttu-id="045af-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="045af-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1165

{
  "value": [
    {
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
  ]
}
```



