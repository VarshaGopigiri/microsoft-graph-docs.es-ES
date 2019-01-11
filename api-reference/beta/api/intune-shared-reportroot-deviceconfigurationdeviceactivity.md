---
title: Función deviceConfigurationDeviceActivity
description: Metadatos para el informe de actividad de dispositivo de configuración de dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ef5a8367ec47242138cdf13cb30447c844bd050e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831761"
---
# <a name="deviceconfigurationdeviceactivity-function"></a><span data-ttu-id="d9e13-103">Función deviceConfigurationDeviceActivity</span><span class="sxs-lookup"><span data-stu-id="d9e13-103">deviceConfigurationDeviceActivity function</span></span>

> <span data-ttu-id="d9e13-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9e13-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9e13-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9e13-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d9e13-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d9e13-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d9e13-107">Metadatos para el informe de actividad de dispositivo de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9e13-107">Metadata for the device configuration device activity report</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d9e13-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d9e13-108">Prerequisites</span></span>
<span data-ttu-id="d9e13-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d9e13-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d9e13-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d9e13-111">Permission type</span></span>|<span data-ttu-id="d9e13-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d9e13-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d9e13-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9e13-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="d9e13-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="d9e13-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="d9e13-115">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="d9e13-115">DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="d9e13-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9e13-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d9e13-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9e13-117">Not supported.</span></span>|
|<span data-ttu-id="d9e13-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9e13-118">Application</span></span>|<span data-ttu-id="d9e13-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9e13-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d9e13-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9e13-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/deviceConfigurationDeviceActivity
```

## <a name="request-headers"></a><span data-ttu-id="d9e13-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9e13-121">Request headers</span></span>
|<span data-ttu-id="d9e13-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9e13-122">Header</span></span>|<span data-ttu-id="d9e13-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e13-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d9e13-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="d9e13-124">Authorization</span></span>|<span data-ttu-id="d9e13-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d9e13-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d9e13-126">Accept</span><span class="sxs-lookup"><span data-stu-id="d9e13-126">Accept</span></span>|<span data-ttu-id="d9e13-127">application/json</span><span class="sxs-lookup"><span data-stu-id="d9e13-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d9e13-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9e13-128">Request body</span></span>
<span data-ttu-id="d9e13-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d9e13-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d9e13-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9e13-130">Response</span></span>
<span data-ttu-id="d9e13-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9e13-131">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9e13-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9e13-132">Example</span></span>
### <a name="request"></a><span data-ttu-id="d9e13-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9e13-133">Request</span></span>
<span data-ttu-id="d9e13-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9e13-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports/deviceConfigurationDeviceActivity
```

### <a name="response"></a><span data-ttu-id="d9e13-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9e13-135">Response</span></span>
<span data-ttu-id="d9e13-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d9e13-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



