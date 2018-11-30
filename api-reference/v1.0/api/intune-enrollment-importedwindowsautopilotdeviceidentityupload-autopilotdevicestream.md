---
title: autopilotDeviceStream (función)
description: Crear una solicitud de carga con la secuencia de dispositivo de piloto automático en ella.
ms.openlocfilehash: 484b62f33a49ac73f3ba143d1936a8332888d431
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029801"
---
# <a name="autopilotdevicestream-function"></a><span data-ttu-id="eea9b-103">autopilotDeviceStream (función)</span><span class="sxs-lookup"><span data-stu-id="eea9b-103">autopilotDeviceStream function</span></span>

> <span data-ttu-id="eea9b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eea9b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eea9b-105">Crear una solicitud de carga con la secuencia de dispositivo de piloto automático en ella.</span><span class="sxs-lookup"><span data-stu-id="eea9b-105">Create a upload request with autopilot device stream in it.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eea9b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eea9b-106">Prerequisites</span></span>
<span data-ttu-id="eea9b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eea9b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eea9b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eea9b-109">Permission type</span></span>|<span data-ttu-id="eea9b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eea9b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eea9b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eea9b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="eea9b-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eea9b-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="eea9b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eea9b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eea9b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eea9b-114">Not supported.</span></span>|
|<span data-ttu-id="eea9b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eea9b-115">Application</span></span>|<span data-ttu-id="eea9b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eea9b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eea9b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eea9b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/autopilotDeviceStream
```

## <a name="request-headers"></a><span data-ttu-id="eea9b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eea9b-118">Request headers</span></span>
|<span data-ttu-id="eea9b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eea9b-119">Header</span></span>|<span data-ttu-id="eea9b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eea9b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eea9b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="eea9b-121">Authorization</span></span>|<span data-ttu-id="eea9b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eea9b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eea9b-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eea9b-123">Accept</span></span>|<span data-ttu-id="eea9b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="eea9b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eea9b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eea9b-125">Request body</span></span>
<span data-ttu-id="eea9b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eea9b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eea9b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eea9b-127">Response</span></span>
<span data-ttu-id="eea9b-128">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eea9b-128">If successful, this function returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eea9b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eea9b-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="eea9b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eea9b-130">Request</span></span>
<span data-ttu-id="eea9b-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eea9b-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/autopilotDeviceStream
```

### <a name="response"></a><span data-ttu-id="eea9b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eea9b-132">Response</span></span>
<span data-ttu-id="eea9b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eea9b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 48

{
  "value": "Autopilot Device Stream value"
}
```



