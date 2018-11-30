---
title: Enumerar managedEBookAssignments
description: Enumere las propiedades y las relaciones de los objetos managedEBookAssignment.
ms.openlocfilehash: ed6ccb04f351b05718c99dc31e7f7d0c53a5f908
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029130"
---
# <a name="list-managedebookassignments"></a><span data-ttu-id="2bebc-103">Enumerar managedEBookAssignments</span><span class="sxs-lookup"><span data-stu-id="2bebc-103">List managedEBookAssignments</span></span>

> <span data-ttu-id="2bebc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2bebc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2bebc-105">Enumere las propiedades y las relaciones de los objetos [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="2bebc-105">List properties and relationships of the [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2bebc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2bebc-106">Prerequisites</span></span>
<span data-ttu-id="2bebc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2bebc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2bebc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bebc-109">Permission type</span></span>|<span data-ttu-id="2bebc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bebc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2bebc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bebc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2bebc-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="2bebc-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="2bebc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bebc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2bebc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bebc-114">Not supported.</span></span>|
|<span data-ttu-id="2bebc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bebc-115">Application</span></span>|<span data-ttu-id="2bebc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bebc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2bebc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bebc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="2bebc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bebc-118">Request headers</span></span>
|<span data-ttu-id="2bebc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bebc-119">Header</span></span>|<span data-ttu-id="2bebc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2bebc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2bebc-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bebc-121">Authorization</span></span>|<span data-ttu-id="2bebc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2bebc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2bebc-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2bebc-123">Accept</span></span>|<span data-ttu-id="2bebc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2bebc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2bebc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bebc-125">Request body</span></span>
<span data-ttu-id="2bebc-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2bebc-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2bebc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bebc-127">Response</span></span>
<span data-ttu-id="2bebc-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bebc-128">If successful, this method returns a `200 OK` response code and a collection of [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2bebc-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bebc-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="2bebc-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bebc-130">Request</span></span>
<span data-ttu-id="2bebc-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bebc-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

### <a name="response"></a><span data-ttu-id="2bebc-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bebc-132">Response</span></span>
<span data-ttu-id="2bebc-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2bebc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 300

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedEBookAssignment",
      "id": "ae8b0d27-0d27-ae8b-270d-8bae270d8bae",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      },
      "installIntent": "required"
    }
  ]
}
```



