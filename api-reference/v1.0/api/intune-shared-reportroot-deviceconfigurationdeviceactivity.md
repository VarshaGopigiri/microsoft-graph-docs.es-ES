---
title: Función deviceConfigurationDeviceActivity
description: Metadatos para el informe de actividad de dispositivo de configuración de dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4de84b71ba5d2e900d54c02fba965fd28e07c00a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925528"
---
# <a name="deviceconfigurationdeviceactivity-function"></a><span data-ttu-id="9551f-103">Función deviceConfigurationDeviceActivity</span><span class="sxs-lookup"><span data-stu-id="9551f-103">deviceConfigurationDeviceActivity function</span></span>

> <span data-ttu-id="9551f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9551f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9551f-105">Metadatos para el informe de actividad de dispositivo de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9551f-105">Metadata for the device configuration device activity report</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9551f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9551f-106">Prerequisites</span></span>
<span data-ttu-id="9551f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9551f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9551f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9551f-109">Permission type</span></span>|<span data-ttu-id="9551f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9551f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9551f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9551f-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="9551f-112">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9551f-112">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="9551f-113">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9551f-113">DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9551f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9551f-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9551f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9551f-115">Not supported.</span></span>|
|<span data-ttu-id="9551f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9551f-116">Application</span></span>|<span data-ttu-id="9551f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9551f-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9551f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9551f-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/deviceConfigurationDeviceActivity
```

## <a name="request-headers"></a><span data-ttu-id="9551f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9551f-119">Request headers</span></span>
|<span data-ttu-id="9551f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9551f-120">Header</span></span>|<span data-ttu-id="9551f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9551f-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9551f-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="9551f-122">Authorization</span></span>|<span data-ttu-id="9551f-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9551f-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9551f-124">Accept</span><span class="sxs-lookup"><span data-stu-id="9551f-124">Accept</span></span>|<span data-ttu-id="9551f-125">application/json</span><span class="sxs-lookup"><span data-stu-id="9551f-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9551f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9551f-126">Request body</span></span>
<span data-ttu-id="9551f-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9551f-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9551f-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9551f-128">Response</span></span>
<span data-ttu-id="9551f-129">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9551f-129">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9551f-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9551f-130">Example</span></span>
### <a name="request"></a><span data-ttu-id="9551f-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9551f-131">Request</span></span>
<span data-ttu-id="9551f-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9551f-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/reports/deviceConfigurationDeviceActivity
```

### <a name="response"></a><span data-ttu-id="9551f-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9551f-133">Response</span></span>
<span data-ttu-id="9551f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9551f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 123

{
  "value": {
    "@odata.type": "microsoft.graph.report",
    "content": "<Unknown Primitive Type Edm.Stream>"
  }
}
```








