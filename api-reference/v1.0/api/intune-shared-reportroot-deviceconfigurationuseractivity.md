---
title: Función deviceConfigurationUserActivity
description: Metadatos para el informe de actividad de usuario de configuración de dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d2ecafdc399eab5150b80d83a68bdb6086dfa486
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849080"
---
# <a name="deviceconfigurationuseractivity-function"></a><span data-ttu-id="dc013-103">Función deviceConfigurationUserActivity</span><span class="sxs-lookup"><span data-stu-id="dc013-103">deviceConfigurationUserActivity function</span></span>

> <span data-ttu-id="dc013-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dc013-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dc013-105">Metadatos para el informe de actividad de usuario de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc013-105">Metadata for the device configuration user activity report</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dc013-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dc013-106">Prerequisites</span></span>
<span data-ttu-id="dc013-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc013-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc013-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc013-109">Permission type</span></span>|<span data-ttu-id="dc013-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc013-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dc013-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc013-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="dc013-112">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="dc013-112">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="dc013-113">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="dc013-113">DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="dc013-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc013-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dc013-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc013-115">Not supported.</span></span>|
|<span data-ttu-id="dc013-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc013-116">Application</span></span>|<span data-ttu-id="dc013-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc013-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dc013-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc013-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/deviceConfigurationUserActivity
```

## <a name="request-headers"></a><span data-ttu-id="dc013-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc013-119">Request headers</span></span>
|<span data-ttu-id="dc013-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc013-120">Header</span></span>|<span data-ttu-id="dc013-121">Valor</span><span class="sxs-lookup"><span data-stu-id="dc013-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dc013-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="dc013-122">Authorization</span></span>|<span data-ttu-id="dc013-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dc013-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dc013-124">Accept</span><span class="sxs-lookup"><span data-stu-id="dc013-124">Accept</span></span>|<span data-ttu-id="dc013-125">application/json</span><span class="sxs-lookup"><span data-stu-id="dc013-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dc013-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc013-126">Request body</span></span>
<span data-ttu-id="dc013-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dc013-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dc013-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc013-128">Response</span></span>
<span data-ttu-id="dc013-129">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune-shared-report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc013-129">If successful, this function returns a `200 OK` response code and a [report](../resources/intune-shared-report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dc013-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc013-130">Example</span></span>
### <a name="request"></a><span data-ttu-id="dc013-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc013-131">Request</span></span>
<span data-ttu-id="dc013-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc013-132">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/reports/deviceConfigurationUserActivity
```

### <a name="response"></a><span data-ttu-id="dc013-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc013-133">Response</span></span>
<span data-ttu-id="dc013-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc013-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








