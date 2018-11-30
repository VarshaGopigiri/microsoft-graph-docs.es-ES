---
title: Obtener deviceManagementExchangeConnector
description: Lea las propiedades y las relaciones del objeto deviceManagementExchangeConnector.
ms.openlocfilehash: 6036b44246aa27ff35e34ba63c1f31d0f51b2064
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029082"
---
# <a name="get-devicemanagementexchangeconnector"></a><span data-ttu-id="b40e3-103">Obtener deviceManagementExchangeConnector</span><span class="sxs-lookup"><span data-stu-id="b40e3-103">Get deviceManagementExchangeConnector</span></span>

> <span data-ttu-id="b40e3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b40e3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b40e3-105">Lea las propiedades y las relaciones del objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="b40e3-105">Read properties and relationships of the [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b40e3-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b40e3-106">Prerequisites</span></span>
<span data-ttu-id="b40e3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b40e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b40e3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b40e3-109">Permission type</span></span>|<span data-ttu-id="b40e3-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b40e3-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b40e3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b40e3-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b40e3-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="b40e3-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="b40e3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b40e3-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b40e3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b40e3-114">Not supported.</span></span>|
|<span data-ttu-id="b40e3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b40e3-115">Application</span></span>|<span data-ttu-id="b40e3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b40e3-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b40e3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b40e3-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b40e3-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b40e3-118">Optional query parameters</span></span>
<span data-ttu-id="b40e3-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b40e3-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b40e3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b40e3-120">Request headers</span></span>
|<span data-ttu-id="b40e3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b40e3-121">Header</span></span>|<span data-ttu-id="b40e3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b40e3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b40e3-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b40e3-123">Authorization</span></span>|<span data-ttu-id="b40e3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b40e3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b40e3-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b40e3-125">Accept</span></span>|<span data-ttu-id="b40e3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b40e3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b40e3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b40e3-127">Request body</span></span>
<span data-ttu-id="b40e3-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b40e3-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b40e3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b40e3-129">Response</span></span>
<span data-ttu-id="b40e3-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b40e3-130">If successful, this method returns a `200 OK` response code and [deviceManagementExchangeConnector](../resources/intune-onboarding-devicemanagementexchangeconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b40e3-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b40e3-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b40e3-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b40e3-132">Request</span></span>
<span data-ttu-id="b40e3-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b40e3-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
```

### <a name="response"></a><span data-ttu-id="b40e3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b40e3-134">Response</span></span>
<span data-ttu-id="b40e3-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b40e3-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 580

{
  "value": {
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
}
```


