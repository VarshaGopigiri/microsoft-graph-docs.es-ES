---
title: Función deviceConfigurationDeviceActivity
description: Metadatos para el informe de actividad de dispositivo de configuración de dispositivo
ms.openlocfilehash: 43b1844b5fd562553114bcaa8e0652b1105c7f69
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030943"
---
# <a name="deviceconfigurationdeviceactivity-function"></a><span data-ttu-id="8b00a-103">Función deviceConfigurationDeviceActivity</span><span class="sxs-lookup"><span data-stu-id="8b00a-103">deviceConfigurationDeviceActivity function</span></span>

> <span data-ttu-id="8b00a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8b00a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8b00a-105">Metadatos para el informe de actividad de dispositivo de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8b00a-105">Metadata for the device configuration device activity report</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8b00a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8b00a-106">Prerequisites</span></span>
<span data-ttu-id="8b00a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8b00a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8b00a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8b00a-109">Permission type</span></span>|<span data-ttu-id="8b00a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8b00a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8b00a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8b00a-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8b00a-112">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8b00a-112">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="8b00a-113">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="8b00a-113">DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="8b00a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8b00a-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8b00a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b00a-115">Not supported.</span></span>|
|<span data-ttu-id="8b00a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8b00a-116">Application</span></span>|<span data-ttu-id="8b00a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8b00a-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8b00a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8b00a-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/deviceConfigurationDeviceActivity
```

## <a name="request-headers"></a><span data-ttu-id="8b00a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8b00a-119">Request headers</span></span>
|<span data-ttu-id="8b00a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b00a-120">Header</span></span>|<span data-ttu-id="8b00a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8b00a-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8b00a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="8b00a-122">Authorization</span></span>|<span data-ttu-id="8b00a-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8b00a-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8b00a-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8b00a-124">Accept</span></span>|<span data-ttu-id="8b00a-125">application/json</span><span class="sxs-lookup"><span data-stu-id="8b00a-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8b00a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8b00a-126">Request body</span></span>
<span data-ttu-id="8b00a-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8b00a-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8b00a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b00a-128">Response</span></span>
<span data-ttu-id="8b00a-129">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b00a-129">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8b00a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8b00a-130">Example</span></span>
### <a name="request"></a><span data-ttu-id="8b00a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8b00a-131">Request</span></span>
<span data-ttu-id="8b00a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8b00a-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/reports/deviceConfigurationDeviceActivity
```

### <a name="response"></a><span data-ttu-id="8b00a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b00a-133">Response</span></span>
<span data-ttu-id="8b00a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8b00a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








