---
title: Obtener deviceConfigurationAssignment
description: Lea las propiedades y las relaciones del objeto deviceConfigurationAssignment.
ms.openlocfilehash: 231d58fc4988e37ae02cc6efa599481aa490c4e5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030735"
---
# <a name="get-deviceconfigurationassignment"></a><span data-ttu-id="bf394-103">Obtener deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="bf394-103">Get deviceConfigurationAssignment</span></span>

> <span data-ttu-id="bf394-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf394-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf394-105">Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bf394-105">Read properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bf394-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf394-106">Prerequisites</span></span>
<span data-ttu-id="bf394-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf394-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf394-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf394-109">Permission type</span></span>|<span data-ttu-id="bf394-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf394-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bf394-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf394-111">Delegated (work or school account)</span></span>|<span data-ttu-id="bf394-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="bf394-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="bf394-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf394-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bf394-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf394-114">Not supported.</span></span>|
|<span data-ttu-id="bf394-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf394-115">Application</span></span>|<span data-ttu-id="bf394-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf394-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bf394-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf394-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bf394-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bf394-118">Optional query parameters</span></span>
<span data-ttu-id="bf394-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf394-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bf394-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf394-120">Request headers</span></span>
|<span data-ttu-id="bf394-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf394-121">Header</span></span>|<span data-ttu-id="bf394-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bf394-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bf394-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bf394-123">Authorization</span></span>|<span data-ttu-id="bf394-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bf394-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bf394-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bf394-125">Accept</span></span>|<span data-ttu-id="bf394-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bf394-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bf394-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf394-127">Request body</span></span>
<span data-ttu-id="bf394-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bf394-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bf394-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf394-129">Response</span></span>
<span data-ttu-id="bf394-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf394-130">If successful, this method returns a `200 OK` response code and [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf394-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf394-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="bf394-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf394-132">Request</span></span>
<span data-ttu-id="bf394-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf394-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignments/{deviceConfigurationAssignmentId}
```

### <a name="response"></a><span data-ttu-id="bf394-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf394-134">Response</span></span>
<span data-ttu-id="bf394-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf394-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 247

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
    "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
    "target": {
      "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
    }
  }
}
```



