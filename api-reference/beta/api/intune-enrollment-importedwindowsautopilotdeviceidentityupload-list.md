---
title: Lista importedWindowsAutopilotDeviceIdentityUploads
description: Propiedades de la lista y relaciones de los objetos importedWindowsAutopilotDeviceIdentityUpload.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3d6867ac4d29741f5d223168606c1e5573525c41
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968991"
---
# <a name="list-importedwindowsautopilotdeviceidentityuploads"></a><span data-ttu-id="ddfba-103">Lista importedWindowsAutopilotDeviceIdentityUploads</span><span class="sxs-lookup"><span data-stu-id="ddfba-103">List importedWindowsAutopilotDeviceIdentityUploads</span></span>

> <span data-ttu-id="ddfba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ddfba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ddfba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ddfba-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ddfba-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ddfba-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ddfba-107">Propiedades de la lista y relaciones de los objetos [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="ddfba-107">List properties and relationships of the [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ddfba-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ddfba-108">Prerequisites</span></span>
<span data-ttu-id="ddfba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ddfba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ddfba-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ddfba-111">Permission type</span></span>|<span data-ttu-id="ddfba-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ddfba-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ddfba-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ddfba-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ddfba-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="ddfba-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="ddfba-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ddfba-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ddfba-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ddfba-116">Not supported.</span></span>|
|<span data-ttu-id="ddfba-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ddfba-117">Application</span></span>|<span data-ttu-id="ddfba-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ddfba-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ddfba-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddfba-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

## <a name="request-headers"></a><span data-ttu-id="ddfba-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfba-120">Request headers</span></span>
|<span data-ttu-id="ddfba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddfba-121">Header</span></span>|<span data-ttu-id="ddfba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ddfba-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ddfba-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ddfba-123">Authorization</span></span>|<span data-ttu-id="ddfba-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ddfba-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ddfba-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ddfba-125">Accept</span></span>|<span data-ttu-id="ddfba-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ddfba-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ddfba-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfba-127">Request body</span></span>
<span data-ttu-id="ddfba-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ddfba-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ddfba-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddfba-129">Response</span></span>
<span data-ttu-id="ddfba-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddfba-130">If successful, this method returns a `200 OK` response code and a collection of [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ddfba-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddfba-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ddfba-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfba-132">Request</span></span>
<span data-ttu-id="ddfba-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddfba-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

### <a name="response"></a><span data-ttu-id="ddfba-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddfba-134">Response</span></span>
<span data-ttu-id="ddfba-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ddfba-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





