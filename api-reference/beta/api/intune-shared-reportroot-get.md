---
title: Obtener reportRoot
description: Lea las propiedades y las relaciones del objeto reportRoot.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3ae57e5bd5638e41ab6c6acfda810fe64d04a461
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954249"
---
# <a name="get-reportroot"></a><span data-ttu-id="26894-103">Obtener reportRoot</span><span class="sxs-lookup"><span data-stu-id="26894-103">Get reportRoot</span></span>

> <span data-ttu-id="26894-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26894-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26894-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26894-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="26894-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26894-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26894-107">Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="26894-107">Read properties and relationships of the [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="26894-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="26894-108">Prerequisites</span></span>
<span data-ttu-id="26894-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="26894-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="26894-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26894-111">Permission type</span></span>|<span data-ttu-id="26894-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26894-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="26894-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26894-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="26894-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="26894-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="26894-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="26894-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
| <span data-ttu-id="26894-116">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="26894-116">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="26894-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="26894-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="26894-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26894-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="26894-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26894-119">Not supported.</span></span>|
|<span data-ttu-id="26894-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26894-120">Application</span></span>|<span data-ttu-id="26894-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26894-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="26894-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26894-122">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports
```

## <a name="optional-query-parameters"></a><span data-ttu-id="26894-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="26894-123">Optional query parameters</span></span>
<span data-ttu-id="26894-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26894-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="26894-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="26894-125">Request headers</span></span>
|<span data-ttu-id="26894-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26894-126">Header</span></span>|<span data-ttu-id="26894-127">Valor</span><span class="sxs-lookup"><span data-stu-id="26894-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="26894-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="26894-128">Authorization</span></span>|<span data-ttu-id="26894-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="26894-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="26894-130">Accept</span><span class="sxs-lookup"><span data-stu-id="26894-130">Accept</span></span>|<span data-ttu-id="26894-131">application/json</span><span class="sxs-lookup"><span data-stu-id="26894-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="26894-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26894-132">Request body</span></span>
<span data-ttu-id="26894-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="26894-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="26894-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26894-134">Response</span></span>
<span data-ttu-id="26894-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [reportRoot](../resources/intune-shared-reportroot.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26894-135">If successful, this method returns a `200 OK` response code and [reportRoot](../resources/intune-shared-reportroot.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="26894-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26894-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="26894-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="26894-137">Request</span></span>
<span data-ttu-id="26894-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26894-138">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports
```

### <a name="response"></a><span data-ttu-id="26894-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26894-139">Response</span></span>
<span data-ttu-id="26894-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="26894-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 124

{
  "value": {
    "@odata.type": "#microsoft.graph.reportRoot",
    "id": "9ab6b3dd-b3dd-9ab6-ddb3-b69addb3b69a"
  }
}
```



