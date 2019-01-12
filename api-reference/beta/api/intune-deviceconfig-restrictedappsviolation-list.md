---
title: Lista restrictedAppsViolations
description: Propiedades de la lista y relaciones de los objetos restrictedAppsViolation.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ecd78f2300461198b31fb94117005995d12892bb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950378"
---
# <a name="list-restrictedappsviolations"></a><span data-ttu-id="7cb77-103">Lista restrictedAppsViolations</span><span class="sxs-lookup"><span data-stu-id="7cb77-103">List restrictedAppsViolations</span></span>

> <span data-ttu-id="7cb77-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7cb77-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7cb77-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7cb77-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7cb77-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7cb77-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7cb77-107">Propiedades de la lista y relaciones de los objetos [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="7cb77-107">List properties and relationships of the [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7cb77-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7cb77-108">Prerequisites</span></span>
<span data-ttu-id="7cb77-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7cb77-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7cb77-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7cb77-111">Permission type</span></span>|<span data-ttu-id="7cb77-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7cb77-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7cb77-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7cb77-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7cb77-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="7cb77-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="7cb77-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7cb77-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7cb77-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7cb77-116">Not supported.</span></span>|
|<span data-ttu-id="7cb77-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7cb77-117">Application</span></span>|<span data-ttu-id="7cb77-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7cb77-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7cb77-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7cb77-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurationRestrictedAppsViolations
```

## <a name="request-headers"></a><span data-ttu-id="7cb77-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7cb77-120">Request headers</span></span>
|<span data-ttu-id="7cb77-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cb77-121">Header</span></span>|<span data-ttu-id="7cb77-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb77-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7cb77-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7cb77-123">Authorization</span></span>|<span data-ttu-id="7cb77-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7cb77-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7cb77-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7cb77-125">Accept</span></span>|<span data-ttu-id="7cb77-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7cb77-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7cb77-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7cb77-127">Request body</span></span>
<span data-ttu-id="7cb77-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7cb77-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7cb77-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7cb77-129">Response</span></span>
<span data-ttu-id="7cb77-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7cb77-130">If successful, this method returns a `200 OK` response code and a collection of [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7cb77-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7cb77-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="7cb77-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7cb77-132">Request</span></span>
<span data-ttu-id="7cb77-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7cb77-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationRestrictedAppsViolations
```

### <a name="response"></a><span data-ttu-id="7cb77-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7cb77-134">Response</span></span>
<span data-ttu-id="7cb77-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7cb77-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 710

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.restrictedAppsViolation",
      "id": "53f99903-9903-53f9-0399-f9530399f953",
      "userId": "User Id value",
      "userName": "User Name value",
      "managedDeviceId": "Managed Device Id value",
      "deviceName": "Device Name value",
      "deviceConfigurationId": "Device Configuration Id value",
      "deviceConfigurationName": "Device Configuration Name value",
      "platformType": "androidForWork",
      "restrictedAppsState": "notApprovedApps",
      "restrictedApps": [
        {
          "@odata.type": "microsoft.graph.managedDeviceReportedApp",
          "appId": "App Id value"
        }
      ]
    }
  ]
}
```





