---
title: Lista importedWindowsAutopilotDeviceIdentityUploads
description: Propiedades de la lista y relaciones de los objetos importedWindowsAutopilotDeviceIdentityUpload.
author: tfitzmac
ms.openlocfilehash: 2946fa4264e5f1b275ac1c74a769b60032f775fd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353070"
---
# <a name="list-importedwindowsautopilotdeviceidentityuploads"></a><span data-ttu-id="d71e7-103">Lista importedWindowsAutopilotDeviceIdentityUploads</span><span class="sxs-lookup"><span data-stu-id="d71e7-103">List importedWindowsAutopilotDeviceIdentityUploads</span></span>

> <span data-ttu-id="d71e7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d71e7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d71e7-105">Propiedades de la lista y relaciones de los objetos [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="d71e7-105">List properties and relationships of the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d71e7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d71e7-106">Prerequisites</span></span>
<span data-ttu-id="d71e7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d71e7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d71e7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d71e7-109">Permission type</span></span>|<span data-ttu-id="d71e7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d71e7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d71e7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d71e7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d71e7-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="d71e7-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="d71e7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d71e7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d71e7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d71e7-114">Not supported.</span></span>|
|<span data-ttu-id="d71e7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d71e7-115">Application</span></span>|<span data-ttu-id="d71e7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d71e7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d71e7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d71e7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

## <a name="request-headers"></a><span data-ttu-id="d71e7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d71e7-118">Request headers</span></span>
|<span data-ttu-id="d71e7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d71e7-119">Header</span></span>|<span data-ttu-id="d71e7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d71e7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d71e7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d71e7-121">Authorization</span></span>|<span data-ttu-id="d71e7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d71e7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d71e7-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d71e7-123">Accept</span></span>|<span data-ttu-id="d71e7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d71e7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d71e7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d71e7-125">Request body</span></span>
<span data-ttu-id="d71e7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d71e7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d71e7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d71e7-127">Response</span></span>
<span data-ttu-id="d71e7-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d71e7-128">If successful, this method returns a `200 OK` response code and a collection of [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d71e7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d71e7-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="d71e7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d71e7-130">Request</span></span>
<span data-ttu-id="d71e7-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d71e7-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

### <a name="response"></a><span data-ttu-id="d71e7-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d71e7-132">Response</span></span>
<span data-ttu-id="d71e7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d71e7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 270

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
      "id": "8d639524-9524-8d63-2495-638d2495638d",
      "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
      "status": "pending"
    }
  ]
}
```



