---
title: Actualizar termsAndConditionsAssignment
description: Actualice las propiedades de un objeto termsAndConditionsAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 79b8595015496605711d2304d22381171ef3ef34
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851460"
---
# <a name="update-termsandconditionsassignment"></a><span data-ttu-id="bb7a6-103">Actualizar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="bb7a6-103">Update termsAndConditionsAssignment</span></span>

> <span data-ttu-id="bb7a6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb7a6-105">Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bb7a6-105">Update the properties of a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb7a6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bb7a6-106">Prerequisites</span></span>
<span data-ttu-id="bb7a6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb7a6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb7a6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb7a6-109">Permission type</span></span>|<span data-ttu-id="bb7a6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb7a6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb7a6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb7a6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="bb7a6-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb7a6-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bb7a6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb7a6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb7a6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-114">Not supported.</span></span>|
|<span data-ttu-id="bb7a6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb7a6-115">Application</span></span>|<span data-ttu-id="bb7a6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb7a6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb7a6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="bb7a6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb7a6-118">Request headers</span></span>
|<span data-ttu-id="bb7a6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb7a6-119">Header</span></span>|<span data-ttu-id="bb7a6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bb7a6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb7a6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="bb7a6-121">Authorization</span></span>|<span data-ttu-id="bb7a6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb7a6-123">Accept</span><span class="sxs-lookup"><span data-stu-id="bb7a6-123">Accept</span></span>|<span data-ttu-id="bb7a6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="bb7a6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb7a6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb7a6-125">Request body</span></span>
<span data-ttu-id="bb7a6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bb7a6-126">In the request body, supply a JSON representation for the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>

<span data-ttu-id="bb7a6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bb7a6-127">The following table shows the properties that are required when you create the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span></span>

|<span data-ttu-id="bb7a6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb7a6-128">Property</span></span>|<span data-ttu-id="bb7a6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb7a6-129">Type</span></span>|<span data-ttu-id="bb7a6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb7a6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bb7a6-131">id</span><span class="sxs-lookup"><span data-stu-id="bb7a6-131">id</span></span>|<span data-ttu-id="bb7a6-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb7a6-132">String</span></span>|<span data-ttu-id="bb7a6-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="bb7a6-134">target</span><span class="sxs-lookup"><span data-stu-id="bb7a6-134">target</span></span>|[<span data-ttu-id="bb7a6-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="bb7a6-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="bb7a6-136">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-136">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="bb7a6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb7a6-137">Response</span></span>
<span data-ttu-id="bb7a6-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-138">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb7a6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb7a6-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb7a6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb7a6-140">Request</span></span>
<span data-ttu-id="bb7a6-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-141">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="bb7a6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb7a6-142">Response</span></span>
<span data-ttu-id="bb7a6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



