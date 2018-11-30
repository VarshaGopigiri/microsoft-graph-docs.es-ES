---
title: asignar acción
description: Reemplazar todos los grupos para una directiva.
ms.openlocfilehash: dd892444d60338b73df4209eef00069667e15d48
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089318"
---
# <a name="assign-action"></a><span data-ttu-id="8c014-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="8c014-103">assign action</span></span>

> <span data-ttu-id="8c014-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8c014-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8c014-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8c014-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8c014-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8c014-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8c014-107">Reemplazar todos los grupos para una directiva.</span><span class="sxs-lookup"><span data-stu-id="8c014-107">Replace all targeted groups for a policy.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8c014-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c014-108">Prerequisites</span></span>
<span data-ttu-id="8c014-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c014-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8c014-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c014-111">Permission type</span></span>|<span data-ttu-id="8c014-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c014-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8c014-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c014-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8c014-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c014-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8c014-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c014-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8c014-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c014-116">Not supported.</span></span>|
|<span data-ttu-id="8c014-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c014-117">Application</span></span>|<span data-ttu-id="8c014-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c014-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8c014-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c014-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="8c014-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c014-120">Request headers</span></span>
|<span data-ttu-id="8c014-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c014-121">Header</span></span>|<span data-ttu-id="8c014-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8c014-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8c014-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c014-123">Authorization</span></span>|<span data-ttu-id="8c014-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8c014-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8c014-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8c014-125">Accept</span></span>|<span data-ttu-id="8c014-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8c014-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8c014-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c014-127">Request body</span></span>
<span data-ttu-id="8c014-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c014-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="8c014-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="8c014-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="8c014-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c014-130">Property</span></span>|<span data-ttu-id="8c014-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c014-131">Type</span></span>|<span data-ttu-id="8c014-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c014-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8c014-133">officeConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="8c014-133">officeConfigurationAssignments</span></span>|<span data-ttu-id="8c014-134">colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="8c014-134">[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) collection</span></span>|<span data-ttu-id="8c014-135">Lista de las asignaciones de configuración de office</span><span class="sxs-lookup"><span data-stu-id="8c014-135">List of office configuration assignments</span></span>|



## <a name="response"></a><span data-ttu-id="8c014-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c014-136">Response</span></span>
<span data-ttu-id="8c014-137">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y una colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c014-137">If successful, this action returns a `200 OK` response code and a [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8c014-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c014-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="8c014-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c014-139">Request</span></span>
<span data-ttu-id="8c014-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c014-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assign

Content-type: application/json
Content-length: 299

{
  "officeConfigurationAssignments": [
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

### <a name="response"></a><span data-ttu-id="8c014-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c014-141">Response</span></span>
<span data-ttu-id="8c014-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c014-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



