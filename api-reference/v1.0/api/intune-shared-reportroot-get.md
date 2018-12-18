---
title: Obtener reportRoot
description: Lea las propiedades y las relaciones del objeto reportRoot.
author: tfitzmac
ms.openlocfilehash: aa79d3bbc03529c20e0ea66b91c89a92f7782b2d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339413"
---
# <a name="get-reportroot"></a><span data-ttu-id="6ef34-103">Obtener reportRoot</span><span class="sxs-lookup"><span data-stu-id="6ef34-103">Get reportRoot</span></span>

> <span data-ttu-id="6ef34-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ef34-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ef34-105">Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="6ef34-105">Read properties and relationships of the [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ef34-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ef34-106">Prerequisites</span></span>
<span data-ttu-id="6ef34-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ef34-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ef34-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ef34-109">Permission type</span></span>|<span data-ttu-id="6ef34-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ef34-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ef34-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ef34-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="6ef34-112">&nbsp;&nbsp; Configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6ef34-112">&nbsp; &nbsp; Device configuration</span></span> | <span data-ttu-id="6ef34-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="6ef34-113">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
| <span data-ttu-id="6ef34-114">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="6ef34-114">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="6ef34-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="6ef34-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="6ef34-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ef34-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ef34-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ef34-117">Not supported.</span></span>|
|<span data-ttu-id="6ef34-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ef34-118">Application</span></span>|<span data-ttu-id="6ef34-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ef34-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ef34-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ef34-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6ef34-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6ef34-121">Optional query parameters</span></span>
<span data-ttu-id="6ef34-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ef34-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6ef34-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ef34-123">Request headers</span></span>
|<span data-ttu-id="6ef34-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ef34-124">Header</span></span>|<span data-ttu-id="6ef34-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6ef34-125">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ef34-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ef34-126">Authorization</span></span>|<span data-ttu-id="6ef34-127">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ef34-127">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ef34-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6ef34-128">Accept</span></span>|<span data-ttu-id="6ef34-129">application/json</span><span class="sxs-lookup"><span data-stu-id="6ef34-129">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ef34-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ef34-130">Request body</span></span>
<span data-ttu-id="6ef34-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6ef34-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6ef34-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ef34-132">Response</span></span>
<span data-ttu-id="6ef34-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [reportRoot](../resources/intune-shared-reportroot.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ef34-133">If successful, this method returns a `200 OK` response code and [reportRoot](../resources/intune-shared-reportroot.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ef34-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ef34-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ef34-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ef34-135">Request</span></span>
<span data-ttu-id="6ef34-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ef34-136">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/reports
```

### <a name="response"></a><span data-ttu-id="6ef34-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ef34-137">Response</span></span>
<span data-ttu-id="6ef34-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ef34-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








