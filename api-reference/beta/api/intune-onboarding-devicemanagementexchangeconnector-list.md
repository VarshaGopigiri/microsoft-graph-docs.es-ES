---
title: Enumerar deviceManagementExchangeConnectors
description: Enumere las propiedades y las relaciones de los objetos deviceManagementExchangeConnector.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4a3118cda148756c9719eb483623bb2b4e9eb780
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853938"
---
# <a name="list-devicemanagementexchangeconnectors"></a><span data-ttu-id="22344-103">Enumerar deviceManagementExchangeConnectors</span><span class="sxs-lookup"><span data-stu-id="22344-103">List deviceManagementExchangeConnectors</span></span>

> <span data-ttu-id="22344-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="22344-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="22344-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="22344-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="22344-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="22344-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="22344-107">Enumere las propiedades y las relaciones de los objetos [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="22344-107">List properties and relationships of the [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="22344-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="22344-108">Prerequisites</span></span>
<span data-ttu-id="22344-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22344-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="22344-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22344-111">Permission type</span></span>|<span data-ttu-id="22344-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22344-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="22344-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22344-113">Delegated (work or school account)</span></span>|<span data-ttu-id="22344-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="22344-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="22344-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22344-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="22344-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22344-116">Not supported.</span></span>|
|<span data-ttu-id="22344-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22344-117">Application</span></span>|<span data-ttu-id="22344-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22344-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="22344-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22344-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/exchangeConnectors
```

## <a name="request-headers"></a><span data-ttu-id="22344-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22344-120">Request headers</span></span>
|<span data-ttu-id="22344-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22344-121">Header</span></span>|<span data-ttu-id="22344-122">Valor</span><span class="sxs-lookup"><span data-stu-id="22344-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="22344-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="22344-123">Authorization</span></span>|<span data-ttu-id="22344-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="22344-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="22344-125">Accept</span><span class="sxs-lookup"><span data-stu-id="22344-125">Accept</span></span>|<span data-ttu-id="22344-126">application/json</span><span class="sxs-lookup"><span data-stu-id="22344-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="22344-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="22344-127">Request body</span></span>
<span data-ttu-id="22344-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="22344-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="22344-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22344-129">Response</span></span>
<span data-ttu-id="22344-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22344-130">If successful, this method returns a `200 OK` response code and a collection of [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="22344-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22344-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="22344-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22344-132">Request</span></span>
<span data-ttu-id="22344-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22344-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/exchangeConnectors
```

### <a name="response"></a><span data-ttu-id="22344-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22344-134">Response</span></span>
<span data-ttu-id="22344-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="22344-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 616

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
      "id": "e11c1de8-1de8-e11c-e81d-1ce1e81d1ce1",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "status": "connectionPending",
      "primarySmtpAddress": "Primary Smtp Address value",
      "serverName": "Server Name value",
      "connectorServerName": "Connector Server Name value",
      "exchangeConnectorType": "hosted",
      "version": "Version value",
      "exchangeAlias": "Exchange Alias value",
      "exchangeOrganization": "Exchange Organization value"
    }
  ]
}
```





