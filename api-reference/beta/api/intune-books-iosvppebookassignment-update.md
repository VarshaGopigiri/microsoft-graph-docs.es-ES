---
title: Actualizar iosVppEBookAssignment
description: Actualice las propiedades de un objeto iosVppEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 272de2b88b930b8f55849e6a791dce6c77d1595c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958379"
---
# <a name="update-iosvppebookassignment"></a><span data-ttu-id="d1b7b-103">Actualizar iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="d1b7b-103">Update iosVppEBookAssignment</span></span>

> <span data-ttu-id="d1b7b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1b7b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d1b7b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d1b7b-107">Actualice las propiedades de un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d1b7b-107">Update the properties of a [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d1b7b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d1b7b-108">Prerequisites</span></span>
<span data-ttu-id="d1b7b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d1b7b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d1b7b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d1b7b-111">Permission type</span></span>|<span data-ttu-id="d1b7b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d1b7b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d1b7b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d1b7b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d1b7b-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1b7b-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d1b7b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d1b7b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d1b7b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-116">Not supported.</span></span>|
|<span data-ttu-id="d1b7b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d1b7b-117">Application</span></span>|<span data-ttu-id="d1b7b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d1b7b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d1b7b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="d1b7b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b7b-120">Request headers</span></span>
|<span data-ttu-id="d1b7b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1b7b-121">Header</span></span>|<span data-ttu-id="d1b7b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b7b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d1b7b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d1b7b-123">Authorization</span></span>|<span data-ttu-id="d1b7b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d1b7b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d1b7b-125">Accept</span></span>|<span data-ttu-id="d1b7b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d1b7b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d1b7b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b7b-127">Request body</span></span>
<span data-ttu-id="d1b7b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d1b7b-128">In the request body, supply a JSON representation for the [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>

<span data-ttu-id="d1b7b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d1b7b-129">The following table shows the properties that are required when you create the [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span></span>

|<span data-ttu-id="d1b7b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1b7b-130">Property</span></span>|<span data-ttu-id="d1b7b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1b7b-131">Type</span></span>|<span data-ttu-id="d1b7b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1b7b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d1b7b-133">id</span><span class="sxs-lookup"><span data-stu-id="d1b7b-133">id</span></span>|<span data-ttu-id="d1b7b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b7b-134">String</span></span>|<span data-ttu-id="d1b7b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-135">Key of the entity.</span></span> <span data-ttu-id="d1b7b-136">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d1b7b-136">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="d1b7b-137">target</span><span class="sxs-lookup"><span data-stu-id="d1b7b-137">target</span></span>|[<span data-ttu-id="d1b7b-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="d1b7b-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="d1b7b-139">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-139">The assignment target for eBook.</span></span> <span data-ttu-id="d1b7b-140">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d1b7b-140">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="d1b7b-141">installIntent</span><span class="sxs-lookup"><span data-stu-id="d1b7b-141">installIntent</span></span>|[<span data-ttu-id="d1b7b-142">installIntent</span><span class="sxs-lookup"><span data-stu-id="d1b7b-142">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="d1b7b-143">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-143">The install intent for eBook.</span></span> <span data-ttu-id="d1b7b-144">Se hereda de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d1b7b-144">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span></span> <span data-ttu-id="d1b7b-145">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-145">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="d1b7b-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1b7b-146">Response</span></span>
<span data-ttu-id="d1b7b-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-147">If successful, this method returns a `200 OK` response code and an updated [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d1b7b-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1b7b-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="d1b7b-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b7b-149">Request</span></span>
<span data-ttu-id="d1b7b-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-150">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/assignments/{managedEBookAssignmentId}
Content-type: application/json
Content-length: 133

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "required"
}
```

### <a name="response"></a><span data-ttu-id="d1b7b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1b7b-151">Response</span></span>
<span data-ttu-id="d1b7b-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d1b7b-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





