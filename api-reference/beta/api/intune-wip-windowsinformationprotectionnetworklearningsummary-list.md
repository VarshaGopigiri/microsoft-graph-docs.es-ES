---
title: Enumerar windowsInformationProtectionNetworkLearningSummaries
description: Enumere las propiedades y las relaciones de los objetos windowsInformationProtectionNetworkLearningSummary.
ms.openlocfilehash: ce9ff2e2fb662408f911cb907f22a7dc72aede72
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086344"
---
# <a name="list-windowsinformationprotectionnetworklearningsummaries"></a><span data-ttu-id="f7187-103">Enumerar windowsInformationProtectionNetworkLearningSummaries</span><span class="sxs-lookup"><span data-stu-id="f7187-103">List windowsInformationProtectionNetworkLearningSummaries</span></span>

> <span data-ttu-id="f7187-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f7187-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f7187-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f7187-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f7187-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f7187-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f7187-107">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md).</span><span class="sxs-lookup"><span data-stu-id="f7187-107">List properties and relationships of the [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f7187-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f7187-108">Prerequisites</span></span>
<span data-ttu-id="f7187-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7187-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f7187-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7187-111">Permission type</span></span>|<span data-ttu-id="f7187-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7187-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f7187-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7187-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f7187-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7187-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="f7187-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7187-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f7187-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7187-116">Not supported.</span></span>|
|<span data-ttu-id="f7187-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7187-117">Application</span></span>|<span data-ttu-id="f7187-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7187-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f7187-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7187-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="f7187-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7187-120">Request headers</span></span>
|<span data-ttu-id="f7187-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7187-121">Header</span></span>|<span data-ttu-id="f7187-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f7187-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f7187-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f7187-123">Authorization</span></span>|<span data-ttu-id="f7187-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f7187-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f7187-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f7187-125">Accept</span></span>|<span data-ttu-id="f7187-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f7187-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f7187-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7187-127">Request body</span></span>
<span data-ttu-id="f7187-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f7187-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f7187-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7187-129">Response</span></span>
<span data-ttu-id="f7187-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7187-130">If successful, this method returns a `200 OK` response code and a collection of [windowsInformationProtectionNetworkLearningSummary](../resources/intune-wip-windowsinformationprotectionnetworklearningsummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f7187-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7187-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f7187-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7187-132">Request</span></span>
<span data-ttu-id="f7187-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7187-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/windowsInformationProtectionNetworkLearningSummaries
```

### <a name="response"></a><span data-ttu-id="f7187-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7187-134">Response</span></span>
<span data-ttu-id="f7187-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f7187-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 235

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtectionNetworkLearningSummary",
      "id": "242108f7-08f7-2421-f708-2124f7082124",
      "url": "Url value",
      "deviceCount": 11
    }
  ]
}
```





