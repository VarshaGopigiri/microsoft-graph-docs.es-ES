---
title: Actualizar iosVppEBookAssignment
description: Actualice las propiedades de un objeto iosVppEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8b1d4bec696b247e1e234e4329b60af4315e3cc4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876492"
---
# <a name="update-iosvppebookassignment"></a><span data-ttu-id="b3bf6-103">Actualizar iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="b3bf6-103">Update iosVppEBookAssignment</span></span>

> <span data-ttu-id="b3bf6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3bf6-105">Actualice las propiedades de un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b3bf6-105">Update the properties of a [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3bf6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b3bf6-106">Prerequisites</span></span>
<span data-ttu-id="b3bf6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3bf6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3bf6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3bf6-109">Permission type</span></span>|<span data-ttu-id="b3bf6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3bf6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3bf6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3bf6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b3bf6-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b3bf6-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b3bf6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3bf6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3bf6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-114">Not supported.</span></span>|
|<span data-ttu-id="b3bf6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3bf6-115">Application</span></span>|<span data-ttu-id="b3bf6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3bf6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3bf6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="b3bf6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3bf6-118">Request headers</span></span>
|<span data-ttu-id="b3bf6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3bf6-119">Header</span></span>|<span data-ttu-id="b3bf6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b3bf6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3bf6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b3bf6-121">Authorization</span></span>|<span data-ttu-id="b3bf6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b3bf6-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b3bf6-123">Accept</span></span>|<span data-ttu-id="b3bf6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b3bf6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3bf6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3bf6-125">Request body</span></span>
<span data-ttu-id="b3bf6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b3bf6-126">In the request body, supply a JSON representation for the [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>

<span data-ttu-id="b3bf6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b3bf6-127">The following table shows the properties that are required when you create the [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span></span>

|<span data-ttu-id="b3bf6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3bf6-128">Property</span></span>|<span data-ttu-id="b3bf6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3bf6-129">Type</span></span>|<span data-ttu-id="b3bf6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3bf6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3bf6-131">id</span><span class="sxs-lookup"><span data-stu-id="b3bf6-131">id</span></span>|<span data-ttu-id="b3bf6-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3bf6-132">String</span></span>|<span data-ttu-id="b3bf6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-133">Key of the entity.</span></span> <span data-ttu-id="b3bf6-134">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="b3bf6-134">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="b3bf6-135">target</span><span class="sxs-lookup"><span data-stu-id="b3bf6-135">target</span></span>|[<span data-ttu-id="b3bf6-136">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="b3bf6-136">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="b3bf6-137">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-137">The assignment target for eBook.</span></span> <span data-ttu-id="b3bf6-138">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="b3bf6-138">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="b3bf6-139">installIntent</span><span class="sxs-lookup"><span data-stu-id="b3bf6-139">installIntent</span></span>|[<span data-ttu-id="b3bf6-140">installIntent</span><span class="sxs-lookup"><span data-stu-id="b3bf6-140">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="b3bf6-141">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-141">The install intent for eBook.</span></span> <span data-ttu-id="b3bf6-142">Se hereda de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="b3bf6-142">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span></span> <span data-ttu-id="b3bf6-143">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-143">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="b3bf6-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3bf6-144">Response</span></span>
<span data-ttu-id="b3bf6-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-145">If successful, this method returns a `200 OK` response code and an updated [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3bf6-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3bf6-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3bf6-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3bf6-147">Request</span></span>
<span data-ttu-id="b3bf6-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-148">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
Content-type: application/json
Content-length: 193

{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a><span data-ttu-id="b3bf6-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3bf6-149">Response</span></span>
<span data-ttu-id="b3bf6-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b3bf6-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 242

{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "id": "48f05789-5789-48f0-8957-f0488957f048",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```



