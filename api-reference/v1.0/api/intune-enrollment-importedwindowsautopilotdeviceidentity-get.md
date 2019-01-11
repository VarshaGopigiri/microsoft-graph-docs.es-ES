---
title: Obtener importedWindowsAutopilotDeviceIdentity
description: Lee las propiedades y relaciones de los objetos importedWindowsAutopilotDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 370b47a8944b864f1b12b1518ac1cdcf04233850
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856038"
---
# <a name="get-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="cf85d-103">Obtener importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="cf85d-103">Get importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="cf85d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf85d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf85d-105">Lee las propiedades y relaciones de los objetos [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="cf85d-105">Read properties and relationships of the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf85d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf85d-106">Prerequisites</span></span>
<span data-ttu-id="cf85d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf85d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cf85d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf85d-109">Permission type</span></span>|<span data-ttu-id="cf85d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf85d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf85d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf85d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cf85d-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="cf85d-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="cf85d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf85d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf85d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf85d-114">Not supported.</span></span>|
|<span data-ttu-id="cf85d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf85d-115">Application</span></span>|<span data-ttu-id="cf85d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf85d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf85d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf85d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="cf85d-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cf85d-118">Optional query parameters</span></span>
<span data-ttu-id="cf85d-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf85d-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="cf85d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf85d-120">Request headers</span></span>
|<span data-ttu-id="cf85d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf85d-121">Header</span></span>|<span data-ttu-id="cf85d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cf85d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf85d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cf85d-123">Authorization</span></span>|<span data-ttu-id="cf85d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf85d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf85d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="cf85d-125">Accept</span></span>|<span data-ttu-id="cf85d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cf85d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf85d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf85d-127">Request body</span></span>
<span data-ttu-id="cf85d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cf85d-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cf85d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf85d-129">Response</span></span>
<span data-ttu-id="cf85d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf85d-130">If successful, this method returns a `200 OK` response code and [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf85d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf85d-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf85d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf85d-132">Request</span></span>
<span data-ttu-id="cf85d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf85d-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

### <a name="response"></a><span data-ttu-id="cf85d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf85d-134">Response</span></span>
<span data-ttu-id="cf85d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf85d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 635

{
  "value": {
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
}
```



