---
title: Obtener importedWindowsAutopilotDeviceIdentity
description: Lee las propiedades y relaciones de los objetos importedWindowsAutopilotDeviceIdentity.
ms.openlocfilehash: be98ceb835469301184bc12a782ecae57340db70
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090122"
---
# <a name="get-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="910c9-103">Obtener importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="910c9-103">Get importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="910c9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="910c9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="910c9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="910c9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="910c9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="910c9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="910c9-107">Lee las propiedades y relaciones de los objetos [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="910c9-107">Read properties and relationships of the [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="910c9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="910c9-108">Prerequisites</span></span>
<span data-ttu-id="910c9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="910c9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="910c9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="910c9-111">Permission type</span></span>|<span data-ttu-id="910c9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="910c9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="910c9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="910c9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="910c9-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="910c9-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="910c9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="910c9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="910c9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="910c9-116">Not supported.</span></span>|
|<span data-ttu-id="910c9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="910c9-117">Application</span></span>|<span data-ttu-id="910c9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="910c9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="910c9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="910c9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="910c9-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="910c9-120">Optional query parameters</span></span>
<span data-ttu-id="910c9-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="910c9-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="910c9-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="910c9-122">Request headers</span></span>
|<span data-ttu-id="910c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="910c9-123">Header</span></span>|<span data-ttu-id="910c9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="910c9-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="910c9-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="910c9-125">Authorization</span></span>|<span data-ttu-id="910c9-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="910c9-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="910c9-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="910c9-127">Accept</span></span>|<span data-ttu-id="910c9-128">application/json</span><span class="sxs-lookup"><span data-stu-id="910c9-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="910c9-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="910c9-129">Request body</span></span>
<span data-ttu-id="910c9-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="910c9-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="910c9-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="910c9-131">Response</span></span>
<span data-ttu-id="910c9-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="910c9-132">If successful, this method returns a `200 OK` response code and [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="910c9-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="910c9-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="910c9-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="910c9-134">Request</span></span>
<span data-ttu-id="910c9-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="910c9-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

### <a name="response"></a><span data-ttu-id="910c9-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="910c9-136">Response</span></span>
<span data-ttu-id="910c9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="910c9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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




