---
title: Obtener deviceInstallState
description: Lea las propiedades y las relaciones del objeto deviceInstallState.
ms.openlocfilehash: c28e780e396f3ba60e79df58ff6343a50b81ff07
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029500"
---
# <a name="get-deviceinstallstate"></a><span data-ttu-id="937ee-103">Obtener deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="937ee-103">Get deviceInstallState</span></span>

> <span data-ttu-id="937ee-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="937ee-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="937ee-105">Lea las propiedades y las relaciones del objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="937ee-105">Read properties and relationships of the [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="937ee-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="937ee-106">Prerequisites</span></span>
<span data-ttu-id="937ee-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="937ee-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="937ee-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="937ee-109">Permission type</span></span>|<span data-ttu-id="937ee-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="937ee-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="937ee-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="937ee-111">Delegated (work or school account)</span></span>|<span data-ttu-id="937ee-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="937ee-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="937ee-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="937ee-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="937ee-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="937ee-114">Not supported.</span></span>|
|<span data-ttu-id="937ee-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="937ee-115">Application</span></span>|<span data-ttu-id="937ee-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="937ee-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="937ee-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="937ee-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
GET /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates/{deviceInstallStateId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="937ee-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="937ee-118">Optional query parameters</span></span>
<span data-ttu-id="937ee-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="937ee-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="937ee-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="937ee-120">Request headers</span></span>
|<span data-ttu-id="937ee-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="937ee-121">Header</span></span>|<span data-ttu-id="937ee-122">Valor</span><span class="sxs-lookup"><span data-stu-id="937ee-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="937ee-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="937ee-123">Authorization</span></span>|<span data-ttu-id="937ee-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="937ee-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="937ee-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="937ee-125">Accept</span></span>|<span data-ttu-id="937ee-126">application/json</span><span class="sxs-lookup"><span data-stu-id="937ee-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="937ee-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="937ee-127">Request body</span></span>
<span data-ttu-id="937ee-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="937ee-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="937ee-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="937ee-129">Response</span></span>
<span data-ttu-id="937ee-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="937ee-130">If successful, this method returns a `200 OK` response code and [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="937ee-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="937ee-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="937ee-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="937ee-132">Request</span></span>
<span data-ttu-id="937ee-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="937ee-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
```

### <a name="response"></a><span data-ttu-id="937ee-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="937ee-134">Response</span></span>
<span data-ttu-id="937ee-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="937ee-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 462

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceInstallState",
    "id": "b9feb68f-b68f-b9fe-8fb6-feb98fb6feb9",
    "deviceName": "Device Name value",
    "deviceId": "Device Id value",
    "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
    "installState": "installed",
    "errorCode": "Error Code value",
    "osVersion": "Os Version value",
    "osDescription": "Os Description value",
    "userName": "User Name value"
  }
}
```



