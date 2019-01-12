---
title: Crear termsAndConditionsAssignment
description: Cree un objeto termsAndConditionsAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 704aa0a3f86c3b65b3f2882af21010c46c02f1b9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976138"
---
# <a name="create-termsandconditionsassignment"></a><span data-ttu-id="d292d-103">Crear termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="d292d-103">Create termsAndConditionsAssignment</span></span>

> <span data-ttu-id="d292d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d292d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d292d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d292d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d292d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d292d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d292d-107">Cree un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d292d-107">Create a new [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d292d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d292d-108">Prerequisites</span></span>
<span data-ttu-id="d292d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d292d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d292d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d292d-111">Permission type</span></span>|<span data-ttu-id="d292d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d292d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d292d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d292d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d292d-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d292d-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d292d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d292d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d292d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d292d-116">Not supported.</span></span>|
|<span data-ttu-id="d292d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d292d-117">Application</span></span>|<span data-ttu-id="d292d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d292d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d292d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d292d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="d292d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d292d-120">Request headers</span></span>
|<span data-ttu-id="d292d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d292d-121">Header</span></span>|<span data-ttu-id="d292d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d292d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d292d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d292d-123">Authorization</span></span>|<span data-ttu-id="d292d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d292d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d292d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d292d-125">Accept</span></span>|<span data-ttu-id="d292d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d292d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d292d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d292d-127">Request body</span></span>
<span data-ttu-id="d292d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto termsAndConditionsAssignment.</span><span class="sxs-lookup"><span data-stu-id="d292d-128">In the request body, supply a JSON representation for the termsAndConditionsAssignment object.</span></span>

<span data-ttu-id="d292d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto termsAndConditionsAssignment.</span><span class="sxs-lookup"><span data-stu-id="d292d-129">The following table shows the properties that are required when you create the termsAndConditionsAssignment.</span></span>

|<span data-ttu-id="d292d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d292d-130">Property</span></span>|<span data-ttu-id="d292d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d292d-131">Type</span></span>|<span data-ttu-id="d292d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d292d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d292d-133">id</span><span class="sxs-lookup"><span data-stu-id="d292d-133">id</span></span>|<span data-ttu-id="d292d-134">String</span><span class="sxs-lookup"><span data-stu-id="d292d-134">String</span></span>|<span data-ttu-id="d292d-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d292d-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="d292d-136">target</span><span class="sxs-lookup"><span data-stu-id="d292d-136">target</span></span>|[<span data-ttu-id="d292d-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="d292d-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="d292d-138">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="d292d-138">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="d292d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d292d-139">Response</span></span>
<span data-ttu-id="d292d-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d292d-140">If successful, this method returns a `201 Created` response code and a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d292d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d292d-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="d292d-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d292d-142">Request</span></span>
<span data-ttu-id="d292d-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d292d-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
Content-type: application/json
Content-length: 168

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="d292d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d292d-144">Response</span></span>
<span data-ttu-id="d292d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d292d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





