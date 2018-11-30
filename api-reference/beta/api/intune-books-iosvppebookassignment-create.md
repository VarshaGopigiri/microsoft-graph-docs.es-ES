---
title: Crear iosVppEBookAssignment
description: Cree un objeto iosVppEBookAssignment.
ms.openlocfilehash: 192f5e006fa89f3dbf25a320967af68fbd06f7ef
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088411"
---
# <a name="create-iosvppebookassignment"></a><span data-ttu-id="c31c4-103">Crear iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="c31c4-103">Create iosVppEBookAssignment</span></span>

> <span data-ttu-id="c31c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c31c4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c31c4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c31c4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c31c4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c31c4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c31c4-107">Cree un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c31c4-107">Create a new [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c31c4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c31c4-108">Prerequisites</span></span>
<span data-ttu-id="c31c4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c31c4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c31c4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c31c4-111">Permission type</span></span>|<span data-ttu-id="c31c4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c31c4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c31c4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c31c4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c31c4-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c31c4-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c31c4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c31c4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c31c4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c31c4-116">Not supported.</span></span>|
|<span data-ttu-id="c31c4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c31c4-117">Application</span></span>|<span data-ttu-id="c31c4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c31c4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c31c4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c31c4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="c31c4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c31c4-120">Request headers</span></span>
|<span data-ttu-id="c31c4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c31c4-121">Header</span></span>|<span data-ttu-id="c31c4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c31c4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c31c4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c31c4-123">Authorization</span></span>|<span data-ttu-id="c31c4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c31c4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c31c4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c31c4-125">Accept</span></span>|<span data-ttu-id="c31c4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c31c4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c31c4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c31c4-127">Request body</span></span>
<span data-ttu-id="c31c4-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="c31c4-128">In the request body, supply a JSON representation for the iosVppEBookAssignment object.</span></span>

<span data-ttu-id="c31c4-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="c31c4-129">The following table shows the properties that are required when you create the iosVppEBookAssignment.</span></span>

|<span data-ttu-id="c31c4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c31c4-130">Property</span></span>|<span data-ttu-id="c31c4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c31c4-131">Type</span></span>|<span data-ttu-id="c31c4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c31c4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c31c4-133">id</span><span class="sxs-lookup"><span data-stu-id="c31c4-133">id</span></span>|<span data-ttu-id="c31c4-134">String</span><span class="sxs-lookup"><span data-stu-id="c31c4-134">String</span></span>|<span data-ttu-id="c31c4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c31c4-135">Key of the entity.</span></span> <span data-ttu-id="c31c4-136">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="c31c4-136">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="c31c4-137">target</span><span class="sxs-lookup"><span data-stu-id="c31c4-137">target</span></span>|[<span data-ttu-id="c31c4-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="c31c4-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="c31c4-139">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="c31c4-139">The assignment target for eBook.</span></span> <span data-ttu-id="c31c4-140">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="c31c4-140">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="c31c4-141">installIntent</span><span class="sxs-lookup"><span data-stu-id="c31c4-141">installIntent</span></span>|[<span data-ttu-id="c31c4-142">installIntent</span><span class="sxs-lookup"><span data-stu-id="c31c4-142">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="c31c4-143">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="c31c4-143">The install intent for eBook.</span></span> <span data-ttu-id="c31c4-144">Se hereda de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="c31c4-144">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span></span> <span data-ttu-id="c31c4-145">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="c31c4-145">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="c31c4-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c31c4-146">Response</span></span>
<span data-ttu-id="c31c4-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c31c4-147">If successful, this method returns a `201 Created` response code and a [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c31c4-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c31c4-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="c31c4-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c31c4-149">Request</span></span>
<span data-ttu-id="c31c4-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c31c4-150">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
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

### <a name="response"></a><span data-ttu-id="c31c4-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c31c4-151">Response</span></span>
<span data-ttu-id="c31c4-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c31c4-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





