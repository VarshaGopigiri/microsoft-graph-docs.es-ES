---
title: Enumerar iosVppEBookAssignments
description: Enumere las propiedades y las relaciones de los objetos iosVppEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3ff81e17ae6a1ddc99788b879a0cfaf2d062801f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991275"
---
# <a name="list-iosvppebookassignments"></a><span data-ttu-id="63c5c-103">Enumerar iosVppEBookAssignments</span><span class="sxs-lookup"><span data-stu-id="63c5c-103">List iosVppEBookAssignments</span></span>

> <span data-ttu-id="63c5c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63c5c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63c5c-105">Enumere las propiedades y las relaciones de los objetos [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="63c5c-105">List properties and relationships of the [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63c5c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63c5c-106">Prerequisites</span></span>
<span data-ttu-id="63c5c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63c5c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63c5c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63c5c-109">Permission type</span></span>|<span data-ttu-id="63c5c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63c5c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63c5c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63c5c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="63c5c-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="63c5c-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="63c5c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63c5c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63c5c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63c5c-114">Not supported.</span></span>|
|<span data-ttu-id="63c5c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63c5c-115">Application</span></span>|<span data-ttu-id="63c5c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63c5c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63c5c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63c5c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="63c5c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63c5c-118">Request headers</span></span>
|<span data-ttu-id="63c5c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63c5c-119">Header</span></span>|<span data-ttu-id="63c5c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="63c5c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63c5c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="63c5c-121">Authorization</span></span>|<span data-ttu-id="63c5c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63c5c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63c5c-123">Accept</span><span class="sxs-lookup"><span data-stu-id="63c5c-123">Accept</span></span>|<span data-ttu-id="63c5c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="63c5c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63c5c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63c5c-125">Request body</span></span>
<span data-ttu-id="63c5c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="63c5c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="63c5c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63c5c-127">Response</span></span>
<span data-ttu-id="63c5c-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63c5c-128">If successful, this method returns a `200 OK` response code and a collection of [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63c5c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63c5c-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="63c5c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63c5c-130">Request</span></span>
<span data-ttu-id="63c5c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63c5c-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

### <a name="response"></a><span data-ttu-id="63c5c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63c5c-132">Response</span></span>
<span data-ttu-id="63c5c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63c5c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 299

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
      "id": "48f05789-5789-48f0-8957-f0488957f048",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      },
      "installIntent": "required"
    }
  ]
}
```



