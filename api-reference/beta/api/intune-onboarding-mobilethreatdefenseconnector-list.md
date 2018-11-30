---
title: Enumerar mobileThreatDefenseConnectors
description: Enumere las propiedades y las relaciones de los objetos mobileThreatDefenseConnector.
ms.openlocfilehash: 5613292cb43437692a2c6f6395eb9875a464b518
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087992"
---
# <a name="list-mobilethreatdefenseconnectors"></a><span data-ttu-id="5617d-103">Enumerar mobileThreatDefenseConnectors</span><span class="sxs-lookup"><span data-stu-id="5617d-103">List mobileThreatDefenseConnectors</span></span>

> <span data-ttu-id="5617d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5617d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5617d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5617d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5617d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5617d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5617d-107">Enumere las propiedades y las relaciones de los objetos [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md).</span><span class="sxs-lookup"><span data-stu-id="5617d-107">List properties and relationships of the [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5617d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5617d-108">Prerequisites</span></span>
<span data-ttu-id="5617d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5617d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5617d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5617d-111">Permission type</span></span>|<span data-ttu-id="5617d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5617d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5617d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5617d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5617d-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="5617d-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="5617d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5617d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5617d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5617d-116">Not supported.</span></span>|
|<span data-ttu-id="5617d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5617d-117">Application</span></span>|<span data-ttu-id="5617d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5617d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5617d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5617d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/mobileThreatDefenseConnectors
```

## <a name="request-headers"></a><span data-ttu-id="5617d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5617d-120">Request headers</span></span>
|<span data-ttu-id="5617d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5617d-121">Header</span></span>|<span data-ttu-id="5617d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5617d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5617d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5617d-123">Authorization</span></span>|<span data-ttu-id="5617d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5617d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5617d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5617d-125">Accept</span></span>|<span data-ttu-id="5617d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5617d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5617d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5617d-127">Request body</span></span>
<span data-ttu-id="5617d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5617d-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5617d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5617d-129">Response</span></span>
<span data-ttu-id="5617d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5617d-130">If successful, this method returns a `200 OK` response code and a collection of [mobileThreatDefenseConnector](../resources/intune-onboarding-mobilethreatdefenseconnector.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5617d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5617d-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="5617d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5617d-132">Request</span></span>
<span data-ttu-id="5617d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5617d-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/mobileThreatDefenseConnectors
```

### <a name="response"></a><span data-ttu-id="5617d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5617d-134">Response</span></span>
<span data-ttu-id="5617d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5617d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 764

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
      "id": "e4bede14-de14-e4be-14de-bee414debee4",
      "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
      "partnerState": "available",
      "androidEnabled": true,
      "iosEnabled": true,
      "windowsEnabled": true,
      "macEnabled": true,
      "androidDeviceBlockedOnMissingPartnerData": true,
      "iosDeviceBlockedOnMissingPartnerData": true,
      "windowsDeviceBlockedOnMissingPartnerData": true,
      "macDeviceBlockedOnMissingPartnerData": true,
      "partnerUnsupportedOsVersionBlocked": true,
      "partnerUnresponsivenessThresholdInDays": 6,
      "allowPartnerToCollectIOSApplicationMetadata": true
    }
  ]
}
```





