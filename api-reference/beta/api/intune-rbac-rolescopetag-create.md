---
title: Crear roleScopeTag
description: Crear un nuevo objeto roleScopeTag.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 314e9c6fb05f51efb6e2af6ad62faf25974fe3b4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915161"
---
# <a name="create-rolescopetag"></a><span data-ttu-id="37047-103">Crear roleScopeTag</span><span class="sxs-lookup"><span data-stu-id="37047-103">Create roleScopeTag</span></span>

> <span data-ttu-id="37047-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37047-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37047-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37047-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37047-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37047-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37047-107">Crear un nuevo objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) .</span><span class="sxs-lookup"><span data-stu-id="37047-107">Create a new [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="37047-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37047-108">Prerequisites</span></span>
<span data-ttu-id="37047-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37047-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37047-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37047-111">Permission type</span></span>|<span data-ttu-id="37047-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37047-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="37047-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37047-113">Delegated (work or school account)</span></span>|<span data-ttu-id="37047-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="37047-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="37047-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37047-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="37047-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37047-116">Not supported.</span></span>|
|<span data-ttu-id="37047-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37047-117">Application</span></span>|<span data-ttu-id="37047-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37047-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="37047-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37047-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleScopeTags
POST /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/microsoft.graph.deviceAndAppManagementRoleAssignment/roleScopeTags
```

## <a name="request-headers"></a><span data-ttu-id="37047-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37047-120">Request headers</span></span>
|<span data-ttu-id="37047-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37047-121">Header</span></span>|<span data-ttu-id="37047-122">Valor</span><span class="sxs-lookup"><span data-stu-id="37047-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="37047-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="37047-123">Authorization</span></span>|<span data-ttu-id="37047-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="37047-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="37047-125">Accept</span><span class="sxs-lookup"><span data-stu-id="37047-125">Accept</span></span>|<span data-ttu-id="37047-126">application/json</span><span class="sxs-lookup"><span data-stu-id="37047-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="37047-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37047-127">Request body</span></span>
<span data-ttu-id="37047-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto roleScopeTag.</span><span class="sxs-lookup"><span data-stu-id="37047-128">In the request body, supply a JSON representation for the roleScopeTag object.</span></span>

<span data-ttu-id="37047-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el roleScopeTag.</span><span class="sxs-lookup"><span data-stu-id="37047-129">The following table shows the properties that are required when you create the roleScopeTag.</span></span>

|<span data-ttu-id="37047-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37047-130">Property</span></span>|<span data-ttu-id="37047-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="37047-131">Type</span></span>|<span data-ttu-id="37047-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="37047-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37047-133">id</span><span class="sxs-lookup"><span data-stu-id="37047-133">id</span></span>|<span data-ttu-id="37047-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="37047-134">String</span></span>|<span data-ttu-id="37047-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="37047-135">Key of the entity.</span></span> <span data-ttu-id="37047-136">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="37047-136">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="37047-137">displayName</span><span class="sxs-lookup"><span data-stu-id="37047-137">displayName</span></span>|<span data-ttu-id="37047-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="37047-138">String</span></span>|<span data-ttu-id="37047-139">El para mostrar o el nombre descriptivo de la etiqueta de ámbito de función.</span><span class="sxs-lookup"><span data-stu-id="37047-139">The display or friendly name of the Role Scope Tag.</span></span>|
|<span data-ttu-id="37047-140">descripción</span><span class="sxs-lookup"><span data-stu-id="37047-140">description</span></span>|<span data-ttu-id="37047-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="37047-141">String</span></span>|<span data-ttu-id="37047-142">Descripción de la etiqueta de ámbito de función.</span><span class="sxs-lookup"><span data-stu-id="37047-142">Description of the Role Scope Tag.</span></span>|



## <a name="response"></a><span data-ttu-id="37047-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37047-143">Response</span></span>
<span data-ttu-id="37047-144">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [roleScopeTag](../resources/intune-rbac-rolescopetag.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37047-144">If successful, this method returns a `201 Created` response code and a [roleScopeTag](../resources/intune-rbac-rolescopetag.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37047-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37047-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="37047-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37047-146">Request</span></span>
<span data-ttu-id="37047-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37047-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/roleScopeTags
Content-type: application/json
Content-length: 133

{
  "@odata.type": "#microsoft.graph.roleScopeTag",
  "displayName": "Display Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="37047-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37047-148">Response</span></span>
<span data-ttu-id="37047-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37047-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 182

{
  "@odata.type": "#microsoft.graph.roleScopeTag",
  "id": "9ed1e179-e179-9ed1-79e1-d19e79e1d19e",
  "displayName": "Display Name value",
  "description": "Description value"
}
```





