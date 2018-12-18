---
title: Actualizar officeClientConfigurationAssignment
description: Actualizar las propiedades de un objeto officeClientConfigurationAssignment.
author: tfitzmac
ms.openlocfilehash: 78b0ae28bc61bc0d8d8c083502c6f6ef2cf7d0fb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343039"
---
# <a name="update-officeclientconfigurationassignment"></a><span data-ttu-id="a06eb-103">Actualizar officeClientConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a06eb-103">Update officeClientConfigurationAssignment</span></span>

> <span data-ttu-id="a06eb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a06eb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a06eb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a06eb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a06eb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a06eb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a06eb-107">Actualizar las propiedades de un objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a06eb-107">Update the properties of a [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a06eb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a06eb-108">Prerequisites</span></span>
<span data-ttu-id="a06eb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a06eb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a06eb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a06eb-111">Permission type</span></span>|<span data-ttu-id="a06eb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a06eb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a06eb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a06eb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a06eb-114">\*\* TODO: Determinar los ámbitos \*\*</span><span class="sxs-lookup"><span data-stu-id="a06eb-114">\*\*TODO: Determine scopes \*\*</span></span>|
|<span data-ttu-id="a06eb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a06eb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a06eb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a06eb-116">Not supported.</span></span>|
|<span data-ttu-id="a06eb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a06eb-117">Application</span></span>|<span data-ttu-id="a06eb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a06eb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a06eb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a06eb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments/{officeClientConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="a06eb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a06eb-120">Request headers</span></span>
|<span data-ttu-id="a06eb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a06eb-121">Header</span></span>|<span data-ttu-id="a06eb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a06eb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a06eb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a06eb-123">Authorization</span></span>|<span data-ttu-id="a06eb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a06eb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a06eb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a06eb-125">Accept</span></span>|<span data-ttu-id="a06eb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a06eb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a06eb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a06eb-127">Request body</span></span>
<span data-ttu-id="a06eb-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a06eb-128">In the request body, supply a JSON representation for the [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object.</span></span>

<span data-ttu-id="a06eb-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="a06eb-129">The following table shows the properties that are required when you create the [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md).</span></span>

|<span data-ttu-id="a06eb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a06eb-130">Property</span></span>|<span data-ttu-id="a06eb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a06eb-131">Type</span></span>|<span data-ttu-id="a06eb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a06eb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a06eb-133">id</span><span class="sxs-lookup"><span data-stu-id="a06eb-133">id</span></span>|<span data-ttu-id="a06eb-134">String</span><span class="sxs-lookup"><span data-stu-id="a06eb-134">String</span></span>|<span data-ttu-id="a06eb-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a06eb-135">Not yet documented</span></span>|
|<span data-ttu-id="a06eb-136">target</span><span class="sxs-lookup"><span data-stu-id="a06eb-136">target</span></span>|[<span data-ttu-id="a06eb-137">officeConfigurationAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="a06eb-137">officeConfigurationAssignmentTarget</span></span>](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)|<span data-ttu-id="a06eb-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a06eb-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a06eb-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a06eb-139">Response</span></span>
<span data-ttu-id="a06eb-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a06eb-140">If successful, this method returns a `200 OK` response code and an updated [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a06eb-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a06eb-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="a06eb-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a06eb-142">Request</span></span>
<span data-ttu-id="a06eb-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a06eb-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments/{officeClientConfigurationAssignmentId}
Content-type: application/json
Content-length: 98

{
  "target": {
    "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="a06eb-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a06eb-144">Response</span></span>
<span data-ttu-id="a06eb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a06eb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
  "id": "804730f3-30f3-8047-f330-4780f3304780",
  "target": {
    "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
  }
}
```



