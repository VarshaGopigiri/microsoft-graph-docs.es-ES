---
title: Crear officeClientConfigurationAssignment
description: Agregar un grupo de destino a una directiva existente.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 24eee1797c00fd6ef6e380e2fdde20c5147567af
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858698"
---
# <a name="create-officeclientconfigurationassignment"></a><span data-ttu-id="a195d-103">Crear officeClientConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a195d-103">Create officeClientConfigurationAssignment</span></span>

> <span data-ttu-id="a195d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a195d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a195d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a195d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a195d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a195d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a195d-107">Agregar un grupo de destino a una directiva existente.</span><span class="sxs-lookup"><span data-stu-id="a195d-107">Add a target group to an existing policy.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a195d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a195d-108">Prerequisites</span></span>
<span data-ttu-id="a195d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a195d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a195d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a195d-111">Permission type</span></span>|<span data-ttu-id="a195d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a195d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a195d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a195d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a195d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a195d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a195d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a195d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a195d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a195d-116">Not supported.</span></span>|
|<span data-ttu-id="a195d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a195d-117">Application</span></span>|<span data-ttu-id="a195d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a195d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a195d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a195d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /officeConfiguration/clientConfigurations/{key}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="a195d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a195d-120">Request headers</span></span>
|<span data-ttu-id="a195d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a195d-121">Header</span></span>|<span data-ttu-id="a195d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a195d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a195d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a195d-123">Authorization</span></span>|<span data-ttu-id="a195d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a195d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a195d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a195d-125">Accept</span></span>|<span data-ttu-id="a195d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a195d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a195d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a195d-127">Request body</span></span>
<span data-ttu-id="a195d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto officeClientConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="a195d-128">In the request body, supply a JSON representation for the officeClientConfigurationAssignment object.</span></span>

<span data-ttu-id="a195d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el officeClientConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="a195d-129">The following table shows the properties that are required when you create the officeClientConfigurationAssignment.</span></span>

|<span data-ttu-id="a195d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a195d-130">Property</span></span>|<span data-ttu-id="a195d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a195d-131">Type</span></span>|<span data-ttu-id="a195d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a195d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a195d-133">id</span><span class="sxs-lookup"><span data-stu-id="a195d-133">id</span></span>|<span data-ttu-id="a195d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a195d-134">String</span></span>|<span data-ttu-id="a195d-135">Identificador de la OfficeConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="a195d-135">Id of the OfficeConfigurationAssignment.</span></span>|
|<span data-ttu-id="a195d-136">target</span><span class="sxs-lookup"><span data-stu-id="a195d-136">target</span></span>|[<span data-ttu-id="a195d-137">officeConfigurationAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="a195d-137">officeConfigurationAssignmentTarget</span></span>](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)|<span data-ttu-id="a195d-138">La asignación de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="a195d-138">The target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="a195d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a195d-139">Response</span></span>
<span data-ttu-id="a195d-140">Si tiene éxito, este método devuelve una `200 Created` código de respuesta y un objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a195d-140">If successful, this method returns a `200 Created` response code and a [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a195d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a195d-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="a195d-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a195d-142">Request</span></span>
<span data-ttu-id="a195d-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a195d-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{key}/assignments
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="a195d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a195d-144">Response</span></span>
<span data-ttu-id="a195d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a195d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



