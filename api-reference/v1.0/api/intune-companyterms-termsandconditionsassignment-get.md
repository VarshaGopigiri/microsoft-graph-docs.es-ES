---
title: Obtener termsAndConditionsAssignment
description: Lea las propiedades y las relaciones del objeto termsAndConditionsAssignment.
ms.openlocfilehash: ad1defe1403afad9ac30a3d056d198e4e116802c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028889"
---
# <a name="get-termsandconditionsassignment"></a><span data-ttu-id="2e55b-103">Obtener termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="2e55b-103">Get termsAndConditionsAssignment</span></span>

> <span data-ttu-id="2e55b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2e55b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2e55b-105">Lea las propiedades y las relaciones del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="2e55b-105">Read properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2e55b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2e55b-106">Prerequisites</span></span>
<span data-ttu-id="2e55b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2e55b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2e55b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e55b-109">Permission type</span></span>|<span data-ttu-id="2e55b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e55b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2e55b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e55b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2e55b-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="2e55b-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="2e55b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e55b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2e55b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e55b-114">Not supported.</span></span>|
|<span data-ttu-id="2e55b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e55b-115">Application</span></span>|<span data-ttu-id="2e55b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e55b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2e55b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e55b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2e55b-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2e55b-118">Optional query parameters</span></span>
<span data-ttu-id="2e55b-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e55b-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="2e55b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e55b-120">Request headers</span></span>
|<span data-ttu-id="2e55b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e55b-121">Header</span></span>|<span data-ttu-id="2e55b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2e55b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2e55b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2e55b-123">Authorization</span></span>|<span data-ttu-id="2e55b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2e55b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2e55b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2e55b-125">Accept</span></span>|<span data-ttu-id="2e55b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2e55b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2e55b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e55b-127">Request body</span></span>
<span data-ttu-id="2e55b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2e55b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2e55b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e55b-129">Response</span></span>
<span data-ttu-id="2e55b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e55b-130">If successful, this method returns a `200 OK` response code and [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e55b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e55b-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="2e55b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e55b-132">Request</span></span>
<span data-ttu-id="2e55b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e55b-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

### <a name="response"></a><span data-ttu-id="2e55b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e55b-134">Response</span></span>
<span data-ttu-id="2e55b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2e55b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 246

{
  "value": {
    "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
    "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
    "target": {
      "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
    }
  }
}
```



