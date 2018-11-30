---
title: Crear officeClientConfigurationAssignment
description: Agregar un grupo de destino a una directiva existente.
ms.openlocfilehash: 60416fe200214864c063a9fae739d5f7bd436a69
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086197"
---
# <a name="create-officeclientconfigurationassignment"></a><span data-ttu-id="04c77-103">Crear officeClientConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="04c77-103">Create officeClientConfigurationAssignment</span></span>

> <span data-ttu-id="04c77-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04c77-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04c77-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04c77-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="04c77-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04c77-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04c77-107">Agregar un grupo de destino a una directiva existente.</span><span class="sxs-lookup"><span data-stu-id="04c77-107">Add a target group to an existing policy.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="04c77-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="04c77-108">Prerequisites</span></span>
<span data-ttu-id="04c77-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="04c77-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="04c77-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04c77-111">Permission type</span></span>|<span data-ttu-id="04c77-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04c77-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="04c77-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04c77-113">Delegated (work or school account)</span></span>|<span data-ttu-id="04c77-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04c77-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="04c77-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04c77-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="04c77-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04c77-116">Not supported.</span></span>|
|<span data-ttu-id="04c77-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04c77-117">Application</span></span>|<span data-ttu-id="04c77-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04c77-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="04c77-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04c77-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /officeConfiguration/clientConfigurations/{key}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="04c77-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04c77-120">Request headers</span></span>
|<span data-ttu-id="04c77-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04c77-121">Header</span></span>|<span data-ttu-id="04c77-122">Valor</span><span class="sxs-lookup"><span data-stu-id="04c77-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="04c77-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="04c77-123">Authorization</span></span>|<span data-ttu-id="04c77-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="04c77-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="04c77-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="04c77-125">Accept</span></span>|<span data-ttu-id="04c77-126">application/json</span><span class="sxs-lookup"><span data-stu-id="04c77-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="04c77-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04c77-127">Request body</span></span>
<span data-ttu-id="04c77-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto officeClientConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="04c77-128">In the request body, supply a JSON representation for the officeClientConfigurationAssignment object.</span></span>

<span data-ttu-id="04c77-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el officeClientConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="04c77-129">The following table shows the properties that are required when you create the officeClientConfigurationAssignment.</span></span>

|<span data-ttu-id="04c77-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04c77-130">Property</span></span>|<span data-ttu-id="04c77-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="04c77-131">Type</span></span>|<span data-ttu-id="04c77-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="04c77-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04c77-133">id</span><span class="sxs-lookup"><span data-stu-id="04c77-133">id</span></span>|<span data-ttu-id="04c77-134">String</span><span class="sxs-lookup"><span data-stu-id="04c77-134">String</span></span>|<span data-ttu-id="04c77-135">Identificador de la OfficeConfigurationAssignment.</span><span class="sxs-lookup"><span data-stu-id="04c77-135">Id of the OfficeConfigurationAssignment.</span></span>|
|<span data-ttu-id="04c77-136">target</span><span class="sxs-lookup"><span data-stu-id="04c77-136">target</span></span>|[<span data-ttu-id="04c77-137">officeConfigurationAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="04c77-137">officeConfigurationAssignmentTarget</span></span>](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)|<span data-ttu-id="04c77-138">La asignación de destino definida por el administrador.</span><span class="sxs-lookup"><span data-stu-id="04c77-138">The target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="04c77-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04c77-139">Response</span></span>
<span data-ttu-id="04c77-140">Si tiene éxito, este método devuelve una `200 Created` código de respuesta y un objeto [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04c77-140">If successful, this method returns a `200 Created` response code and a [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04c77-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04c77-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="04c77-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04c77-142">Request</span></span>
<span data-ttu-id="04c77-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04c77-143">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="04c77-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04c77-144">Response</span></span>
<span data-ttu-id="04c77-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04c77-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


