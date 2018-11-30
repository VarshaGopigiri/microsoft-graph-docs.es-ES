---
title: Obtener iosVppEBookAssignment
description: Lea las propiedades y las relaciones del objeto iosVppEBookAssignment.
ms.openlocfilehash: e66627a0602e86d5cc4ad5820e019658195dd6e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030562"
---
# <a name="get-iosvppebookassignment"></a><span data-ttu-id="8763b-103">Obtener iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="8763b-103">Get iosVppEBookAssignment</span></span>

> <span data-ttu-id="8763b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8763b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8763b-105">Lea las propiedades y las relaciones del objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="8763b-105">Read properties and relationships of the [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8763b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8763b-106">Prerequisites</span></span>
<span data-ttu-id="8763b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8763b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8763b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8763b-109">Permission type</span></span>|<span data-ttu-id="8763b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8763b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8763b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8763b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8763b-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="8763b-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="8763b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8763b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8763b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8763b-114">Not supported.</span></span>|
|<span data-ttu-id="8763b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8763b-115">Application</span></span>|<span data-ttu-id="8763b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8763b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8763b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8763b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8763b-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8763b-118">Optional query parameters</span></span>
<span data-ttu-id="8763b-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8763b-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="8763b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8763b-120">Request headers</span></span>
|<span data-ttu-id="8763b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8763b-121">Header</span></span>|<span data-ttu-id="8763b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8763b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8763b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8763b-123">Authorization</span></span>|<span data-ttu-id="8763b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8763b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8763b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8763b-125">Accept</span></span>|<span data-ttu-id="8763b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8763b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8763b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8763b-127">Request body</span></span>
<span data-ttu-id="8763b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8763b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8763b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8763b-129">Response</span></span>
<span data-ttu-id="8763b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8763b-130">If successful, this method returns a `200 OK` response code and [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8763b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8763b-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="8763b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8763b-132">Request</span></span>
<span data-ttu-id="8763b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8763b-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

### <a name="response"></a><span data-ttu-id="8763b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8763b-134">Response</span></span>
<span data-ttu-id="8763b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8763b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 273

{
  "value": {
    "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
    "id": "48f05789-5789-48f0-8957-f0488957f048",
    "target": {
      "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
    },
    "installIntent": "required"
  }
}
```


