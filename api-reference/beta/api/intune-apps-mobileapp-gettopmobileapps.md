---
title: getTopMobileApps (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d4f9299e2de7dca455d192637eba84ccc553d434
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879502"
---
# <a name="gettopmobileapps-function"></a><span data-ttu-id="dbe04-103">getTopMobileApps (función)</span><span class="sxs-lookup"><span data-stu-id="dbe04-103">getTopMobileApps function</span></span>

> <span data-ttu-id="dbe04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dbe04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dbe04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dbe04-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dbe04-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dbe04-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dbe04-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dbe04-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dbe04-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbe04-108">Prerequisites</span></span>
<span data-ttu-id="dbe04-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dbe04-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dbe04-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbe04-111">Permission type</span></span>|<span data-ttu-id="dbe04-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbe04-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dbe04-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbe04-113">Delegated (work or school account)</span></span>|<span data-ttu-id="dbe04-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="dbe04-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="dbe04-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbe04-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dbe04-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbe04-116">Not supported.</span></span>|
|<span data-ttu-id="dbe04-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbe04-117">Application</span></span>|<span data-ttu-id="dbe04-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbe04-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dbe04-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbe04-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/getTopMobileApps
```

## <a name="request-headers"></a><span data-ttu-id="dbe04-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbe04-120">Request headers</span></span>
|<span data-ttu-id="dbe04-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbe04-121">Header</span></span>|<span data-ttu-id="dbe04-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dbe04-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dbe04-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="dbe04-123">Authorization</span></span>|<span data-ttu-id="dbe04-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dbe04-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dbe04-125">Accept</span><span class="sxs-lookup"><span data-stu-id="dbe04-125">Accept</span></span>|<span data-ttu-id="dbe04-126">application/json</span><span class="sxs-lookup"><span data-stu-id="dbe04-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dbe04-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbe04-127">Request body</span></span>
<span data-ttu-id="dbe04-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="dbe04-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="dbe04-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="dbe04-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="dbe04-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbe04-130">Property</span></span>|<span data-ttu-id="dbe04-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbe04-131">Type</span></span>|<span data-ttu-id="dbe04-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbe04-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dbe04-133">status</span><span class="sxs-lookup"><span data-stu-id="dbe04-133">status</span></span>|<span data-ttu-id="dbe04-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbe04-134">String</span></span>|<span data-ttu-id="dbe04-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dbe04-135">Not yet documented</span></span>|
|<span data-ttu-id="dbe04-136">count</span><span class="sxs-lookup"><span data-stu-id="dbe04-136">count</span></span>|<span data-ttu-id="dbe04-137">Int64</span><span class="sxs-lookup"><span data-stu-id="dbe04-137">Int64</span></span>|<span data-ttu-id="dbe04-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="dbe04-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="dbe04-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbe04-139">Response</span></span>
<span data-ttu-id="dbe04-140">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y una colección de [mobileApp](../resources/intune-apps-mobileapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbe04-140">If successful, this function returns a `200 OK` response code and a [mobileApp](../resources/intune-apps-mobileapp.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dbe04-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbe04-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="dbe04-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbe04-142">Request</span></span>
<span data-ttu-id="dbe04-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbe04-143">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/getTopMobileApps(status='parameterValue',count=5)
```

### <a name="response"></a><span data-ttu-id="dbe04-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbe04-144">Response</span></span>
<span data-ttu-id="dbe04-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbe04-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 881

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileApp",
      "id": "0177548a-548a-0177-8a54-77018a547701",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisher": "Publisher value",
      "largeIcon": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "Type value",
        "value": "dmFsdWU="
      },
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "isFeatured": true,
      "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
      "informationUrl": "https://example.com/informationUrl/",
      "owner": "Owner value",
      "developer": "Developer value",
      "notes": "Notes value",
      "uploadState": 11,
      "publishingState": "processing"
    }
  ]
}
```





