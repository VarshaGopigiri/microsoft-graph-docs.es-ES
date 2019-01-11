---
title: Crear managedEBookAssignment
description: Cree un objeto managedEBookAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8699cac63bec90693a06d8e73879a53cd3d6a4b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892242"
---
# <a name="create-managedebookassignment"></a><span data-ttu-id="a0666-103">Crear managedEBookAssignment</span><span class="sxs-lookup"><span data-stu-id="a0666-103">Create managedEBookAssignment</span></span>

> <span data-ttu-id="a0666-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0666-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0666-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0666-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a0666-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a0666-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a0666-107">Cree un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).</span><span class="sxs-lookup"><span data-stu-id="a0666-107">Create a new [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a0666-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a0666-108">Prerequisites</span></span>
<span data-ttu-id="a0666-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0666-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0666-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0666-111">Permission type</span></span>|<span data-ttu-id="a0666-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0666-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a0666-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0666-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a0666-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a0666-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a0666-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0666-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a0666-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0666-116">Not supported.</span></span>|
|<span data-ttu-id="a0666-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0666-117">Application</span></span>|<span data-ttu-id="a0666-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0666-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a0666-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0666-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="a0666-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0666-120">Request headers</span></span>
|<span data-ttu-id="a0666-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0666-121">Header</span></span>|<span data-ttu-id="a0666-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a0666-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a0666-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0666-123">Authorization</span></span>|<span data-ttu-id="a0666-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a0666-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a0666-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a0666-125">Accept</span></span>|<span data-ttu-id="a0666-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a0666-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0666-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0666-127">Request body</span></span>
<span data-ttu-id="a0666-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="a0666-128">In the request body, supply a JSON representation for the managedEBookAssignment object.</span></span>

<span data-ttu-id="a0666-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedEBookAssignment.</span><span class="sxs-lookup"><span data-stu-id="a0666-129">The following table shows the properties that are required when you create the managedEBookAssignment.</span></span>

|<span data-ttu-id="a0666-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0666-130">Property</span></span>|<span data-ttu-id="a0666-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0666-131">Type</span></span>|<span data-ttu-id="a0666-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0666-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a0666-133">id</span><span class="sxs-lookup"><span data-stu-id="a0666-133">id</span></span>|<span data-ttu-id="a0666-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a0666-134">String</span></span>|<span data-ttu-id="a0666-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a0666-135">Key of the entity.</span></span>|
|<span data-ttu-id="a0666-136">target</span><span class="sxs-lookup"><span data-stu-id="a0666-136">target</span></span>|[<span data-ttu-id="a0666-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="a0666-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="a0666-138">El destino de la asignación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a0666-138">The assignment target for eBook.</span></span>|
|<span data-ttu-id="a0666-139">installIntent</span><span class="sxs-lookup"><span data-stu-id="a0666-139">installIntent</span></span>|[<span data-ttu-id="a0666-140">installIntent</span><span class="sxs-lookup"><span data-stu-id="a0666-140">installIntent</span></span>](../resources/intune-shared-installintent.md)|<span data-ttu-id="a0666-141">El objetivo de instalación para el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="a0666-141">The install intent for eBook.</span></span> <span data-ttu-id="a0666-142">Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.</span><span class="sxs-lookup"><span data-stu-id="a0666-142">Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|



## <a name="response"></a><span data-ttu-id="a0666-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0666-143">Response</span></span>
<span data-ttu-id="a0666-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0666-144">If successful, this method returns a `201 Created` response code and a [managedEBookAssignment](../resources/intune-books-managedebookassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0666-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0666-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="a0666-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0666-146">Request</span></span>
<span data-ttu-id="a0666-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0666-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
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

### <a name="response"></a><span data-ttu-id="a0666-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0666-148">Response</span></span>
<span data-ttu-id="a0666-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0666-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





