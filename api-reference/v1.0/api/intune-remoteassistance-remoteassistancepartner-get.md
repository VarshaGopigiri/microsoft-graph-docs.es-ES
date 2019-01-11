---
title: Obtener remoteAssistancePartner
description: Lea las propiedades y las relaciones del objeto remoteAssistancePartner.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 51d22e0945c214623956b17db7f87e9d5e5d6b88
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821633"
---
# <a name="get-remoteassistancepartner"></a><span data-ttu-id="69b62-103">Obtener remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="69b62-103">Get remoteAssistancePartner</span></span>

> <span data-ttu-id="69b62-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="69b62-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="69b62-105">Lea las propiedades y las relaciones del objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="69b62-105">Read properties and relationships of the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="69b62-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="69b62-106">Prerequisites</span></span>
<span data-ttu-id="69b62-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69b62-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69b62-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69b62-109">Permission type</span></span>|<span data-ttu-id="69b62-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69b62-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="69b62-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69b62-111">Delegated (work or school account)</span></span>|<span data-ttu-id="69b62-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="69b62-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="69b62-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69b62-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="69b62-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69b62-114">Not supported.</span></span>|
|<span data-ttu-id="69b62-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69b62-115">Application</span></span>|<span data-ttu-id="69b62-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69b62-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="69b62-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69b62-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="69b62-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="69b62-118">Optional query parameters</span></span>
<span data-ttu-id="69b62-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69b62-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="69b62-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69b62-120">Request headers</span></span>
|<span data-ttu-id="69b62-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69b62-121">Header</span></span>|<span data-ttu-id="69b62-122">Valor</span><span class="sxs-lookup"><span data-stu-id="69b62-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="69b62-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="69b62-123">Authorization</span></span>|<span data-ttu-id="69b62-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="69b62-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="69b62-125">Accept</span><span class="sxs-lookup"><span data-stu-id="69b62-125">Accept</span></span>|<span data-ttu-id="69b62-126">application/json</span><span class="sxs-lookup"><span data-stu-id="69b62-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="69b62-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69b62-127">Request body</span></span>
<span data-ttu-id="69b62-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="69b62-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="69b62-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69b62-129">Response</span></span>
<span data-ttu-id="69b62-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69b62-130">If successful, this method returns a `200 OK` response code and [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69b62-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69b62-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="69b62-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69b62-132">Request</span></span>
<span data-ttu-id="69b62-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69b62-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

### <a name="response"></a><span data-ttu-id="69b62-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69b62-134">Response</span></span>
<span data-ttu-id="69b62-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69b62-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 346

{
  "value": {
    "@odata.type": "#microsoft.graph.remoteAssistancePartner",
    "id": "7443c8b9-c8b9-7443-b9c8-4374b9c84374",
    "displayName": "Display Name value",
    "onboardingUrl": "https://example.com/onboardingUrl/",
    "onboardingStatus": "onboarding",
    "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
  }
}
```



