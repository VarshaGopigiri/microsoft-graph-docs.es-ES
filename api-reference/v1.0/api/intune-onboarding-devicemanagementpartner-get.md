---
title: Obtener deviceManagementPartner
description: Lea las propiedades y las relaciones del objeto deviceManagementPartner.
ms.openlocfilehash: f5a0a7fc2edcac82421049ad3789fc2f1edda1e3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029401"
---
# <a name="get-devicemanagementpartner"></a><span data-ttu-id="f5a4e-103">Obtener deviceManagementPartner</span><span class="sxs-lookup"><span data-stu-id="f5a4e-103">Get deviceManagementPartner</span></span>

> <span data-ttu-id="f5a4e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f5a4e-105">Lea las propiedades y las relaciones del objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="f5a4e-105">Read properties and relationships of the [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f5a4e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5a4e-106">Prerequisites</span></span>
<span data-ttu-id="f5a4e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5a4e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5a4e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5a4e-109">Permission type</span></span>|<span data-ttu-id="f5a4e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5a4e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f5a4e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5a4e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f5a4e-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5a4e-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="f5a4e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5a4e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f5a4e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-114">Not supported.</span></span>|
|<span data-ttu-id="f5a4e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5a4e-115">Application</span></span>|<span data-ttu-id="f5a4e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f5a4e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5a4e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f5a4e-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f5a4e-118">Optional query parameters</span></span>
<span data-ttu-id="f5a4e-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f5a4e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5a4e-120">Request headers</span></span>
|<span data-ttu-id="f5a4e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5a4e-121">Header</span></span>|<span data-ttu-id="f5a4e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f5a4e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f5a4e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5a4e-123">Authorization</span></span>|<span data-ttu-id="f5a4e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f5a4e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f5a4e-125">Accept</span></span>|<span data-ttu-id="f5a4e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f5a4e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f5a4e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5a4e-127">Request body</span></span>
<span data-ttu-id="f5a4e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5a4e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5a4e-129">Response</span></span>
<span data-ttu-id="f5a4e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-130">If successful, this method returns a `200 OK` response code and [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f5a4e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5a4e-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f5a4e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5a4e-132">Request</span></span>
<span data-ttu-id="f5a4e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners/{deviceManagementPartnerId}
```

### <a name="response"></a><span data-ttu-id="f5a4e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5a4e-134">Response</span></span>
<span data-ttu-id="f5a4e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5a4e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 590

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceManagementPartner",
    "id": "d21e377a-377a-d21e-7a37-1ed27a371ed2",
    "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
    "partnerState": "unavailable",
    "partnerAppType": "singleTenantApp",
    "singleTenantAppId": "Single Tenant App Id value",
    "displayName": "Display Name value",
    "isConfigured": true,
    "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
    "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
  }
}
```



