---
title: Obtener deviceAppManagement
description: Lea las propiedades y las relaciones del objeto deviceAppManagement.
ms.openlocfilehash: 02ccc2ab618187824ca69fb536f0a73b922ef1d7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029859"
---
# <a name="get-deviceappmanagement"></a><span data-ttu-id="b5b7a-103">Obtener deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="b5b7a-103">Get deviceAppManagement</span></span>

> <span data-ttu-id="b5b7a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b5b7a-105">Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="b5b7a-105">Read properties and relationships of the [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5b7a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b5b7a-106">Prerequisites</span></span>

<span data-ttu-id="b5b7a-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="b5b7a-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b5b7a-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="b5b7a-109">Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-109">Note that the appropriate permission varies according to the workflow.</span></span>

|<span data-ttu-id="b5b7a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5b7a-110">Permission type</span></span>|<span data-ttu-id="b5b7a-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5b7a-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b5b7a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5b7a-112">Delegated (work or school account)</span></span>|<span data-ttu-id="b5b7a-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b5b7a-113">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
|<span data-ttu-id="b5b7a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5b7a-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b5b7a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-115">Not supported.</span></span>|
|<span data-ttu-id="b5b7a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5b7a-116">Application</span></span>|<span data-ttu-id="b5b7a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b5b7a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5b7a-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b5b7a-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b5b7a-119">Optional query parameters</span></span>
<span data-ttu-id="b5b7a-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b5b7a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5b7a-121">Request headers</span></span>
|<span data-ttu-id="b5b7a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5b7a-122">Header</span></span>|<span data-ttu-id="b5b7a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b5b7a-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b5b7a-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5b7a-124">Authorization</span></span>|<span data-ttu-id="b5b7a-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b5b7a-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b5b7a-126">Accept</span></span>|<span data-ttu-id="b5b7a-127">application/json</span><span class="sxs-lookup"><span data-stu-id="b5b7a-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b5b7a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5b7a-128">Request body</span></span>
<span data-ttu-id="b5b7a-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b5b7a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5b7a-130">Response</span></span>
<span data-ttu-id="b5b7a-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-131">If successful, this method returns a `200 OK` response code and [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object in the response body.</span></span>

## <a name="example-request"></a><span data-ttu-id="b5b7a-132">Ejemplo de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5b7a-132">Example request</span></span>

``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement
```

## <a name="example-response"></a><span data-ttu-id="b5b7a-133">Respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5b7a-133">Example response</span></span>
<span data-ttu-id="b5b7a-134">El objeto de respuesta que se muestra aquí es posible que esté truncado por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-134">The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="b5b7a-135">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5b7a-135">All properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 133

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAppManagement",
    "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
  }
}
```



