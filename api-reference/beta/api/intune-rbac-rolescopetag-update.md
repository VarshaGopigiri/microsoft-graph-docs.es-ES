---
title: Actualizar roleScopeTag
description: Actualizar las propiedades de un objeto roleScopeTag.
ms.openlocfilehash: d18f4f47be9aab01b1221e9ce7736878bb059bed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089663"
---
# <a name="update-rolescopetag"></a><span data-ttu-id="46f76-103">Actualizar roleScopeTag</span><span class="sxs-lookup"><span data-stu-id="46f76-103">Update roleScopeTag</span></span>

> <span data-ttu-id="46f76-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46f76-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46f76-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46f76-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46f76-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46f76-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46f76-107">Actualizar las propiedades de un objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="46f76-107">Update the properties of a [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46f76-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46f76-108">Prerequisites</span></span>
<span data-ttu-id="46f76-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="46f76-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46f76-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46f76-111">Permission type</span></span>|<span data-ttu-id="46f76-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46f76-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46f76-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46f76-113">Delegated (work or school account)</span></span>|<span data-ttu-id="46f76-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46f76-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="46f76-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46f76-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46f76-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46f76-116">Not supported.</span></span>|
|<span data-ttu-id="46f76-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46f76-117">Application</span></span>|<span data-ttu-id="46f76-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46f76-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46f76-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46f76-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleScopeTags/{roleScopeTagId}
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/microsoft.graph.deviceAndAppManagementRoleAssignment/roleScopeTags/{roleScopeTagId}
```

## <a name="request-headers"></a><span data-ttu-id="46f76-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46f76-120">Request headers</span></span>
|<span data-ttu-id="46f76-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46f76-121">Header</span></span>|<span data-ttu-id="46f76-122">Valor</span><span class="sxs-lookup"><span data-stu-id="46f76-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46f76-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="46f76-123">Authorization</span></span>|<span data-ttu-id="46f76-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46f76-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46f76-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="46f76-125">Accept</span></span>|<span data-ttu-id="46f76-126">application/json</span><span class="sxs-lookup"><span data-stu-id="46f76-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46f76-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46f76-127">Request body</span></span>
<span data-ttu-id="46f76-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="46f76-128">In the request body, supply a JSON representation for the [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>

<span data-ttu-id="46f76-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [roleScopeTag](../resources/intune-rbac-rolescopetag.md).</span><span class="sxs-lookup"><span data-stu-id="46f76-129">The following table shows the properties that are required when you create the [roleScopeTag](../resources/intune-rbac-rolescopetag.md).</span></span>

|<span data-ttu-id="46f76-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46f76-130">Property</span></span>|<span data-ttu-id="46f76-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="46f76-131">Type</span></span>|<span data-ttu-id="46f76-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="46f76-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46f76-133">id</span><span class="sxs-lookup"><span data-stu-id="46f76-133">id</span></span>|<span data-ttu-id="46f76-134">String</span><span class="sxs-lookup"><span data-stu-id="46f76-134">String</span></span>|<span data-ttu-id="46f76-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="46f76-135">Key of the entity.</span></span> <span data-ttu-id="46f76-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="46f76-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="46f76-137">displayName</span><span class="sxs-lookup"><span data-stu-id="46f76-137">displayName</span></span>|<span data-ttu-id="46f76-138">String</span><span class="sxs-lookup"><span data-stu-id="46f76-138">String</span></span>|<span data-ttu-id="46f76-139">El para mostrar o el nombre descriptivo de la etiqueta de ámbito de función.</span><span class="sxs-lookup"><span data-stu-id="46f76-139">The display or friendly name of the Role Scope Tag.</span></span>|
|<span data-ttu-id="46f76-140">descripción</span><span class="sxs-lookup"><span data-stu-id="46f76-140">description</span></span>|<span data-ttu-id="46f76-141">String</span><span class="sxs-lookup"><span data-stu-id="46f76-141">String</span></span>|<span data-ttu-id="46f76-142">Descripción de la etiqueta de ámbito de función.</span><span class="sxs-lookup"><span data-stu-id="46f76-142">Description of the Role Scope Tag.</span></span>|



## <a name="response"></a><span data-ttu-id="46f76-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46f76-143">Response</span></span>
<span data-ttu-id="46f76-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [roleScopeTag](../resources/intune-rbac-rolescopetag.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46f76-144">If successful, this method returns a `200 OK` response code and an updated [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46f76-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46f76-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="46f76-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46f76-146">Request</span></span>
<span data-ttu-id="46f76-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46f76-147">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/roleScopeTags/{roleScopeTagId}
Content-type: application/json
Content-length: 82

{
  "displayName": "Display Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="46f76-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46f76-148">Response</span></span>
<span data-ttu-id="46f76-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46f76-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





