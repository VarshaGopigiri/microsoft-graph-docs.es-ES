---
title: asignar acción
description: Todavía no documentado
ms.openlocfilehash: dd26c61f298071a98ad0734aa1ac5023581d5a9e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090778"
---
# <a name="assign-action"></a><span data-ttu-id="cbc9e-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="cbc9e-103">assign action</span></span>

> <span data-ttu-id="cbc9e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cbc9e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cbc9e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cbc9e-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cbc9e-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cbc9e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cbc9e-108">Prerequisites</span></span>
<span data-ttu-id="cbc9e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cbc9e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cbc9e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cbc9e-111">Permission type</span></span>|<span data-ttu-id="cbc9e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cbc9e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cbc9e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cbc9e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cbc9e-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cbc9e-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="cbc9e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cbc9e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cbc9e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-116">Not supported.</span></span>|
|<span data-ttu-id="cbc9e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cbc9e-117">Application</span></span>|<span data-ttu-id="cbc9e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cbc9e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cbc9e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assign
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration/assign
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="cbc9e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cbc9e-120">Request headers</span></span>
|<span data-ttu-id="cbc9e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbc9e-121">Header</span></span>|<span data-ttu-id="cbc9e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cbc9e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cbc9e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="cbc9e-123">Authorization</span></span>|<span data-ttu-id="cbc9e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cbc9e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cbc9e-125">Accept</span></span>|<span data-ttu-id="cbc9e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cbc9e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cbc9e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cbc9e-127">Request body</span></span>
<span data-ttu-id="cbc9e-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="cbc9e-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="cbc9e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbc9e-130">Property</span></span>|<span data-ttu-id="cbc9e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbc9e-131">Type</span></span>|<span data-ttu-id="cbc9e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbc9e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cbc9e-133">deviceConfigurationGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="cbc9e-133">deviceConfigurationGroupAssignments</span></span>|<span data-ttu-id="cbc9e-134">colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cbc9e-134">[deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) collection</span></span>|<span data-ttu-id="cbc9e-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cbc9e-135">Not yet documented</span></span>|
|<span data-ttu-id="cbc9e-136">asignaciones</span><span class="sxs-lookup"><span data-stu-id="cbc9e-136">assignments</span></span>|<span data-ttu-id="cbc9e-137">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cbc9e-137">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="cbc9e-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cbc9e-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="cbc9e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbc9e-139">Response</span></span>
<span data-ttu-id="cbc9e-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-140">If successful, this action returns a `200 OK` response code and a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cbc9e-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbc9e-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="cbc9e-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cbc9e-142">Request</span></span>
<span data-ttu-id="cbc9e-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assign

Content-type: application/json
Content-length: 548

{
  "deviceConfigurationGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationGroupAssignment",
      "id": "561d26c5-26c5-561d-c526-1d56c5261d56",
      "targetGroupId": "Target Group Id value",
      "excludeGroup": true
    }
  ],
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
      "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="cbc9e-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cbc9e-144">Response</span></span>
<span data-ttu-id="cbc9e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cbc9e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 271

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
      "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```





