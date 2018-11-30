---
title: Enumerar importedWindowsAutopilotDeviceIdentities
description: Lista de propiedades y relaciones de los objetos importedWindowsAutopilotDeviceIdentity.
ms.openlocfilehash: 74387db4dbfb4055a558f1213a2670e7ed3449a8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028765"
---
# <a name="list-importedwindowsautopilotdeviceidentities"></a><span data-ttu-id="1c2d6-103">Enumerar importedWindowsAutopilotDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="1c2d6-103">List importedWindowsAutopilotDeviceIdentities</span></span>

> <span data-ttu-id="1c2d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1c2d6-105">Lista de propiedades y relaciones de los objetos [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="1c2d6-105">List properties and relationships of the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1c2d6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1c2d6-106">Prerequisites</span></span>
<span data-ttu-id="1c2d6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1c2d6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1c2d6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c2d6-109">Permission type</span></span>|<span data-ttu-id="1c2d6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c2d6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1c2d6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c2d6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1c2d6-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="1c2d6-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="1c2d6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c2d6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1c2d6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-114">Not supported.</span></span>|
|<span data-ttu-id="1c2d6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c2d6-115">Application</span></span>|<span data-ttu-id="1c2d6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1c2d6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c2d6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentities
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities
```

## <a name="request-headers"></a><span data-ttu-id="1c2d6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c2d6-118">Request headers</span></span>
|<span data-ttu-id="1c2d6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c2d6-119">Header</span></span>|<span data-ttu-id="1c2d6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1c2d6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1c2d6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c2d6-121">Authorization</span></span>|<span data-ttu-id="1c2d6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1c2d6-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1c2d6-123">Accept</span></span>|<span data-ttu-id="1c2d6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1c2d6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1c2d6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c2d6-125">Request body</span></span>
<span data-ttu-id="1c2d6-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c2d6-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c2d6-127">Response</span></span>
<span data-ttu-id="1c2d6-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-128">If successful, this method returns a `200 OK` response code and a collection of [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c2d6-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c2d6-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1c2d6-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c2d6-130">Request</span></span>
<span data-ttu-id="1c2d6-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentities
```

### <a name="response"></a><span data-ttu-id="1c2d6-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c2d6-132">Response</span></span>
<span data-ttu-id="1c2d6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c2d6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 675

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentity",
      "id": "985b4f49-4f49-985b-494f-5b98494f5b98",
      "orderIdentifier": "Order Identifier value",
      "serialNumber": "Serial Number value",
      "productKey": "Product Key value",
      "hardwareIdentifier": "aGFyZHdhcmVJZGVudGlmaWVy",
      "state": {
        "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
        "deviceImportStatus": "pending",
        "deviceRegistrationId": "Device Registration Id value",
        "deviceErrorCode": 15,
        "deviceErrorName": "Device Error Name value"
      }
    }
  ]
}
```



