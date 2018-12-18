---
title: Lista embeddedSIMDeviceStates
description: Propiedades de la lista y relaciones de los objetos embeddedSIMDeviceState.
author: tfitzmac
ms.openlocfilehash: 3e3f68a0152e6919d5bf96847404b1d3d4f100e7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342920"
---
# <a name="list-embeddedsimdevicestates"></a><span data-ttu-id="8f091-103">Lista embeddedSIMDeviceStates</span><span class="sxs-lookup"><span data-stu-id="8f091-103">List embeddedSIMDeviceStates</span></span>

> <span data-ttu-id="8f091-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f091-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f091-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f091-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8f091-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f091-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f091-107">Propiedades de la lista y relaciones de los objetos [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="8f091-107">List properties and relationships of the [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8f091-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8f091-108">Prerequisites</span></span>
<span data-ttu-id="8f091-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f091-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f091-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f091-111">Permission type</span></span>|<span data-ttu-id="8f091-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f091-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8f091-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f091-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8f091-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="8f091-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="8f091-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f091-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8f091-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f091-116">Not supported.</span></span>|
|<span data-ttu-id="8f091-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f091-117">Application</span></span>|<span data-ttu-id="8f091-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f091-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8f091-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f091-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="8f091-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f091-120">Request headers</span></span>
|<span data-ttu-id="8f091-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f091-121">Header</span></span>|<span data-ttu-id="8f091-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8f091-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8f091-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8f091-123">Authorization</span></span>|<span data-ttu-id="8f091-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8f091-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8f091-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8f091-125">Accept</span></span>|<span data-ttu-id="8f091-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8f091-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f091-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f091-127">Request body</span></span>
<span data-ttu-id="8f091-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8f091-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8f091-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f091-129">Response</span></span>
<span data-ttu-id="8f091-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f091-130">If successful, this method returns a `200 OK` response code and a collection of [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f091-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f091-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="8f091-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f091-132">Request</span></span>
<span data-ttu-id="8f091-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f091-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/deviceStates
```

### <a name="response"></a><span data-ttu-id="8f091-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f091-134">Response</span></span>
<span data-ttu-id="8f091-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f091-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 602

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.embeddedSIMDeviceState",
      "id": "908884a3-84a3-9088-a384-8890a3848890",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "universalIntegratedCircuitCardIdentifier": "Universal Integrated Circuit Card Identifier value",
      "deviceName": "Device Name value",
      "userName": "User Name value",
      "state": "failed",
      "stateDetails": "State Details value"
    }
  ]
}
```





