---
title: Crear resourceOperation
description: Cree un objeto resourceOperation.
ms.openlocfilehash: 40f8c7175c5f6ad5e2885fe7e893bba118458be1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030512"
---
# <a name="create-resourceoperation"></a><span data-ttu-id="8dff0-103">Crear resourceOperation</span><span class="sxs-lookup"><span data-stu-id="8dff0-103">Create resourceOperation</span></span>

> <span data-ttu-id="8dff0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8dff0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8dff0-105">Cree un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="8dff0-105">Create a new [resourceOperation](../resources/intune-rbac-resourceoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8dff0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8dff0-106">Prerequisites</span></span>
<span data-ttu-id="8dff0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8dff0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8dff0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8dff0-109">Permission type</span></span>|<span data-ttu-id="8dff0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8dff0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8dff0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8dff0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8dff0-112">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8dff0-112">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="8dff0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8dff0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8dff0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8dff0-114">Not supported.</span></span>|
|<span data-ttu-id="8dff0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8dff0-115">Application</span></span>|<span data-ttu-id="8dff0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8dff0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8dff0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8dff0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/resourceOperations
```

## <a name="request-headers"></a><span data-ttu-id="8dff0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8dff0-118">Request headers</span></span>
|<span data-ttu-id="8dff0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dff0-119">Header</span></span>|<span data-ttu-id="8dff0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8dff0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8dff0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8dff0-121">Authorization</span></span>|<span data-ttu-id="8dff0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8dff0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8dff0-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8dff0-123">Accept</span></span>|<span data-ttu-id="8dff0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8dff0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8dff0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8dff0-125">Request body</span></span>
<span data-ttu-id="8dff0-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto resourceOperation.</span><span class="sxs-lookup"><span data-stu-id="8dff0-126">In the request body, supply a JSON representation for the resourceOperation object.</span></span>

<span data-ttu-id="8dff0-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto resourceOperation.</span><span class="sxs-lookup"><span data-stu-id="8dff0-127">The following table shows the properties that are required when you create the resourceOperation.</span></span>

|<span data-ttu-id="8dff0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8dff0-128">Property</span></span>|<span data-ttu-id="8dff0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8dff0-129">Type</span></span>|<span data-ttu-id="8dff0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dff0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8dff0-131">id</span><span class="sxs-lookup"><span data-stu-id="8dff0-131">id</span></span>|<span data-ttu-id="8dff0-132">String</span><span class="sxs-lookup"><span data-stu-id="8dff0-132">String</span></span>|<span data-ttu-id="8dff0-133">Clave de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dff0-133">Key of the Resource Operation.</span></span> <span data-ttu-id="8dff0-134">Solo lectura, generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8dff0-134">Read-only, automatically generated.</span></span>|
|<span data-ttu-id="8dff0-135">resourceName</span><span class="sxs-lookup"><span data-stu-id="8dff0-135">resourceName</span></span>|<span data-ttu-id="8dff0-136">String</span><span class="sxs-lookup"><span data-stu-id="8dff0-136">String</span></span>|<span data-ttu-id="8dff0-137">Nombre del recurso en el que se realiza esta operación.</span><span class="sxs-lookup"><span data-stu-id="8dff0-137">Name of the Resource this operation is performed on.</span></span>|
|<span data-ttu-id="8dff0-138">actionName</span><span class="sxs-lookup"><span data-stu-id="8dff0-138">actionName</span></span>|<span data-ttu-id="8dff0-139">String</span><span class="sxs-lookup"><span data-stu-id="8dff0-139">String</span></span>|<span data-ttu-id="8dff0-140">Tipo de acción que va a realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="8dff0-140">Type of action this operation is going to perform.</span></span> <span data-ttu-id="8dff0-141">El actionName debe ser conciso y limitado al menor número de palabras posible.</span><span class="sxs-lookup"><span data-stu-id="8dff0-141">The actionName should be concise and limited to as few words as possible.</span></span>|
|<span data-ttu-id="8dff0-142">description</span><span class="sxs-lookup"><span data-stu-id="8dff0-142">description</span></span>|<span data-ttu-id="8dff0-143">String</span><span class="sxs-lookup"><span data-stu-id="8dff0-143">String</span></span>|<span data-ttu-id="8dff0-144">Descripción de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dff0-144">Description of the resource operation.</span></span> <span data-ttu-id="8dff0-145">La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="8dff0-145">The description is used in mouse-over text for the operation when shown in the Azure Portal.</span></span>|



## <a name="response"></a><span data-ttu-id="8dff0-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8dff0-146">Response</span></span>
<span data-ttu-id="8dff0-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8dff0-147">If successful, this method returns a `201 Created` response code and a [resourceOperation](../resources/intune-rbac-resourceoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8dff0-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8dff0-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="8dff0-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8dff0-149">Request</span></span>
<span data-ttu-id="8dff0-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8dff0-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/resourceOperations
Content-type: application/json
Content-length: 178

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="8dff0-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8dff0-151">Response</span></span>
<span data-ttu-id="8dff0-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8dff0-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



