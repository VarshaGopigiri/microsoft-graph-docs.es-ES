---
title: Lista officeClientConfigurationAssignments
description: Propiedades de la lista y relaciones de los objetos officeClientConfigurationAssignment.
ms.openlocfilehash: 8c8447a7e6339b40e958e019ddd0b9eed17b8c9f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083303"
---
# <a name="list-officeclientconfigurationassignments"></a><span data-ttu-id="ae532-103">Lista officeClientConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="ae532-103">List officeClientConfigurationAssignments</span></span>

> <span data-ttu-id="ae532-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ae532-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ae532-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ae532-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ae532-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ae532-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ae532-107">Propiedades de la lista y relaciones de los objetos [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="ae532-107">List properties and relationships of the [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ae532-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae532-108">Prerequisites</span></span>
<span data-ttu-id="ae532-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae532-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ae532-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae532-111">Permission type</span></span>|<span data-ttu-id="ae532-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae532-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ae532-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae532-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ae532-114">\*\* TODO: Determinar los ámbitos \*\*</span><span class="sxs-lookup"><span data-stu-id="ae532-114">\*\*TODO: Determine scopes \*\*</span></span>|
|<span data-ttu-id="ae532-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae532-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ae532-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae532-116">Not supported.</span></span>|
|<span data-ttu-id="ae532-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae532-117">Application</span></span>|<span data-ttu-id="ae532-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae532-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ae532-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae532-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="ae532-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae532-120">Request headers</span></span>
|<span data-ttu-id="ae532-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae532-121">Header</span></span>|<span data-ttu-id="ae532-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ae532-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ae532-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae532-123">Authorization</span></span>|<span data-ttu-id="ae532-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ae532-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ae532-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ae532-125">Accept</span></span>|<span data-ttu-id="ae532-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ae532-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ae532-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae532-127">Request body</span></span>
<span data-ttu-id="ae532-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ae532-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ae532-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae532-129">Response</span></span>
<span data-ttu-id="ae532-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae532-130">If successful, this method returns a `200 OK` response code and a collection of [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ae532-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae532-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ae532-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae532-132">Request</span></span>
<span data-ttu-id="ae532-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae532-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments
```

### <a name="response"></a><span data-ttu-id="ae532-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae532-134">Response</span></span>
<span data-ttu-id="ae532-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ae532-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 274

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
      "id": "804730f3-30f3-8047-f330-4780f3304780",
      "target": {
        "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
      }
    }
  ]
}
```



