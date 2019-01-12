---
title: Lista userAppInstallStatuses
description: Propiedades de la lista y relaciones de los objetos userAppInstallStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7638ce7755c655c454022bcf2df5556abac109f4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985196"
---
# <a name="list-userappinstallstatuses"></a><span data-ttu-id="71f71-103">Lista userAppInstallStatuses</span><span class="sxs-lookup"><span data-stu-id="71f71-103">List userAppInstallStatuses</span></span>

> <span data-ttu-id="71f71-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71f71-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71f71-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71f71-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="71f71-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71f71-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71f71-107">Propiedades de la lista y relaciones de los objetos [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="71f71-107">List properties and relationships of the [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71f71-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71f71-108">Prerequisites</span></span>
<span data-ttu-id="71f71-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71f71-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71f71-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71f71-111">Permission type</span></span>|<span data-ttu-id="71f71-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71f71-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71f71-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71f71-113">Delegated (work or school account)</span></span>|<span data-ttu-id="71f71-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="71f71-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="71f71-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71f71-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71f71-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71f71-116">Not supported.</span></span>|
|<span data-ttu-id="71f71-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71f71-117">Application</span></span>|<span data-ttu-id="71f71-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71f71-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71f71-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71f71-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="71f71-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71f71-120">Request headers</span></span>
|<span data-ttu-id="71f71-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71f71-121">Header</span></span>|<span data-ttu-id="71f71-122">Valor</span><span class="sxs-lookup"><span data-stu-id="71f71-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71f71-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="71f71-123">Authorization</span></span>|<span data-ttu-id="71f71-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71f71-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71f71-125">Accept</span><span class="sxs-lookup"><span data-stu-id="71f71-125">Accept</span></span>|<span data-ttu-id="71f71-126">application/json</span><span class="sxs-lookup"><span data-stu-id="71f71-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71f71-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71f71-127">Request body</span></span>
<span data-ttu-id="71f71-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71f71-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71f71-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71f71-129">Response</span></span>
<span data-ttu-id="71f71-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71f71-130">If successful, this method returns a `200 OK` response code and a collection of [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71f71-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71f71-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="71f71-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71f71-132">Request</span></span>
<span data-ttu-id="71f71-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71f71-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/userStatuses
```

### <a name="response"></a><span data-ttu-id="71f71-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71f71-134">Response</span></span>
<span data-ttu-id="71f71-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71f71-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 349

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.userAppInstallStatus",
      "id": "14959a2a-9a2a-1495-2a9a-95142a9a9514",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value",
      "installedDeviceCount": 4,
      "failedDeviceCount": 1,
      "notInstalledDeviceCount": 7
    }
  ]
}
```





