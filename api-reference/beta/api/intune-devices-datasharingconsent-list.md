---
title: Lista dataSharingConsents
description: Propiedades de la lista y relaciones de los objetos dataSharingConsent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4aa781f00bc24423b8b2f67bd783d824d73298ba
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948908"
---
# <a name="list-datasharingconsents"></a><span data-ttu-id="bb9aa-103">Lista dataSharingConsents</span><span class="sxs-lookup"><span data-stu-id="bb9aa-103">List dataSharingConsents</span></span>

> <span data-ttu-id="bb9aa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb9aa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bb9aa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb9aa-107">Propiedades de la lista y relaciones de los objetos [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9aa-107">List properties and relationships of the [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb9aa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bb9aa-108">Prerequisites</span></span>
<span data-ttu-id="bb9aa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb9aa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb9aa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb9aa-111">Permission type</span></span>|<span data-ttu-id="bb9aa-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb9aa-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb9aa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb9aa-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bb9aa-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb9aa-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bb9aa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb9aa-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb9aa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-116">Not supported.</span></span>|
|<span data-ttu-id="bb9aa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb9aa-117">Application</span></span>|<span data-ttu-id="bb9aa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb9aa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb9aa-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/dataSharingConsents
```

## <a name="request-headers"></a><span data-ttu-id="bb9aa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb9aa-120">Request headers</span></span>
|<span data-ttu-id="bb9aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb9aa-121">Header</span></span>|<span data-ttu-id="bb9aa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bb9aa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb9aa-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bb9aa-123">Authorization</span></span>|<span data-ttu-id="bb9aa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb9aa-125">Accept</span><span class="sxs-lookup"><span data-stu-id="bb9aa-125">Accept</span></span>|<span data-ttu-id="bb9aa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bb9aa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb9aa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb9aa-127">Request body</span></span>
<span data-ttu-id="bb9aa-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb9aa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb9aa-129">Response</span></span>
<span data-ttu-id="bb9aa-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-130">If successful, this method returns a `200 OK` response code and a collection of [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb9aa-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb9aa-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb9aa-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb9aa-132">Request</span></span>
<span data-ttu-id="bb9aa-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/dataSharingConsents
```

### <a name="response"></a><span data-ttu-id="bb9aa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb9aa-134">Response</span></span>
<span data-ttu-id="bb9aa-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb9aa-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 447

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.dataSharingConsent",
      "id": "333387f7-87f7-3333-f787-3333f7873333",
      "serviceDisplayName": "Service Display Name value",
      "termsUrl": "https://example.com/termsUrl/",
      "granted": true,
      "grantDateTime": "2016-12-31T23:59:55.7154191-08:00",
      "grantedByUpn": "Granted By Upn value",
      "grantedByUserId": "Granted By User Id value"
    }
  ]
}
```





