---
title: Lista mobileAppInstallStatuses
description: Propiedades de la lista y relaciones de los objetos mobileAppInstallStatus.
ms.openlocfilehash: 5dac6698f41ebb9307ebe80e1884fe892762b3d7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084888"
---
# <a name="list-mobileappinstallstatuses"></a><span data-ttu-id="b6896-103">Lista mobileAppInstallStatuses</span><span class="sxs-lookup"><span data-stu-id="b6896-103">List mobileAppInstallStatuses</span></span>

> <span data-ttu-id="b6896-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6896-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6896-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6896-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b6896-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b6896-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6896-107">Propiedades de la lista y relaciones de los objetos [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b6896-107">List properties and relationships of the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6896-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6896-108">Prerequisites</span></span>
<span data-ttu-id="b6896-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6896-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6896-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6896-111">Permission type</span></span>|<span data-ttu-id="b6896-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6896-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b6896-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6896-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b6896-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6896-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="b6896-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6896-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b6896-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6896-116">Not supported.</span></span>|
|<span data-ttu-id="b6896-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6896-117">Application</span></span>|<span data-ttu-id="b6896-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6896-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b6896-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6896-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="b6896-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6896-120">Request headers</span></span>
|<span data-ttu-id="b6896-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6896-121">Header</span></span>|<span data-ttu-id="b6896-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b6896-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b6896-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6896-123">Authorization</span></span>|<span data-ttu-id="b6896-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b6896-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b6896-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b6896-125">Accept</span></span>|<span data-ttu-id="b6896-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b6896-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6896-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6896-127">Request body</span></span>
<span data-ttu-id="b6896-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6896-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6896-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6896-129">Response</span></span>
<span data-ttu-id="b6896-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6896-130">If successful, this method returns a `200 OK` response code and a collection of [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6896-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6896-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b6896-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6896-132">Request</span></span>
<span data-ttu-id="b6896-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6896-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="b6896-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6896-134">Response</span></span>
<span data-ttu-id="b6896-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6896-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 687

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileAppInstallStatus",
      "id": "7560ee45-ee45-7560-45ee-607545ee6075",
      "deviceName": "Device Name value",
      "deviceId": "Device Id value",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "mobileAppInstallStatusValue": "failed",
      "installState": "failed",
      "installStateDetail": "seeInstallErrorCode",
      "errorCode": 9,
      "osVersion": "Os Version value",
      "osDescription": "Os Description value",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value",
      "displayVersion": "Display Version value"
    }
  ]
}
```





