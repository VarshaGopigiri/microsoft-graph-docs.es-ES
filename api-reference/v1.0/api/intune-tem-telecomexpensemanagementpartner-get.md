---
title: Obtener telecomExpenseManagementPartner
description: Lea las propiedades y las relaciones del objeto telecomExpenseManagementPartner.
ms.openlocfilehash: 4b0e33b86a084d97c426134f42e48711b646c86f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031146"
---
# <a name="get-telecomexpensemanagementpartner"></a><span data-ttu-id="f2935-103">Obtener telecomExpenseManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f2935-103">Get telecomExpenseManagementPartner</span></span>

> <span data-ttu-id="f2935-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f2935-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f2935-105">Lea las propiedades y las relaciones del objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="f2935-105">Read properties and relationships of the [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f2935-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2935-106">Prerequisites</span></span>
<span data-ttu-id="f2935-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f2935-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f2935-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f2935-109">Permission type</span></span>|<span data-ttu-id="f2935-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f2935-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f2935-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f2935-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f2935-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="f2935-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="f2935-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f2935-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f2935-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2935-114">Not supported.</span></span>|
|<span data-ttu-id="f2935-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f2935-115">Application</span></span>|<span data-ttu-id="f2935-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2935-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f2935-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2935-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f2935-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f2935-118">Optional query parameters</span></span>
<span data-ttu-id="f2935-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2935-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f2935-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2935-120">Request headers</span></span>
|<span data-ttu-id="f2935-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2935-121">Header</span></span>|<span data-ttu-id="f2935-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f2935-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f2935-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2935-123">Authorization</span></span>|<span data-ttu-id="f2935-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f2935-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f2935-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f2935-125">Accept</span></span>|<span data-ttu-id="f2935-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f2935-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f2935-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2935-127">Request body</span></span>
<span data-ttu-id="f2935-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f2935-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f2935-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2935-129">Response</span></span>
<span data-ttu-id="f2935-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2935-130">If successful, this method returns a `200 OK` response code and [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2935-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2935-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f2935-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2935-132">Request</span></span>
<span data-ttu-id="f2935-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2935-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
```

### <a name="response"></a><span data-ttu-id="f2935-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2935-134">Response</span></span>
<span data-ttu-id="f2935-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f2935-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 330

{
  "value": {
    "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
    "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
    "displayName": "Display Name value",
    "url": "Url value",
    "appAuthorized": true,
    "enabled": true,
    "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
  }
}
```



