---
title: Obtener officeClientConfigurationAssignment
description: Leer las propiedades y las relaciones del objeto officeClientConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: 4aec74e0df54d86ccffd5fb216ebfc1781412f5c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356318"
---
# <a name="get-officeclientconfigurationassignment"></a><span data-ttu-id="c8253-103">Obtener officeClientConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="c8253-103">Get officeClientConfigurationAssignment</span></span>

> <span data-ttu-id="c8253-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c8253-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c8253-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c8253-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c8253-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c8253-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c8253-107">Leer las propiedades y las relaciones del objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="c8253-107">Read properties and relationships of the [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c8253-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c8253-108">Prerequisites</span></span>
<span data-ttu-id="c8253-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c8253-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c8253-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c8253-111">Permission type</span></span>|<span data-ttu-id="c8253-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c8253-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c8253-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c8253-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c8253-114">\*\* TODO: Determinar los ámbitos \*\*</span><span class="sxs-lookup"><span data-stu-id="c8253-114">\*\*TODO: Determine scopes \*\*</span></span>|
|<span data-ttu-id="c8253-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c8253-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c8253-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8253-116">Not supported.</span></span>|
|<span data-ttu-id="c8253-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c8253-117">Application</span></span>|<span data-ttu-id="c8253-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8253-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c8253-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c8253-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments/{officeClientConfigurationAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c8253-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c8253-120">Optional query parameters</span></span>
<span data-ttu-id="c8253-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8253-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c8253-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c8253-122">Request headers</span></span>
|<span data-ttu-id="c8253-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8253-123">Header</span></span>|<span data-ttu-id="c8253-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c8253-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c8253-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="c8253-125">Authorization</span></span>|<span data-ttu-id="c8253-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c8253-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c8253-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c8253-127">Accept</span></span>|<span data-ttu-id="c8253-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c8253-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c8253-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c8253-129">Request body</span></span>
<span data-ttu-id="c8253-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c8253-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c8253-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8253-131">Response</span></span>
<span data-ttu-id="c8253-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8253-132">If successful, this method returns a `200 OK` response code and [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c8253-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8253-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="c8253-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c8253-134">Request</span></span>
<span data-ttu-id="c8253-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8253-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments/{officeClientConfigurationAssignmentId}
```

### <a name="response"></a><span data-ttu-id="c8253-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8253-136">Response</span></span>
<span data-ttu-id="c8253-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c8253-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 250

{
  "value": {
    "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
    "id": "804730f3-30f3-8047-f330-4780f3304780",
    "target": {
      "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
    }
  }
}
```



