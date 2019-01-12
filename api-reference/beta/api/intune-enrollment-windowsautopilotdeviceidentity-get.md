---
title: Obtener windowsAutopilotDeviceIdentity
description: Leer las propiedades y las relaciones del objeto windowsAutopilotDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 0334737780fb2c98b0dbb0d8e3c07ef1ac9d20a5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969796"
---
# <a name="get-windowsautopilotdeviceidentity"></a><span data-ttu-id="9b0ae-103">Obtener windowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="9b0ae-103">Get windowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="9b0ae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b0ae-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b0ae-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b0ae-107">Leer las propiedades y las relaciones del objeto [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="9b0ae-107">Read properties and relationships of the [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b0ae-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b0ae-108">Prerequisites</span></span>
<span data-ttu-id="9b0ae-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b0ae-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b0ae-111">Permission type</span></span>|<span data-ttu-id="9b0ae-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b0ae-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9b0ae-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="9b0ae-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="9b0ae-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b0ae-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b0ae-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-116">Not supported.</span></span>|
|<span data-ttu-id="9b0ae-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b0ae-117">Application</span></span>|<span data-ttu-id="9b0ae-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b0ae-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b0ae-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}
GET /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignedDevices/{windowsAutopilotDeviceIdentityId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9b0ae-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9b0ae-120">Optional query parameters</span></span>
<span data-ttu-id="9b0ae-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9b0ae-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ae-122">Request headers</span></span>
|<span data-ttu-id="9b0ae-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b0ae-123">Header</span></span>|<span data-ttu-id="9b0ae-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9b0ae-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b0ae-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="9b0ae-125">Authorization</span></span>|<span data-ttu-id="9b0ae-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b0ae-127">Accept</span><span class="sxs-lookup"><span data-stu-id="9b0ae-127">Accept</span></span>|<span data-ttu-id="9b0ae-128">application/json</span><span class="sxs-lookup"><span data-stu-id="9b0ae-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b0ae-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ae-129">Request body</span></span>
<span data-ttu-id="9b0ae-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9b0ae-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0ae-131">Response</span></span>
<span data-ttu-id="9b0ae-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-132">If successful, this method returns a `200 OK` response code and [windowsAutopilotDeviceIdentity](../resources/intune-enrollment-windowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b0ae-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b0ae-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b0ae-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ae-134">Request</span></span>
<span data-ttu-id="9b0ae-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}
```

### <a name="response"></a><span data-ttu-id="9b0ae-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0ae-136">Response</span></span>
<span data-ttu-id="9b0ae-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b0ae-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 853

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsAutopilotDeviceIdentity",
    "id": "fac6f0b1-f0b1-fac6-b1f0-c6fab1f0c6fa",
    "deploymentProfileAssignmentStatus": "assignedInSync",
    "deploymentProfileAssignmentDetailedStatus": "hardwareRequirementsNotMet",
    "deploymentProfileAssignedDateTime": "2016-12-31T23:58:26.2447023-08:00",
    "orderIdentifier": "Order Identifier value",
    "purchaseOrderIdentifier": "Purchase Order Identifier value",
    "serialNumber": "Serial Number value",
    "productKey": "Product Key value",
    "manufacturer": "Manufacturer value",
    "model": "Model value",
    "enrollmentState": "enrolled",
    "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
    "addressableUserName": "Addressable User Name value",
    "userPrincipalName": "User Principal Name value"
  }
}
```





