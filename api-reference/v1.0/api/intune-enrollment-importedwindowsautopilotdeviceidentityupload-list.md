---
title: Lista importedWindowsAutopilotDeviceIdentityUploads
description: Propiedades de la lista y relaciones de los objetos importedWindowsAutopilotDeviceIdentityUpload.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6fad9ad4fca9dccd1b6aa402795248e5fc67734f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857319"
---
# <a name="list-importedwindowsautopilotdeviceidentityuploads"></a><span data-ttu-id="b8706-103">Lista importedWindowsAutopilotDeviceIdentityUploads</span><span class="sxs-lookup"><span data-stu-id="b8706-103">List importedWindowsAutopilotDeviceIdentityUploads</span></span>

> <span data-ttu-id="b8706-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b8706-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b8706-105">Propiedades de la lista y relaciones de los objetos [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="b8706-105">List properties and relationships of the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b8706-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b8706-106">Prerequisites</span></span>
<span data-ttu-id="b8706-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8706-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8706-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8706-109">Permission type</span></span>|<span data-ttu-id="b8706-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8706-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b8706-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8706-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b8706-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b8706-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="b8706-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8706-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b8706-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8706-114">Not supported.</span></span>|
|<span data-ttu-id="b8706-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8706-115">Application</span></span>|<span data-ttu-id="b8706-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b8706-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b8706-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8706-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

## <a name="request-headers"></a><span data-ttu-id="b8706-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8706-118">Request headers</span></span>
|<span data-ttu-id="b8706-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8706-119">Header</span></span>|<span data-ttu-id="b8706-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b8706-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b8706-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b8706-121">Authorization</span></span>|<span data-ttu-id="b8706-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b8706-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b8706-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b8706-123">Accept</span></span>|<span data-ttu-id="b8706-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b8706-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b8706-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8706-125">Request body</span></span>
<span data-ttu-id="b8706-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b8706-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b8706-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8706-127">Response</span></span>
<span data-ttu-id="b8706-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8706-128">If successful, this method returns a `200 OK` response code and a collection of [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8706-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8706-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b8706-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8706-130">Request</span></span>
<span data-ttu-id="b8706-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8706-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

### <a name="response"></a><span data-ttu-id="b8706-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8706-132">Response</span></span>
<span data-ttu-id="b8706-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b8706-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



