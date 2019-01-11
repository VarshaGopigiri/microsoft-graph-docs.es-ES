---
title: Función getUserIdsWithFlaggedAppRegistration
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a501474373dad9bcb57b2e8aca448e846da0f8b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842318"
---
# <a name="getuseridswithflaggedappregistration-function"></a><span data-ttu-id="54dcc-103">Función getUserIdsWithFlaggedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="54dcc-103">getUserIdsWithFlaggedAppRegistration function</span></span>

> <span data-ttu-id="54dcc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54dcc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54dcc-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="54dcc-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54dcc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54dcc-106">Prerequisites</span></span>
<span data-ttu-id="54dcc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="54dcc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="54dcc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54dcc-109">Permission type</span></span>|<span data-ttu-id="54dcc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54dcc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54dcc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54dcc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="54dcc-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="54dcc-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="54dcc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54dcc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54dcc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54dcc-114">Not supported.</span></span>|
|<span data-ttu-id="54dcc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54dcc-115">Application</span></span>|<span data-ttu-id="54dcc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54dcc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54dcc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54dcc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations/getUserIdsWithFlaggedAppRegistration
```

## <a name="request-headers"></a><span data-ttu-id="54dcc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54dcc-118">Request headers</span></span>
|<span data-ttu-id="54dcc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54dcc-119">Header</span></span>|<span data-ttu-id="54dcc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="54dcc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54dcc-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="54dcc-121">Authorization</span></span>|<span data-ttu-id="54dcc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54dcc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54dcc-123">Accept</span><span class="sxs-lookup"><span data-stu-id="54dcc-123">Accept</span></span>|<span data-ttu-id="54dcc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="54dcc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54dcc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54dcc-125">Request body</span></span>
<span data-ttu-id="54dcc-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="54dcc-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="54dcc-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54dcc-127">Response</span></span>
<span data-ttu-id="54dcc-128">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54dcc-128">If successful, this function returns a `200 OK` response code and a String collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54dcc-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54dcc-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="54dcc-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54dcc-130">Request</span></span>
<span data-ttu-id="54dcc-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54dcc-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/getUserIdsWithFlaggedAppRegistration
```

### <a name="response"></a><span data-ttu-id="54dcc-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54dcc-132">Response</span></span>
<span data-ttu-id="54dcc-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54dcc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 79

{
  "value": [
    "Get User Ids With Flagged App Registration value"
  ]
}
```



