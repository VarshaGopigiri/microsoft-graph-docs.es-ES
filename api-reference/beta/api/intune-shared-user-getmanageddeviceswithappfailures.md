---
title: getManagedDevicesWithAppFailures (función)
description: Recupera la lista de dispositivos con aplicaciones con errores
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: cafda91617bfd183606877bfda352370f2364c9f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890072"
---
# <a name="getmanageddeviceswithappfailures-function"></a><span data-ttu-id="69cbd-103">getManagedDevicesWithAppFailures (función)</span><span class="sxs-lookup"><span data-stu-id="69cbd-103">getManagedDevicesWithAppFailures function</span></span>

> <span data-ttu-id="69cbd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="69cbd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="69cbd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="69cbd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="69cbd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="69cbd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="69cbd-107">Recupera la lista de dispositivos con aplicaciones con errores</span><span class="sxs-lookup"><span data-stu-id="69cbd-107">Retrieves the list of devices with failed apps</span></span>
## <a name="prerequisites"></a><span data-ttu-id="69cbd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="69cbd-108">Prerequisites</span></span>
<span data-ttu-id="69cbd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69cbd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69cbd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69cbd-111">Permission type</span></span>|<span data-ttu-id="69cbd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69cbd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="69cbd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69cbd-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="69cbd-114">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="69cbd-114">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="69cbd-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="69cbd-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="69cbd-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69cbd-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="69cbd-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69cbd-117">Not supported.</span></span>|
|<span data-ttu-id="69cbd-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69cbd-118">Application</span></span>|<span data-ttu-id="69cbd-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69cbd-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="69cbd-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69cbd-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedDevicesWithAppFailures
```

## <a name="request-headers"></a><span data-ttu-id="69cbd-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69cbd-121">Request headers</span></span>
|<span data-ttu-id="69cbd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69cbd-122">Header</span></span>|<span data-ttu-id="69cbd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="69cbd-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="69cbd-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="69cbd-124">Authorization</span></span>|<span data-ttu-id="69cbd-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="69cbd-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="69cbd-126">Accept</span><span class="sxs-lookup"><span data-stu-id="69cbd-126">Accept</span></span>|<span data-ttu-id="69cbd-127">application/json</span><span class="sxs-lookup"><span data-stu-id="69cbd-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="69cbd-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69cbd-128">Request body</span></span>
<span data-ttu-id="69cbd-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="69cbd-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="69cbd-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69cbd-130">Response</span></span>
<span data-ttu-id="69cbd-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69cbd-131">If successful, this function returns a `200 OK` response code and a String collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69cbd-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69cbd-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="69cbd-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69cbd-133">Request</span></span>
<span data-ttu-id="69cbd-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69cbd-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/getManagedDevicesWithAppFailures
```

### <a name="response"></a><span data-ttu-id="69cbd-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69cbd-135">Response</span></span>
<span data-ttu-id="69cbd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69cbd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 74

{
  "value": [
    "Get Managed Devices With App Failures value"
  ]
}
```





