---
title: Crear iosVppEBookAssignment
description: Cree un objeto iosVppEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b5ff460b702c943268d9992bd17e99fd54369548
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963972"
---
# <a name="create-iosvppebookassignment"></a><span data-ttu-id="ffdab-103">Crear iosVppEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="ffdab-103">Create iosVppEBookAssignment</span></span>

> <span data-ttu-id="ffdab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffdab-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffdab-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffdab-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ffdab-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffdab-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffdab-107">Cree un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ffdab-107">Create a new [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ffdab-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ffdab-108">Prerequisites</span></span>
<span data-ttu-id="ffdab-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ffdab-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ffdab-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ffdab-111">Permission type</span></span>|<span data-ttu-id="ffdab-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ffdab-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ffdab-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ffdab-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ffdab-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffdab-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ffdab-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ffdab-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ffdab-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffdab-116">Not supported.</span></span>|
|<span data-ttu-id="ffdab-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ffdab-117">Application</span></span>|<span data-ttu-id="ffdab-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ffdab-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ffdab-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ffdab-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="ffdab-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ffdab-120">Request headers</span></span>
|<span data-ttu-id="ffdab-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffdab-121">Header</span></span>|<span data-ttu-id="ffdab-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ffdab-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ffdab-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ffdab-123">Authorization</span></span>|<span data-ttu-id="ffdab-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ffdab-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ffdab-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ffdab-125">Accept</span></span>|<span data-ttu-id="ffdab-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ffdab-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ffdab-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ffdab-127">Request body</span></span>
<span data-ttu-id="ffdab-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="ffdab-128">In the request body, supply a JSON representation for the iosVppEBookAssignment object.</span></span>

<span data-ttu-id="ffdab-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="ffdab-129">The following table shows the properties that are required when you create the iosVppEBookAssignment.</span></span>

|<span data-ttu-id="ffdab-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffdab-130">Property</span></span>|<span data-ttu-id="ffdab-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffdab-131">Type</span></span>|<span data-ttu-id="ffdab-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffdab-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ffdab-133">id</span><span class="sxs-lookup"><span data-stu-id="ffdab-133">id</span></span>|<span data-ttu-id="ffdab-134">String</span><span class="sxs-lookup"><span data-stu-id="ffdab-134">String</span></span>|<span data-ttu-id="ffdab-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ffdab-135">Key of the entity.</span></span> <span data-ttu-id="ffdab-136">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ffdab-136">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="ffdab-137">target</span><span class="sxs-lookup"><span data-stu-id="ffdab-137">target</span></span>|[<span data-ttu-id="ffdab-138">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="ffdab-138">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="ffdab-139">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="ffdab-139">The assignment target for eBook.</span></span> <span data-ttu-id="ffdab-140">Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ffdab-140">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span></span>|
|<span data-ttu-id="ffdab-141">installIntent</span><span class="sxs-lookup"><span data-stu-id="ffdab-141">installIntent</span></span>|[<span data-ttu-id="ffdab-142">installIntent</span><span class="sxs-lookup"><span data-stu-id="ffdab-142">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="ffdab-143">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="ffdab-143">The install intent for eBook.</span></span> <span data-ttu-id="ffdab-144">Se hereda de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ffdab-144">Inherited from [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span></span> <span data-ttu-id="ffdab-145">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="ffdab-145">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="ffdab-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffdab-146">Response</span></span>
<span data-ttu-id="ffdab-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ffdab-147">If successful, this method returns a `201 Created` response code and a [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ffdab-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ffdab-148">Example</span></span>
### <a name="request"></a><span data-ttu-id="ffdab-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ffdab-149">Request</span></span>
<span data-ttu-id="ffdab-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ffdab-150">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ffdab-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ffdab-151">Response</span></span>
<span data-ttu-id="ffdab-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ffdab-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





