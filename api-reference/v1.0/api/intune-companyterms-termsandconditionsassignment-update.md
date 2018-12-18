---
title: Actualizar termsAndConditionsAssignment
description: Actualice las propiedades de un objeto termsAndConditionsAssignment.
author: tfitzmac
ms.openlocfilehash: b55ec01c6bac55f9b1d72a5aad5f931bed6b6b2a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301410"
---
# <a name="update-termsandconditionsassignment"></a><span data-ttu-id="3986c-103">Actualizar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="3986c-103">Update termsAndConditionsAssignment</span></span>

> <span data-ttu-id="3986c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3986c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3986c-105">Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3986c-105">Update the properties of a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3986c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3986c-106">Prerequisites</span></span>
<span data-ttu-id="3986c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3986c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3986c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3986c-109">Permission type</span></span>|<span data-ttu-id="3986c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3986c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3986c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3986c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3986c-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3986c-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="3986c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3986c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3986c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3986c-114">Not supported.</span></span>|
|<span data-ttu-id="3986c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3986c-115">Application</span></span>|<span data-ttu-id="3986c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3986c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3986c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3986c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="3986c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3986c-118">Request headers</span></span>
|<span data-ttu-id="3986c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3986c-119">Header</span></span>|<span data-ttu-id="3986c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3986c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3986c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3986c-121">Authorization</span></span>|<span data-ttu-id="3986c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3986c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3986c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3986c-123">Accept</span></span>|<span data-ttu-id="3986c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3986c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3986c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3986c-125">Request body</span></span>
<span data-ttu-id="3986c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3986c-126">In the request body, supply a JSON representation for the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>

<span data-ttu-id="3986c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3986c-127">The following table shows the properties that are required when you create the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span></span>

|<span data-ttu-id="3986c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3986c-128">Property</span></span>|<span data-ttu-id="3986c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3986c-129">Type</span></span>|<span data-ttu-id="3986c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3986c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3986c-131">id</span><span class="sxs-lookup"><span data-stu-id="3986c-131">id</span></span>|<span data-ttu-id="3986c-132">String</span><span class="sxs-lookup"><span data-stu-id="3986c-132">String</span></span>|<span data-ttu-id="3986c-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3986c-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="3986c-134">target</span><span class="sxs-lookup"><span data-stu-id="3986c-134">target</span></span>|[<span data-ttu-id="3986c-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="3986c-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="3986c-136">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="3986c-136">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="3986c-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3986c-137">Response</span></span>
<span data-ttu-id="3986c-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3986c-138">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3986c-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3986c-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="3986c-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3986c-140">Request</span></span>
<span data-ttu-id="3986c-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3986c-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
Content-type: application/json
Content-length: 168

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="3986c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3986c-142">Response</span></span>
<span data-ttu-id="3986c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3986c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 217

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



