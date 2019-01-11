---
title: Enumerar managedEBookAssignments
description: Enumere las propiedades y las relaciones de los objetos managedEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 141d01a21a09f0706f5689cae527db072b9fb6a8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825406"
---
# <a name="list-managedebookassignments"></a><span data-ttu-id="2efe9-103">Enumerar managedEBookAssignments</span><span class="sxs-lookup"><span data-stu-id="2efe9-103">List managedEBookAssignments</span></span>

> <span data-ttu-id="2efe9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2efe9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2efe9-105">Enumere las propiedades y las relaciones de los objetos [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="2efe9-105">List properties and relationships of the [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2efe9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2efe9-106">Prerequisites</span></span>
<span data-ttu-id="2efe9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2efe9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2efe9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2efe9-109">Permission type</span></span>|<span data-ttu-id="2efe9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2efe9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2efe9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2efe9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2efe9-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="2efe9-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="2efe9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2efe9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2efe9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2efe9-114">Not supported.</span></span>|
|<span data-ttu-id="2efe9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2efe9-115">Application</span></span>|<span data-ttu-id="2efe9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2efe9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2efe9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2efe9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="2efe9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2efe9-118">Request headers</span></span>
|<span data-ttu-id="2efe9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2efe9-119">Header</span></span>|<span data-ttu-id="2efe9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2efe9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2efe9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2efe9-121">Authorization</span></span>|<span data-ttu-id="2efe9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2efe9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2efe9-123">Accept</span><span class="sxs-lookup"><span data-stu-id="2efe9-123">Accept</span></span>|<span data-ttu-id="2efe9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2efe9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2efe9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2efe9-125">Request body</span></span>
<span data-ttu-id="2efe9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2efe9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2efe9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2efe9-127">Response</span></span>
<span data-ttu-id="2efe9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2efe9-128">If successful, this method returns a `200 OK` response code and a collection of [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2efe9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2efe9-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="2efe9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2efe9-130">Request</span></span>
<span data-ttu-id="2efe9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2efe9-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

### <a name="response"></a><span data-ttu-id="2efe9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2efe9-132">Response</span></span>
<span data-ttu-id="2efe9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2efe9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



