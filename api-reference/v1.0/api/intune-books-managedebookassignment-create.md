---
title: Crear managedEBookAssignment
description: Cree un objeto managedEBookAssignment.
ms.openlocfilehash: c471362f9f3cfddb9aa2cd3779ac66d28ec5d198
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032164"
---
# <a name="create-managedebookassignment"></a><span data-ttu-id="25fce-103">Crear managedEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="25fce-103">Create managedEBookAssignment</span></span>

> <span data-ttu-id="25fce-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25fce-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25fce-105">Cree un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="25fce-105">Create a new [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="25fce-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25fce-106">Prerequisites</span></span>
<span data-ttu-id="25fce-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25fce-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25fce-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25fce-109">Permission type</span></span>|<span data-ttu-id="25fce-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25fce-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="25fce-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25fce-111">Delegated (work or school account)</span></span>|<span data-ttu-id="25fce-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25fce-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="25fce-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25fce-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="25fce-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25fce-114">Not supported.</span></span>|
|<span data-ttu-id="25fce-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25fce-115">Application</span></span>|<span data-ttu-id="25fce-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25fce-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="25fce-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25fce-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="25fce-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25fce-118">Request headers</span></span>
|<span data-ttu-id="25fce-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25fce-119">Header</span></span>|<span data-ttu-id="25fce-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25fce-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="25fce-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="25fce-121">Authorization</span></span>|<span data-ttu-id="25fce-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="25fce-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="25fce-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="25fce-123">Accept</span></span>|<span data-ttu-id="25fce-124">application/json</span><span class="sxs-lookup"><span data-stu-id="25fce-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="25fce-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25fce-125">Request body</span></span>
<span data-ttu-id="25fce-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="25fce-126">In the request body, supply a JSON representation for the managedEBookAssignment object.</span></span>

<span data-ttu-id="25fce-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="25fce-127">The following table shows the properties that are required when you create the managedEBookAssignment.</span></span>

|<span data-ttu-id="25fce-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25fce-128">Property</span></span>|<span data-ttu-id="25fce-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="25fce-129">Type</span></span>|<span data-ttu-id="25fce-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="25fce-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25fce-131">id</span><span class="sxs-lookup"><span data-stu-id="25fce-131">id</span></span>|<span data-ttu-id="25fce-132">String</span><span class="sxs-lookup"><span data-stu-id="25fce-132">String</span></span>|<span data-ttu-id="25fce-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="25fce-133">Key of the entity.</span></span>|
|<span data-ttu-id="25fce-134">target</span><span class="sxs-lookup"><span data-stu-id="25fce-134">target</span></span>|[<span data-ttu-id="25fce-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="25fce-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="25fce-136">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="25fce-136">The assignment target for eBook.</span></span>|
|<span data-ttu-id="25fce-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="25fce-137">installIntent</span></span>|[<span data-ttu-id="25fce-138">installIntent</span><span class="sxs-lookup"><span data-stu-id="25fce-138">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="25fce-139">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="25fce-139">The install intent for eBook.</span></span> <span data-ttu-id="25fce-140">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="25fce-140">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="25fce-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25fce-141">Response</span></span>
<span data-ttu-id="25fce-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25fce-142">If successful, this method returns a `201 Created` response code and a [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25fce-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25fce-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="25fce-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25fce-144">Request</span></span>
<span data-ttu-id="25fce-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25fce-145">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
Content-type: application/json
Content-length: 194

{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a><span data-ttu-id="25fce-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25fce-146">Response</span></span>
<span data-ttu-id="25fce-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25fce-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 243

{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "id": "ae8b0d27-0d27-ae8b-270d-8bae270d8bae",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```


