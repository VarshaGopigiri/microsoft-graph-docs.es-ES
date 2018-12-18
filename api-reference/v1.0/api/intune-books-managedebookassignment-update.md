---
title: Actualizar managedEBookAssignment
description: Actualice las propiedades de un objeto managedEBookAssignment.
author: tfitzmac
ms.openlocfilehash: 041d1b16754c7c3f8047a40073590d5647e91f3c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326505"
---
# <a name="update-managedebookassignment"></a><span data-ttu-id="73c0c-103">Actualizar managedEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="73c0c-103">Update managedEBookAssignment</span></span>

> <span data-ttu-id="73c0c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="73c0c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="73c0c-105">Actualice las propiedades de un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="73c0c-105">Update the properties of a [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="73c0c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="73c0c-106">Prerequisites</span></span>
<span data-ttu-id="73c0c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73c0c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73c0c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73c0c-109">Permission type</span></span>|<span data-ttu-id="73c0c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73c0c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="73c0c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73c0c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="73c0c-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="73c0c-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="73c0c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73c0c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="73c0c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73c0c-114">Not supported.</span></span>|
|<span data-ttu-id="73c0c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73c0c-115">Application</span></span>|<span data-ttu-id="73c0c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73c0c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="73c0c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73c0c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="73c0c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73c0c-118">Request headers</span></span>
|<span data-ttu-id="73c0c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73c0c-119">Header</span></span>|<span data-ttu-id="73c0c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="73c0c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="73c0c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="73c0c-121">Authorization</span></span>|<span data-ttu-id="73c0c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="73c0c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="73c0c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="73c0c-123">Accept</span></span>|<span data-ttu-id="73c0c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="73c0c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="73c0c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73c0c-125">Request body</span></span>
<span data-ttu-id="73c0c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="73c0c-126">In the request body, supply a JSON representation for the [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object.</span></span>

<span data-ttu-id="73c0c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="73c0c-127">The following table shows the properties that are required when you create the [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span></span>

|<span data-ttu-id="73c0c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73c0c-128">Property</span></span>|<span data-ttu-id="73c0c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="73c0c-129">Type</span></span>|<span data-ttu-id="73c0c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="73c0c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="73c0c-131">id</span><span class="sxs-lookup"><span data-stu-id="73c0c-131">id</span></span>|<span data-ttu-id="73c0c-132">String</span><span class="sxs-lookup"><span data-stu-id="73c0c-132">String</span></span>|<span data-ttu-id="73c0c-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="73c0c-133">Key of the entity.</span></span>|
|<span data-ttu-id="73c0c-134">target</span><span class="sxs-lookup"><span data-stu-id="73c0c-134">target</span></span>|[<span data-ttu-id="73c0c-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="73c0c-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="73c0c-136">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="73c0c-136">The assignment target for eBook.</span></span>|
|<span data-ttu-id="73c0c-137">installIntent</span><span class="sxs-lookup"><span data-stu-id="73c0c-137">installIntent</span></span>|[<span data-ttu-id="73c0c-138">installIntent</span><span class="sxs-lookup"><span data-stu-id="73c0c-138">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="73c0c-139">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="73c0c-139">The install intent for eBook.</span></span> <span data-ttu-id="73c0c-140">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="73c0c-140">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="73c0c-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73c0c-141">Response</span></span>
<span data-ttu-id="73c0c-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73c0c-142">If successful, this method returns a `200 OK` response code and an updated [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="73c0c-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73c0c-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="73c0c-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73c0c-144">Request</span></span>
<span data-ttu-id="73c0c-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73c0c-145">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
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

### <a name="response"></a><span data-ttu-id="73c0c-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73c0c-146">Response</span></span>
<span data-ttu-id="73c0c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="73c0c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



