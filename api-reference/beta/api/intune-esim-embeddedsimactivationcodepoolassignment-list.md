---
title: Lista embeddedSIMActivationCodePoolAssignments
description: Propiedades de la lista y relaciones de los objetos embeddedSIMActivationCodePoolAssignment.
ms.openlocfilehash: cfaef6034509a9a3b7a48588bfa98cbbbaacf80c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087456"
---
# <a name="list-embeddedsimactivationcodepoolassignments"></a><span data-ttu-id="70376-103">Lista embeddedSIMActivationCodePoolAssignments</span><span class="sxs-lookup"><span data-stu-id="70376-103">List embeddedSIMActivationCodePoolAssignments</span></span>

> <span data-ttu-id="70376-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="70376-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="70376-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="70376-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="70376-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="70376-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="70376-107">Propiedades de la lista y relaciones de los objetos [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="70376-107">List properties and relationships of the [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="70376-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="70376-108">Prerequisites</span></span>
<span data-ttu-id="70376-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="70376-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="70376-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70376-111">Permission type</span></span>|<span data-ttu-id="70376-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70376-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="70376-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70376-113">Delegated (work or school account)</span></span>|<span data-ttu-id="70376-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="70376-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="70376-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70376-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="70376-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70376-116">Not supported.</span></span>|
|<span data-ttu-id="70376-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70376-117">Application</span></span>|<span data-ttu-id="70376-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70376-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="70376-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70376-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="70376-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70376-120">Request headers</span></span>
|<span data-ttu-id="70376-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70376-121">Header</span></span>|<span data-ttu-id="70376-122">Valor</span><span class="sxs-lookup"><span data-stu-id="70376-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="70376-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="70376-123">Authorization</span></span>|<span data-ttu-id="70376-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="70376-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="70376-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="70376-125">Accept</span></span>|<span data-ttu-id="70376-126">application/json</span><span class="sxs-lookup"><span data-stu-id="70376-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="70376-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70376-127">Request body</span></span>
<span data-ttu-id="70376-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="70376-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="70376-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70376-129">Response</span></span>
<span data-ttu-id="70376-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70376-130">If successful, this method returns a `200 OK` response code and a collection of [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70376-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70376-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="70376-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70376-132">Request</span></span>
<span data-ttu-id="70376-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70376-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/assignments
```

### <a name="response"></a><span data-ttu-id="70376-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70376-134">Response</span></span>
<span data-ttu-id="70376-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70376-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 281

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePoolAssignment",
      "id": "e7304dcc-4dcc-e730-cc4d-30e7cc4d30e7",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```





