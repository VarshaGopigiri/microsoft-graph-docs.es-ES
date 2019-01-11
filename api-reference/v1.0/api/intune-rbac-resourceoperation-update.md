---
title: Actualizar resourceOperation
description: Actualice las propiedades de un objeto resourceOperation.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 97457b82bb74891ef4d709809efcae2d171df670
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830411"
---
# <a name="update-resourceoperation"></a><span data-ttu-id="91ba4-103">Actualizar resourceOperation</span><span class="sxs-lookup"><span data-stu-id="91ba4-103">Update resourceOperation</span></span>

> <span data-ttu-id="91ba4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="91ba4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="91ba4-105">Actualice las propiedades de un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="91ba4-105">Update the properties of a [resourceOperation](../resources/intune-rbac-resourceoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="91ba4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="91ba4-106">Prerequisites</span></span>
<span data-ttu-id="91ba4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91ba4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="91ba4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="91ba4-109">Permission type</span></span>|<span data-ttu-id="91ba4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="91ba4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="91ba4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="91ba4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="91ba4-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="91ba4-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="91ba4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="91ba4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="91ba4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="91ba4-114">Not supported.</span></span>|
|<span data-ttu-id="91ba4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="91ba4-115">Application</span></span>|<span data-ttu-id="91ba4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="91ba4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="91ba4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91ba4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/resourceOperations/{resourceOperationId}
```

## <a name="request-headers"></a><span data-ttu-id="91ba4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91ba4-118">Request headers</span></span>
|<span data-ttu-id="91ba4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91ba4-119">Header</span></span>|<span data-ttu-id="91ba4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="91ba4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="91ba4-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="91ba4-121">Authorization</span></span>|<span data-ttu-id="91ba4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="91ba4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="91ba4-123">Accept</span><span class="sxs-lookup"><span data-stu-id="91ba4-123">Accept</span></span>|<span data-ttu-id="91ba4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="91ba4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="91ba4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="91ba4-125">Request body</span></span>
<span data-ttu-id="91ba4-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="91ba4-126">In the request body, supply a JSON representation for the [resourceOperation](../resources/intune-rbac-resourceoperation.md) object.</span></span>

<span data-ttu-id="91ba4-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="91ba4-127">The following table shows the properties that are required when you create the [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span></span>

|<span data-ttu-id="91ba4-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91ba4-128">Property</span></span>|<span data-ttu-id="91ba4-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="91ba4-129">Type</span></span>|<span data-ttu-id="91ba4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="91ba4-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="91ba4-131">id</span><span class="sxs-lookup"><span data-stu-id="91ba4-131">id</span></span>|<span data-ttu-id="91ba4-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="91ba4-132">String</span></span>|<span data-ttu-id="91ba4-133">Clave de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="91ba4-133">Key of the Resource Operation.</span></span> <span data-ttu-id="91ba4-134">Solo lectura, generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="91ba4-134">Read-only, automatically generated.</span></span>|
|<span data-ttu-id="91ba4-135">resourceName</span><span class="sxs-lookup"><span data-stu-id="91ba4-135">resourceName</span></span>|<span data-ttu-id="91ba4-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="91ba4-136">String</span></span>|<span data-ttu-id="91ba4-137">Nombre del recurso en el que se realiza esta operación.</span><span class="sxs-lookup"><span data-stu-id="91ba4-137">Name of the Resource this operation is performed on.</span></span>|
|<span data-ttu-id="91ba4-138">actionName</span><span class="sxs-lookup"><span data-stu-id="91ba4-138">actionName</span></span>|<span data-ttu-id="91ba4-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="91ba4-139">String</span></span>|<span data-ttu-id="91ba4-140">Tipo de acción que va a realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="91ba4-140">Type of action this operation is going to perform.</span></span> <span data-ttu-id="91ba4-141">El actionName debe ser conciso y limitado al menor número de palabras posible.</span><span class="sxs-lookup"><span data-stu-id="91ba4-141">The actionName should be concise and limited to as few words as possible.</span></span>|
|<span data-ttu-id="91ba4-142">description</span><span class="sxs-lookup"><span data-stu-id="91ba4-142">description</span></span>|<span data-ttu-id="91ba4-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="91ba4-143">String</span></span>|<span data-ttu-id="91ba4-144">Descripción de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="91ba4-144">Description of the resource operation.</span></span> <span data-ttu-id="91ba4-145">La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="91ba4-145">The description is used in mouse-over text for the operation when shown in the Azure Portal.</span></span>|



## <a name="response"></a><span data-ttu-id="91ba4-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91ba4-146">Response</span></span>
<span data-ttu-id="91ba4-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91ba4-147">If successful, this method returns a `200 OK` response code and an updated [resourceOperation](../resources/intune-rbac-resourceoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="91ba4-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91ba4-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="91ba4-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91ba4-149">Request</span></span>
<span data-ttu-id="91ba4-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="91ba4-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/resourceOperations/{resourceOperationId}
Content-type: application/json
Content-length: 178

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="91ba4-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91ba4-151">Response</span></span>
<span data-ttu-id="91ba4-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="91ba4-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 227

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "id": "232b8fee-8fee-232b-ee8f-2b23ee8f2b23",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value"
}
```



