---
title: Obtener reportRoot
description: Lea las propiedades y las relaciones del objeto reportRoot.
ms.openlocfilehash: 681c378977a8439d4876e4a650d1d9cea6d91f60
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088719"
---
# <a name="get-reportroot"></a><span data-ttu-id="c52b0-103">Obtener reportRoot</span><span class="sxs-lookup"><span data-stu-id="c52b0-103">Get reportRoot</span></span>

> <span data-ttu-id="c52b0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c52b0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c52b0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c52b0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c52b0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c52b0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c52b0-107">Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune-shared-reportroot.md).</span><span class="sxs-lookup"><span data-stu-id="c52b0-107">Read properties and relationships of the [reportRoot](../resources/intune-shared-reportroot.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c52b0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c52b0-108">Prerequisites</span></span>
<span data-ttu-id="c52b0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c52b0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c52b0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c52b0-111">Permission type</span></span>|<span data-ttu-id="c52b0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c52b0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c52b0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c52b0-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="c52b0-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="c52b0-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="c52b0-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c52b0-115">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
| <span data-ttu-id="c52b0-116">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="c52b0-116">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="c52b0-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="c52b0-117">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="c52b0-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c52b0-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c52b0-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c52b0-119">Not supported.</span></span>|
|<span data-ttu-id="c52b0-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c52b0-120">Application</span></span>|<span data-ttu-id="c52b0-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c52b0-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c52b0-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c52b0-122">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c52b0-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c52b0-123">Optional query parameters</span></span>
<span data-ttu-id="c52b0-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c52b0-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c52b0-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c52b0-125">Request headers</span></span>
|<span data-ttu-id="c52b0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c52b0-126">Header</span></span>|<span data-ttu-id="c52b0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c52b0-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c52b0-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="c52b0-128">Authorization</span></span>|<span data-ttu-id="c52b0-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c52b0-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c52b0-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c52b0-130">Accept</span></span>|<span data-ttu-id="c52b0-131">application/json</span><span class="sxs-lookup"><span data-stu-id="c52b0-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c52b0-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c52b0-132">Request body</span></span>
<span data-ttu-id="c52b0-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c52b0-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c52b0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c52b0-134">Response</span></span>
<span data-ttu-id="c52b0-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [reportRoot](../resources/intune-shared-reportroot.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c52b0-135">If successful, this method returns a `200 OK` response code and [reportRoot](../resources/intune-shared-reportroot.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c52b0-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c52b0-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="c52b0-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c52b0-137">Request</span></span>
<span data-ttu-id="c52b0-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c52b0-138">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/reports
```

### <a name="response"></a><span data-ttu-id="c52b0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c52b0-139">Response</span></span>
<span data-ttu-id="c52b0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c52b0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



