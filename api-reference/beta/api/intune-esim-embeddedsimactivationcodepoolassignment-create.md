---
title: Crear embeddedSIMActivationCodePoolAssignment
description: Crear un nuevo objeto embeddedSIMActivationCodePoolAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 61a541d9b95f7a8e9f3057856c11fb873dd00fc3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953472"
---
# <a name="create-embeddedsimactivationcodepoolassignment"></a><span data-ttu-id="a9b8a-103">Crear embeddedSIMActivationCodePoolAssignment</span><span class="sxs-lookup"><span data-stu-id="a9b8a-103">Create embeddedSIMActivationCodePoolAssignment</span></span>

> <span data-ttu-id="a9b8a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a9b8a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a9b8a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a9b8a-107">Crear un nuevo objeto [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a9b8a-107">Create a new [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a9b8a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a9b8a-108">Prerequisites</span></span>
<span data-ttu-id="a9b8a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a9b8a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a9b8a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a9b8a-111">Permission type</span></span>|<span data-ttu-id="a9b8a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a9b8a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a9b8a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a9b8a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a9b8a-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a9b8a-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a9b8a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9b8a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a9b8a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-116">Not supported.</span></span>|
|<span data-ttu-id="a9b8a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a9b8a-117">Application</span></span>|<span data-ttu-id="a9b8a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a9b8a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a9b8a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="a9b8a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9b8a-120">Request headers</span></span>
|<span data-ttu-id="a9b8a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9b8a-121">Header</span></span>|<span data-ttu-id="a9b8a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a9b8a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a9b8a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a9b8a-123">Authorization</span></span>|<span data-ttu-id="a9b8a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a9b8a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a9b8a-125">Accept</span></span>|<span data-ttu-id="a9b8a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a9b8a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a9b8a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a9b8a-127">Request body</span></span>
<span data-ttu-id="a9b8a-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto embeddedSIMActivationCodePoolAssignment.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-128">In the request body, supply a JSON representation for the embeddedSIMActivationCodePoolAssignment object.</span></span>

<span data-ttu-id="a9b8a-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el embeddedSIMActivationCodePoolAssignment.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-129">The following table shows the properties that are required when you create the embeddedSIMActivationCodePoolAssignment.</span></span>

|<span data-ttu-id="a9b8a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a9b8a-130">Property</span></span>|<span data-ttu-id="a9b8a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9b8a-131">Type</span></span>|<span data-ttu-id="a9b8a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9b8a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a9b8a-133">id</span><span class="sxs-lookup"><span data-stu-id="a9b8a-133">id</span></span>|<span data-ttu-id="a9b8a-134">String</span><span class="sxs-lookup"><span data-stu-id="a9b8a-134">String</span></span>|<span data-ttu-id="a9b8a-135">Identificador único para la asignación de grupo de código de activación SIM incrustada.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-135">Unique identifier for the embedded SIM activation code pool assignment.</span></span> <span data-ttu-id="a9b8a-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-136">System generated value assigned when created.</span></span>|
|<span data-ttu-id="a9b8a-137">target</span><span class="sxs-lookup"><span data-stu-id="a9b8a-137">target</span></span>|[<span data-ttu-id="a9b8a-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="a9b8a-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="a9b8a-139">El tipo de grupos de destino mediante el grupo de código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-139">The type of groups targeted by the embedded SIM activation code pool.</span></span>|



## <a name="response"></a><span data-ttu-id="a9b8a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9b8a-140">Response</span></span>
<span data-ttu-id="a9b8a-141">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-141">If successful, this method returns a `201 Created` response code and a [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a9b8a-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9b8a-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="a9b8a-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a9b8a-143">Request</span></span>
<span data-ttu-id="a9b8a-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/assignments
Content-type: application/json
Content-length: 179

{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePoolAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="a9b8a-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9b8a-145">Response</span></span>
<span data-ttu-id="a9b8a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a9b8a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePoolAssignment",
  "id": "e7304dcc-4dcc-e730-cc4d-30e7cc4d30e7",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





