---
title: Lista iosLobAppProvisioningConfigurations
description: Propiedades de la lista y relaciones de los objetos iosLobAppProvisioningConfiguration.
author: tfitzmac
ms.openlocfilehash: f3535b412cb0eaac732b2237cc96adec88d19a35
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348478"
---
# <a name="list-ioslobappprovisioningconfigurations"></a><span data-ttu-id="826f2-103">Lista iosLobAppProvisioningConfigurations</span><span class="sxs-lookup"><span data-stu-id="826f2-103">List iosLobAppProvisioningConfigurations</span></span>

> <span data-ttu-id="826f2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="826f2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="826f2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="826f2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="826f2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="826f2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="826f2-107">Propiedades de la lista y relaciones de los objetos [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="826f2-107">List properties and relationships of the [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="826f2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="826f2-108">Prerequisites</span></span>
<span data-ttu-id="826f2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="826f2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="826f2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="826f2-111">Permission type</span></span>|<span data-ttu-id="826f2-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="826f2-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="826f2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="826f2-113">Delegated (work or school account)</span></span>|<span data-ttu-id="826f2-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="826f2-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="826f2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="826f2-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="826f2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="826f2-116">Not supported.</span></span>|
|<span data-ttu-id="826f2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="826f2-117">Application</span></span>|<span data-ttu-id="826f2-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="826f2-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="826f2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="826f2-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosLobAppProvisioningConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="826f2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="826f2-120">Request headers</span></span>
|<span data-ttu-id="826f2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="826f2-121">Header</span></span>|<span data-ttu-id="826f2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="826f2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="826f2-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="826f2-123">Authorization</span></span>|<span data-ttu-id="826f2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="826f2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="826f2-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="826f2-125">Accept</span></span>|<span data-ttu-id="826f2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="826f2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="826f2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="826f2-127">Request body</span></span>
<span data-ttu-id="826f2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="826f2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="826f2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="826f2-129">Response</span></span>
<span data-ttu-id="826f2-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="826f2-130">If successful, this method returns a `200 OK` response code and a collection of [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="826f2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="826f2-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="826f2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="826f2-132">Request</span></span>
<span data-ttu-id="826f2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="826f2-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations
```

### <a name="response"></a><span data-ttu-id="826f2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="826f2-134">Response</span></span>
<span data-ttu-id="826f2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="826f2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 558

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfiguration",
      "id": "e2a23631-3631-e2a2-3136-a2e23136a2e2",
      "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
      "payloadFileName": "Payload File Name value",
      "payload": "cGF5bG9hZA==",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "displayName": "Display Name value",
      "version": 7
    }
  ]
}
```





