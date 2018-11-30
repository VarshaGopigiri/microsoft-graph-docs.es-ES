---
title: Actualizar termsAndConditionsGroupAssignment
description: Actualizar las propiedades de un objeto termsAndConditionsGroupAssignment.
ms.openlocfilehash: 0b38a5da65f76262d890ace17dc4d174567f62c1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085244"
---
# <a name="update-termsandconditionsgroupassignment"></a><span data-ttu-id="96dda-103">Actualizar termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="96dda-103">Update termsAndConditionsGroupAssignment</span></span>

> <span data-ttu-id="96dda-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96dda-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96dda-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96dda-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="96dda-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="96dda-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="96dda-107">Actualizar las propiedades de un objeto [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="96dda-107">Update the properties of a [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="96dda-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="96dda-108">Prerequisites</span></span>
<span data-ttu-id="96dda-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="96dda-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="96dda-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="96dda-111">Permission type</span></span>|<span data-ttu-id="96dda-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="96dda-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="96dda-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="96dda-113">Delegated (work or school account)</span></span>|<span data-ttu-id="96dda-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="96dda-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="96dda-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="96dda-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="96dda-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96dda-116">Not supported.</span></span>|
|<span data-ttu-id="96dda-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="96dda-117">Application</span></span>|<span data-ttu-id="96dda-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="96dda-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="96dda-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="96dda-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments/{termsAndConditionsGroupAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="96dda-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="96dda-120">Request headers</span></span>
|<span data-ttu-id="96dda-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96dda-121">Header</span></span>|<span data-ttu-id="96dda-122">Valor</span><span class="sxs-lookup"><span data-stu-id="96dda-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="96dda-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="96dda-123">Authorization</span></span>|<span data-ttu-id="96dda-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="96dda-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="96dda-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="96dda-125">Accept</span></span>|<span data-ttu-id="96dda-126">application/json</span><span class="sxs-lookup"><span data-stu-id="96dda-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="96dda-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="96dda-127">Request body</span></span>
<span data-ttu-id="96dda-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="96dda-128">In the request body, supply a JSON representation for the [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) object.</span></span>

<span data-ttu-id="96dda-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md).</span><span class="sxs-lookup"><span data-stu-id="96dda-129">The following table shows the properties that are required when you create the [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md).</span></span>

|<span data-ttu-id="96dda-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96dda-130">Property</span></span>|<span data-ttu-id="96dda-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="96dda-131">Type</span></span>|<span data-ttu-id="96dda-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="96dda-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="96dda-133">id</span><span class="sxs-lookup"><span data-stu-id="96dda-133">id</span></span>|<span data-ttu-id="96dda-134">String</span><span class="sxs-lookup"><span data-stu-id="96dda-134">String</span></span>|<span data-ttu-id="96dda-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="96dda-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="96dda-136">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="96dda-136">targetGroupId</span></span>|<span data-ttu-id="96dda-137">String</span><span class="sxs-lookup"><span data-stu-id="96dda-137">String</span></span>|<span data-ttu-id="96dda-138">Identificador único de un grupo que se asigna la directiva T & C a.</span><span class="sxs-lookup"><span data-stu-id="96dda-138">Unique identifier of a group that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="96dda-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96dda-139">Response</span></span>
<span data-ttu-id="96dda-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="96dda-140">If successful, this method returns a `200 OK` response code and an updated [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="96dda-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="96dda-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="96dda-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="96dda-142">Request</span></span>
<span data-ttu-id="96dda-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="96dda-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/groupAssignments/{termsAndConditionsGroupAssignmentId}
Content-type: application/json
Content-length: 48

{
  "targetGroupId": "Target Group Id value"
}
```

### <a name="response"></a><span data-ttu-id="96dda-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="96dda-144">Response</span></span>
<span data-ttu-id="96dda-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="96dda-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 169

{
  "@odata.type": "#microsoft.graph.termsAndConditionsGroupAssignment",
  "id": "2eb1aab7-aab7-2eb1-b7aa-b12eb7aab12e",
  "targetGroupId": "Target Group Id value"
}
```




