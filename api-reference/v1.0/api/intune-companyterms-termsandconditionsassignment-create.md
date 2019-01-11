---
title: Crear termsAndConditionsAssignment
description: Cree un objeto termsAndConditionsAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 154bbee10ce552b4e7f8b69cb82adb8a1013cf38
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825315"
---
# <a name="create-termsandconditionsassignment"></a><span data-ttu-id="bf217-103">Crear termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="bf217-103">Create termsAndConditionsAssignment</span></span>

> <span data-ttu-id="bf217-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf217-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf217-105">Cree un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bf217-105">Create a new [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bf217-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf217-106">Prerequisites</span></span>
<span data-ttu-id="bf217-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bf217-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bf217-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf217-109">Permission type</span></span>|<span data-ttu-id="bf217-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf217-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bf217-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf217-111">Delegated (work or school account)</span></span>|<span data-ttu-id="bf217-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf217-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bf217-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf217-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bf217-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf217-114">Not supported.</span></span>|
|<span data-ttu-id="bf217-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf217-115">Application</span></span>|<span data-ttu-id="bf217-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf217-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bf217-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf217-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="bf217-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf217-118">Request headers</span></span>
|<span data-ttu-id="bf217-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf217-119">Header</span></span>|<span data-ttu-id="bf217-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bf217-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bf217-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="bf217-121">Authorization</span></span>|<span data-ttu-id="bf217-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bf217-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bf217-123">Accept</span><span class="sxs-lookup"><span data-stu-id="bf217-123">Accept</span></span>|<span data-ttu-id="bf217-124">application/json</span><span class="sxs-lookup"><span data-stu-id="bf217-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bf217-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf217-125">Request body</span></span>
<span data-ttu-id="bf217-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto termsAndConditionsAssignment.</span><span class="sxs-lookup"><span data-stu-id="bf217-126">In the request body, supply a JSON representation for the termsAndConditionsAssignment object.</span></span>

<span data-ttu-id="bf217-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto termsAndConditionsAssignment.</span><span class="sxs-lookup"><span data-stu-id="bf217-127">The following table shows the properties that are required when you create the termsAndConditionsAssignment.</span></span>

|<span data-ttu-id="bf217-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf217-128">Property</span></span>|<span data-ttu-id="bf217-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf217-129">Type</span></span>|<span data-ttu-id="bf217-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf217-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf217-131">id</span><span class="sxs-lookup"><span data-stu-id="bf217-131">id</span></span>|<span data-ttu-id="bf217-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="bf217-132">String</span></span>|<span data-ttu-id="bf217-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bf217-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="bf217-134">target</span><span class="sxs-lookup"><span data-stu-id="bf217-134">target</span></span>|[<span data-ttu-id="bf217-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="bf217-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="bf217-136">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="bf217-136">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="bf217-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf217-137">Response</span></span>
<span data-ttu-id="bf217-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf217-138">If successful, this method returns a `201 Created` response code and a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf217-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf217-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="bf217-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf217-140">Request</span></span>
<span data-ttu-id="bf217-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf217-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
Content-type: application/json
Content-length: 168

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="bf217-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf217-142">Response</span></span>
<span data-ttu-id="bf217-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf217-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



