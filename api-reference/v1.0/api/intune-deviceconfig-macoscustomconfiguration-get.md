---
title: Obtener macOSCustomConfiguration
description: Lea las propiedades y las relaciones del objeto macOSCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 87f1243a6c859e0510aa29d9cca9748de57e3828
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968865"
---
# <a name="get-macoscustomconfiguration"></a><span data-ttu-id="680a8-103">Obtener macOSCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="680a8-103">Get macOSCustomConfiguration</span></span>

> <span data-ttu-id="680a8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="680a8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="680a8-105">Lea las propiedades y las relaciones del objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="680a8-105">Read properties and relationships of the [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="680a8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="680a8-106">Prerequisites</span></span>
<span data-ttu-id="680a8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="680a8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="680a8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="680a8-109">Permission type</span></span>|<span data-ttu-id="680a8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="680a8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="680a8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="680a8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="680a8-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="680a8-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="680a8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="680a8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="680a8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="680a8-114">Not supported.</span></span>|
|<span data-ttu-id="680a8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="680a8-115">Application</span></span>|<span data-ttu-id="680a8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="680a8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="680a8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="680a8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="680a8-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="680a8-118">Optional query parameters</span></span>
<span data-ttu-id="680a8-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="680a8-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="680a8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="680a8-120">Request headers</span></span>
|<span data-ttu-id="680a8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="680a8-121">Header</span></span>|<span data-ttu-id="680a8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="680a8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="680a8-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="680a8-123">Authorization</span></span>|<span data-ttu-id="680a8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="680a8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="680a8-125">Accept</span><span class="sxs-lookup"><span data-stu-id="680a8-125">Accept</span></span>|<span data-ttu-id="680a8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="680a8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="680a8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="680a8-127">Request body</span></span>
<span data-ttu-id="680a8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="680a8-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="680a8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="680a8-129">Response</span></span>
<span data-ttu-id="680a8-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="680a8-130">If successful, this method returns a `200 OK` response code and [macOSCustomConfiguration](../resources/intune-deviceconfig-macoscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="680a8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="680a8-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="680a8-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="680a8-132">Request</span></span>
<span data-ttu-id="680a8-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="680a8-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="680a8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="680a8-134">Response</span></span>
<span data-ttu-id="680a8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="680a8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 492

{
  "value": {
    "@odata.type": "#microsoft.graph.macOSCustomConfiguration",
    "id": "a253835d-835d-a253-5d83-53a25d8353a2",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "payloadName": "Payload Name value",
    "payloadFileName": "Payload File Name value",
    "payload": "cGF5bG9hZA=="
  }
}
```



