---
title: Crear termsAndConditionsAssignment
description: Cree un objeto termsAndConditionsAssignment.
author: tfitzmac
ms.openlocfilehash: 0a6cc4024487610fe4d243a2957d99a0522d800b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333337"
---
# <a name="create-termsandconditionsassignment"></a><span data-ttu-id="3b497-103">Crear termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="3b497-103">Create termsAndConditionsAssignment</span></span>

> <span data-ttu-id="3b497-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3b497-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3b497-105">Cree un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3b497-105">Create a new [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3b497-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3b497-106">Prerequisites</span></span>
<span data-ttu-id="3b497-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b497-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3b497-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b497-109">Permission type</span></span>|<span data-ttu-id="3b497-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b497-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3b497-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b497-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3b497-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b497-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="3b497-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b497-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3b497-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b497-114">Not supported.</span></span>|
|<span data-ttu-id="3b497-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b497-115">Application</span></span>|<span data-ttu-id="3b497-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b497-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3b497-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b497-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="3b497-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b497-118">Request headers</span></span>
|<span data-ttu-id="3b497-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b497-119">Header</span></span>|<span data-ttu-id="3b497-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3b497-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3b497-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3b497-121">Authorization</span></span>|<span data-ttu-id="3b497-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3b497-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3b497-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3b497-123">Accept</span></span>|<span data-ttu-id="3b497-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3b497-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3b497-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b497-125">Request body</span></span>
<span data-ttu-id="3b497-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto termsAndConditionsAssignment.</span><span class="sxs-lookup"><span data-stu-id="3b497-126">In the request body, supply a JSON representation for the termsAndConditionsAssignment object.</span></span>

<span data-ttu-id="3b497-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto termsAndConditionsAssignment.</span><span class="sxs-lookup"><span data-stu-id="3b497-127">The following table shows the properties that are required when you create the termsAndConditionsAssignment.</span></span>

|<span data-ttu-id="3b497-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b497-128">Property</span></span>|<span data-ttu-id="3b497-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b497-129">Type</span></span>|<span data-ttu-id="3b497-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b497-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3b497-131">id</span><span class="sxs-lookup"><span data-stu-id="3b497-131">id</span></span>|<span data-ttu-id="3b497-132">String</span><span class="sxs-lookup"><span data-stu-id="3b497-132">String</span></span>|<span data-ttu-id="3b497-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3b497-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="3b497-134">target</span><span class="sxs-lookup"><span data-stu-id="3b497-134">target</span></span>|[<span data-ttu-id="3b497-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="3b497-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="3b497-136">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="3b497-136">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="3b497-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b497-137">Response</span></span>
<span data-ttu-id="3b497-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b497-138">If successful, this method returns a `201 Created` response code and a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b497-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b497-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="3b497-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b497-140">Request</span></span>
<span data-ttu-id="3b497-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b497-141">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="3b497-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b497-142">Response</span></span>
<span data-ttu-id="3b497-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3b497-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



