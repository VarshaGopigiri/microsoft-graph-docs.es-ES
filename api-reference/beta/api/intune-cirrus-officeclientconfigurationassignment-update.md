---
title: Actualizar officeClientConfigurationAssignment
description: Actualizar las propiedades de un objeto officeClientConfigurationAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d76fd4808c6a9b28151d2487bfb7c6b2afcc7c60
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935195"
---
# <a name="update-officeclientconfigurationassignment"></a><span data-ttu-id="f9776-103">Actualizar officeClientConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f9776-103">Update officeClientConfigurationAssignment</span></span>

> <span data-ttu-id="f9776-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9776-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9776-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9776-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f9776-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9776-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9776-107">Actualizar las propiedades de un objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="f9776-107">Update the properties of a [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9776-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9776-108">Prerequisites</span></span>
<span data-ttu-id="f9776-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9776-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9776-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9776-111">Permission type</span></span>|<span data-ttu-id="f9776-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9776-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9776-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9776-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f9776-114">\*\* TODO: Determinar los ámbitos \*\*</span><span class="sxs-lookup"><span data-stu-id="f9776-114">\*\*TODO: Determine scopes \*\*</span></span>|
|<span data-ttu-id="f9776-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9776-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9776-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9776-116">Not supported.</span></span>|
|<span data-ttu-id="f9776-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9776-117">Application</span></span>|<span data-ttu-id="f9776-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9776-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9776-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9776-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /officeConfiguration/clientConfigurations/{officeClientConfigurationId}/assignments/{officeClientConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="f9776-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9776-120">Request headers</span></span>
|<span data-ttu-id="f9776-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9776-121">Header</span></span>|<span data-ttu-id="f9776-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f9776-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9776-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f9776-123">Authorization</span></span>|<span data-ttu-id="f9776-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f9776-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f9776-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f9776-125">Accept</span></span>|<span data-ttu-id="f9776-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f9776-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9776-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9776-127">Request body</span></span>
<span data-ttu-id="f9776-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="f9776-128">In the request body, supply a JSON representation for the [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object.</span></span>

<span data-ttu-id="f9776-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="f9776-129">The following table shows the properties that are required when you create the [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md).</span></span>

|<span data-ttu-id="f9776-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9776-130">Property</span></span>|<span data-ttu-id="f9776-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9776-131">Type</span></span>|<span data-ttu-id="f9776-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9776-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f9776-133">id</span><span class="sxs-lookup"><span data-stu-id="f9776-133">id</span></span>|<span data-ttu-id="f9776-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9776-134">String</span></span>|<span data-ttu-id="f9776-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f9776-135">Not yet documented</span></span>|
|<span data-ttu-id="f9776-136">target</span><span class="sxs-lookup"><span data-stu-id="f9776-136">target</span></span>|[<span data-ttu-id="f9776-137">officeConfigurationAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="f9776-137">officeConfigurationAssignmentTarget</span></span>](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)|<span data-ttu-id="f9776-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f9776-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="f9776-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9776-139">Response</span></span>
<span data-ttu-id="f9776-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9776-140">If successful, this method returns a `200 OK` response code and an updated [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9776-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9776-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="f9776-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9776-142">Request</span></span>
<span data-ttu-id="f9776-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9776-143">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f9776-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9776-144">Response</span></span>
<span data-ttu-id="f9776-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9776-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



