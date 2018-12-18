---
title: Actualizar resourceOperation
description: Actualice las propiedades de un objeto resourceOperation.
author: tfitzmac
ms.openlocfilehash: 8050b91aee679f9dd29e78cbbad62f9f6352343e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317825"
---
# <a name="update-resourceoperation"></a><span data-ttu-id="d6171-103">Actualizar resourceOperation</span><span class="sxs-lookup"><span data-stu-id="d6171-103">Update resourceOperation</span></span>

> <span data-ttu-id="d6171-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d6171-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d6171-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d6171-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d6171-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d6171-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d6171-107">Actualice las propiedades de un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="d6171-107">Update the properties of a [resourceOperation](../resources/intune-rbac-resourceoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d6171-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d6171-108">Prerequisites</span></span>
<span data-ttu-id="d6171-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6171-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d6171-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6171-111">Permission type</span></span>|<span data-ttu-id="d6171-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6171-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d6171-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6171-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d6171-114">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6171-114">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="d6171-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6171-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d6171-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6171-116">Not supported.</span></span>|
|<span data-ttu-id="d6171-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6171-117">Application</span></span>|<span data-ttu-id="d6171-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6171-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d6171-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6171-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/resourceOperations/{resourceOperationId}
```

## <a name="request-headers"></a><span data-ttu-id="d6171-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6171-120">Request headers</span></span>
|<span data-ttu-id="d6171-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6171-121">Header</span></span>|<span data-ttu-id="d6171-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d6171-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d6171-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d6171-123">Authorization</span></span>|<span data-ttu-id="d6171-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d6171-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d6171-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d6171-125">Accept</span></span>|<span data-ttu-id="d6171-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d6171-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d6171-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6171-127">Request body</span></span>
<span data-ttu-id="d6171-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="d6171-128">In the request body, supply a JSON representation for the [resourceOperation](../resources/intune-rbac-resourceoperation.md) object.</span></span>

<span data-ttu-id="d6171-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="d6171-129">The following table shows the properties that are required when you create the [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span></span>

|<span data-ttu-id="d6171-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6171-130">Property</span></span>|<span data-ttu-id="d6171-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6171-131">Type</span></span>|<span data-ttu-id="d6171-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6171-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d6171-133">id</span><span class="sxs-lookup"><span data-stu-id="d6171-133">id</span></span>|<span data-ttu-id="d6171-134">String</span><span class="sxs-lookup"><span data-stu-id="d6171-134">String</span></span>|<span data-ttu-id="d6171-135">Clave de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6171-135">Key of the Resource Operation.</span></span> <span data-ttu-id="d6171-136">Solo lectura, generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d6171-136">Read-only, automatically generated.</span></span>|
|<span data-ttu-id="d6171-137">resource</span><span class="sxs-lookup"><span data-stu-id="d6171-137">resource</span></span>|<span data-ttu-id="d6171-138">String</span><span class="sxs-lookup"><span data-stu-id="d6171-138">String</span></span>|<span data-ttu-id="d6171-139">Categoría de recurso al que pertenece esta operación.</span><span class="sxs-lookup"><span data-stu-id="d6171-139">Resource category to which this Operation belongs.</span></span>|
|<span data-ttu-id="d6171-140">resourceName</span><span class="sxs-lookup"><span data-stu-id="d6171-140">resourceName</span></span>|<span data-ttu-id="d6171-141">String</span><span class="sxs-lookup"><span data-stu-id="d6171-141">String</span></span>|<span data-ttu-id="d6171-142">Nombre del recurso en el que se realiza esta operación.</span><span class="sxs-lookup"><span data-stu-id="d6171-142">Name of the Resource this operation is performed on.</span></span>|
|<span data-ttu-id="d6171-143">actionName</span><span class="sxs-lookup"><span data-stu-id="d6171-143">actionName</span></span>|<span data-ttu-id="d6171-144">String</span><span class="sxs-lookup"><span data-stu-id="d6171-144">String</span></span>|<span data-ttu-id="d6171-145">Tipo de acción que va a realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="d6171-145">Type of action this operation is going to perform.</span></span> <span data-ttu-id="d6171-146">El actionName debe ser conciso y limitado al menor número de palabras posible.</span><span class="sxs-lookup"><span data-stu-id="d6171-146">The actionName should be concise and limited to as few words as possible.</span></span>|
|<span data-ttu-id="d6171-147">description</span><span class="sxs-lookup"><span data-stu-id="d6171-147">description</span></span>|<span data-ttu-id="d6171-148">String</span><span class="sxs-lookup"><span data-stu-id="d6171-148">String</span></span>|<span data-ttu-id="d6171-149">Descripción de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6171-149">Description of the resource operation.</span></span> <span data-ttu-id="d6171-150">La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="d6171-150">The description is used in mouse-over text for the operation when shown in the Azure Portal.</span></span>|
|<span data-ttu-id="d6171-151">enabledForScopeValidation</span><span class="sxs-lookup"><span data-stu-id="d6171-151">enabledForScopeValidation</span></span>|<span data-ttu-id="d6171-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="d6171-152">Boolean</span></span>|<span data-ttu-id="d6171-153">Determina si el permiso se valida para ámbitos definidos por la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="d6171-153">Determines whether the Permission is validated for Scopes defined per Role Assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="d6171-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6171-154">Response</span></span>
<span data-ttu-id="d6171-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6171-155">If successful, this method returns a `200 OK` response code and an updated [resourceOperation](../resources/intune-rbac-resourceoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6171-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6171-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="d6171-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6171-157">Request</span></span>
<span data-ttu-id="d6171-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6171-158">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/resourceOperations/{resourceOperationId}
Content-type: application/json
Content-length: 193

{
  "resource": "Resource value",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value",
  "enabledForScopeValidation": true
}
```

### <a name="response"></a><span data-ttu-id="d6171-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6171-159">Response</span></span>
<span data-ttu-id="d6171-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6171-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 298

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "id": "232b8fee-8fee-232b-ee8f-2b23ee8f2b23",
  "resource": "Resource value",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value",
  "enabledForScopeValidation": true
}
```





