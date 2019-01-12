---
title: Obtener restrictedAppsViolation
description: Leer las propiedades y las relaciones del objeto restrictedAppsViolation.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f0dd407e71f0ed777bceb1e8711df522230961ca
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950322"
---
# <a name="get-restrictedappsviolation"></a><span data-ttu-id="c5534-103">Obtener restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="c5534-103">Get restrictedAppsViolation</span></span>

> <span data-ttu-id="c5534-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5534-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5534-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5534-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c5534-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c5534-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c5534-107">Leer las propiedades y las relaciones del objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="c5534-107">Read properties and relationships of the [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c5534-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c5534-108">Prerequisites</span></span>
<span data-ttu-id="c5534-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5534-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c5534-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c5534-111">Permission type</span></span>|<span data-ttu-id="c5534-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c5534-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c5534-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c5534-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c5534-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c5534-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="c5534-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c5534-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c5534-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5534-116">Not supported.</span></span>|
|<span data-ttu-id="c5534-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c5534-117">Application</span></span>|<span data-ttu-id="c5534-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5534-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c5534-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5534-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurationRestrictedAppsViolations/{restrictedAppsViolationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c5534-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c5534-120">Optional query parameters</span></span>
<span data-ttu-id="c5534-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5534-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c5534-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5534-122">Request headers</span></span>
|<span data-ttu-id="c5534-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5534-123">Header</span></span>|<span data-ttu-id="c5534-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c5534-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c5534-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="c5534-125">Authorization</span></span>|<span data-ttu-id="c5534-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c5534-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c5534-127">Accept</span><span class="sxs-lookup"><span data-stu-id="c5534-127">Accept</span></span>|<span data-ttu-id="c5534-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c5534-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c5534-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5534-129">Request body</span></span>
<span data-ttu-id="c5534-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c5534-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c5534-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5534-131">Response</span></span>
<span data-ttu-id="c5534-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5534-132">If successful, this method returns a `200 OK` response code and [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c5534-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5534-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="c5534-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5534-134">Request</span></span>
<span data-ttu-id="c5534-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5534-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationRestrictedAppsViolations/{restrictedAppsViolationId}
```

### <a name="response"></a><span data-ttu-id="c5534-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5534-136">Response</span></span>
<span data-ttu-id="c5534-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5534-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 664

{
  "value": {
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
}
```





