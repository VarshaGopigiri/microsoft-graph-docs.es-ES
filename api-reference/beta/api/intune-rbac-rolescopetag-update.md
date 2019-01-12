---
title: Actualizar roleScopeTag
description: Actualizar las propiedades de un objeto roleScopeTag.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ec006889750999bf2a61aaefd6fba7bc5b747999
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933525"
---
# <a name="update-rolescopetag"></a><span data-ttu-id="03e4c-103">Actualizar roleScopeTag</span><span class="sxs-lookup"><span data-stu-id="03e4c-103">Update roleScopeTag</span></span>

> <span data-ttu-id="03e4c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="03e4c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03e4c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03e4c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="03e4c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03e4c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03e4c-107">Actualizar las propiedades de un objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="03e4c-107">Update the properties of a [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03e4c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03e4c-108">Prerequisites</span></span>
<span data-ttu-id="03e4c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03e4c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03e4c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03e4c-111">Permission type</span></span>|<span data-ttu-id="03e4c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03e4c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03e4c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03e4c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="03e4c-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03e4c-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="03e4c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03e4c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03e4c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03e4c-116">Not supported.</span></span>|
|<span data-ttu-id="03e4c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03e4c-117">Application</span></span>|<span data-ttu-id="03e4c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03e4c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03e4c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03e4c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleScopeTags/{roleScopeTagId}
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/microsoft.graph.deviceAndAppManagementRoleAssignment/roleScopeTags/{roleScopeTagId}
```

## <a name="request-headers"></a><span data-ttu-id="03e4c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03e4c-120">Request headers</span></span>
|<span data-ttu-id="03e4c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03e4c-121">Header</span></span>|<span data-ttu-id="03e4c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="03e4c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03e4c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="03e4c-123">Authorization</span></span>|<span data-ttu-id="03e4c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03e4c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03e4c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="03e4c-125">Accept</span></span>|<span data-ttu-id="03e4c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="03e4c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03e4c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03e4c-127">Request body</span></span>
<span data-ttu-id="03e4c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="03e4c-128">In the request body, supply a JSON representation for the [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>

<span data-ttu-id="03e4c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [roleScopeTag](../resources/intune-rbac-rolescopetag.md).</span><span class="sxs-lookup"><span data-stu-id="03e4c-129">The following table shows the properties that are required when you create the [roleScopeTag](../resources/intune-rbac-rolescopetag.md).</span></span>

|<span data-ttu-id="03e4c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="03e4c-130">Property</span></span>|<span data-ttu-id="03e4c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="03e4c-131">Type</span></span>|<span data-ttu-id="03e4c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="03e4c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="03e4c-133">id</span><span class="sxs-lookup"><span data-stu-id="03e4c-133">id</span></span>|<span data-ttu-id="03e4c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="03e4c-134">String</span></span>|<span data-ttu-id="03e4c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="03e4c-135">Key of the entity.</span></span> <span data-ttu-id="03e4c-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="03e4c-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="03e4c-137">displayName</span><span class="sxs-lookup"><span data-stu-id="03e4c-137">displayName</span></span>|<span data-ttu-id="03e4c-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="03e4c-138">String</span></span>|<span data-ttu-id="03e4c-139">El para mostrar o el nombre descriptivo de la etiqueta de ámbito de función.</span><span class="sxs-lookup"><span data-stu-id="03e4c-139">The display or friendly name of the Role Scope Tag.</span></span>|
|<span data-ttu-id="03e4c-140">descripción</span><span class="sxs-lookup"><span data-stu-id="03e4c-140">description</span></span>|<span data-ttu-id="03e4c-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="03e4c-141">String</span></span>|<span data-ttu-id="03e4c-142">Descripción de la etiqueta de ámbito de función.</span><span class="sxs-lookup"><span data-stu-id="03e4c-142">Description of the Role Scope Tag.</span></span>|



## <a name="response"></a><span data-ttu-id="03e4c-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03e4c-143">Response</span></span>
<span data-ttu-id="03e4c-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [roleScopeTag](../resources/intune-rbac-rolescopetag.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03e4c-144">If successful, this method returns a `200 OK` response code and an updated [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03e4c-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03e4c-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="03e4c-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03e4c-146">Request</span></span>
<span data-ttu-id="03e4c-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03e4c-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/roleScopeTags/{roleScopeTagId}
Content-type: application/json
Content-length: 82

{
  "displayName": "Display Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="03e4c-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03e4c-148">Response</span></span>
<span data-ttu-id="03e4c-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03e4c-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 182

{
  "@odata.type": "#microsoft.graph.roleScopeTag",
  "id": "9ed1e179-e179-9ed1-79e1-d19e79e1d19e",
  "displayName": "Display Name value",
  "description": "Description value"
}
```





