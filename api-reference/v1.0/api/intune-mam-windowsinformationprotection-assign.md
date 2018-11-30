---
title: asignar acción
description: Todavía no documentado
ms.openlocfilehash: 928067d1058df303c6963d54d4322c2b41ddddb1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032546"
---
# <a name="assign-action"></a><span data-ttu-id="67cc5-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="67cc5-103">assign action</span></span>

> <span data-ttu-id="67cc5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="67cc5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="67cc5-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="67cc5-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="67cc5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67cc5-106">Prerequisites</span></span>
<span data-ttu-id="67cc5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="67cc5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="67cc5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="67cc5-109">Permission type</span></span>|<span data-ttu-id="67cc5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="67cc5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="67cc5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="67cc5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="67cc5-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="67cc5-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="67cc5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="67cc5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="67cc5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67cc5-114">Not supported.</span></span>|
|<span data-ttu-id="67cc5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="67cc5-115">Application</span></span>|<span data-ttu-id="67cc5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67cc5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="67cc5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67cc5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/assign
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}/assign
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="67cc5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67cc5-118">Request headers</span></span>
|<span data-ttu-id="67cc5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67cc5-119">Header</span></span>|<span data-ttu-id="67cc5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="67cc5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="67cc5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="67cc5-121">Authorization</span></span>|<span data-ttu-id="67cc5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="67cc5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="67cc5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="67cc5-123">Accept</span></span>|<span data-ttu-id="67cc5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="67cc5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="67cc5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67cc5-125">Request body</span></span>
<span data-ttu-id="67cc5-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="67cc5-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="67cc5-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="67cc5-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="67cc5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67cc5-128">Property</span></span>|<span data-ttu-id="67cc5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="67cc5-129">Type</span></span>|<span data-ttu-id="67cc5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="67cc5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="67cc5-131">asignaciones</span><span class="sxs-lookup"><span data-stu-id="67cc5-131">assignments</span></span>|<span data-ttu-id="67cc5-132">Colección [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="67cc5-132">[targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="67cc5-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="67cc5-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="67cc5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67cc5-134">Response</span></span>
<span data-ttu-id="67cc5-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="67cc5-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="67cc5-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67cc5-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="67cc5-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67cc5-137">Request</span></span>
<span data-ttu-id="67cc5-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67cc5-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/assign

Content-type: application/json
Content-length: 282

{
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.targetedManagedAppPolicyAssignment",
      "id": "8b68c4a6-c4a6-8b68-a6c4-688ba6c4688b",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="67cc5-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67cc5-139">Response</span></span>
<span data-ttu-id="67cc5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67cc5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



