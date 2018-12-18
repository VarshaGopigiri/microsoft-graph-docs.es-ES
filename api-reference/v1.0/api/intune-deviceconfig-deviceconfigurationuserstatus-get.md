---
title: Obtener deviceConfigurationUserStatus
description: Lea las propiedades y las relaciones del objeto deviceConfigurationUserStatus.
author: tfitzmac
ms.openlocfilehash: 19ae9c0abcae8a46d252bd6b09eeee2e7338a4c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304063"
---
# <a name="get-deviceconfigurationuserstatus"></a><span data-ttu-id="9b948-103">Obtener deviceConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="9b948-103">Get deviceConfigurationUserStatus</span></span>

> <span data-ttu-id="9b948-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b948-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b948-105">Lea las propiedades y las relaciones del objeto [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9b948-105">Read properties and relationships of the [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b948-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b948-106">Prerequisites</span></span>
<span data-ttu-id="9b948-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b948-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b948-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b948-109">Permission type</span></span>|<span data-ttu-id="9b948-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b948-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b948-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b948-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9b948-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9b948-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9b948-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b948-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b948-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b948-114">Not supported.</span></span>|
|<span data-ttu-id="9b948-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b948-115">Application</span></span>|<span data-ttu-id="9b948-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b948-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b948-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b948-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses/{deviceConfigurationUserStatusId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9b948-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9b948-118">Optional query parameters</span></span>
<span data-ttu-id="9b948-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b948-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9b948-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b948-120">Request headers</span></span>
|<span data-ttu-id="9b948-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b948-121">Header</span></span>|<span data-ttu-id="9b948-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b948-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b948-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9b948-123">Authorization</span></span>|<span data-ttu-id="9b948-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b948-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b948-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9b948-125">Accept</span></span>|<span data-ttu-id="9b948-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9b948-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b948-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b948-127">Request body</span></span>
<span data-ttu-id="9b948-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b948-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9b948-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b948-129">Response</span></span>
<span data-ttu-id="9b948-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b948-130">If successful, this method returns a `200 OK` response code and [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b948-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b948-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b948-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b948-132">Request</span></span>
<span data-ttu-id="9b948-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b948-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses/{deviceConfigurationUserStatusId}
```

### <a name="response"></a><span data-ttu-id="9b948-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b948-134">Response</span></span>
<span data-ttu-id="9b948-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b948-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 372

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
    "id": "7e323db2-3db2-7e32-b23d-327eb23d327e",
    "userDisplayName": "User Display Name value",
    "devicesCount": 12,
    "status": "notApplicable",
    "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
    "userPrincipalName": "User Principal Name value"
  }
}
```



