---
title: Lista sideLoadingKeies
description: Propiedades de la lista y relaciones de los objetos sideLoadingKey.
author: tfitzmac
ms.openlocfilehash: d18a9dbffea23408f7ba32c89620bcf340fe47e7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311126"
---
# <a name="list-sideloadingkeies"></a><span data-ttu-id="cbaaa-103">Lista sideLoadingKeies</span><span class="sxs-lookup"><span data-stu-id="cbaaa-103">List sideLoadingKeies</span></span>

> <span data-ttu-id="cbaaa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cbaaa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cbaaa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cbaaa-107">Propiedades de la lista y relaciones de los objetos [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .</span><span class="sxs-lookup"><span data-stu-id="cbaaa-107">List properties and relationships of the [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cbaaa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cbaaa-108">Prerequisites</span></span>
<span data-ttu-id="cbaaa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cbaaa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cbaaa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cbaaa-111">Permission type</span></span>|<span data-ttu-id="cbaaa-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cbaaa-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cbaaa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cbaaa-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cbaaa-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="cbaaa-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="cbaaa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cbaaa-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cbaaa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-116">Not supported.</span></span>|
|<span data-ttu-id="cbaaa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cbaaa-117">Application</span></span>|<span data-ttu-id="cbaaa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cbaaa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cbaaa-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/sideLoadingKeys
```

## <a name="request-headers"></a><span data-ttu-id="cbaaa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cbaaa-120">Request headers</span></span>
|<span data-ttu-id="cbaaa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbaaa-121">Header</span></span>|<span data-ttu-id="cbaaa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cbaaa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cbaaa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cbaaa-123">Authorization</span></span>|<span data-ttu-id="cbaaa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cbaaa-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cbaaa-125">Accept</span></span>|<span data-ttu-id="cbaaa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cbaaa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cbaaa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cbaaa-127">Request body</span></span>
<span data-ttu-id="cbaaa-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cbaaa-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbaaa-129">Response</span></span>
<span data-ttu-id="cbaaa-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-130">If successful, this method returns a `200 OK` response code and a collection of [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cbaaa-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbaaa-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cbaaa-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cbaaa-132">Request</span></span>
<span data-ttu-id="cbaaa-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/sideLoadingKeys
```

### <a name="response"></a><span data-ttu-id="cbaaa-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbaaa-134">Response</span></span>
<span data-ttu-id="cbaaa-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cbaaa-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 356

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.sideLoadingKey",
      "id": "21c4a3ff-a3ff-21c4-ffa3-c421ffa3c421",
      "value": "Value value",
      "displayName": "Display Name value",
      "description": "Description value",
      "totalActivation": 15,
      "lastUpdatedDateTime": "Last Updated Date Time value"
    }
  ]
}
```





