---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1e013038603a1d92595b50b5929be9954e1b280d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805939"
---
# <a name="assign-action"></a><span data-ttu-id="51dc0-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="51dc0-103">assign action</span></span>

> <span data-ttu-id="51dc0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51dc0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51dc0-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="51dc0-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51dc0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51dc0-106">Prerequisites</span></span>
<span data-ttu-id="51dc0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51dc0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51dc0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51dc0-109">Permission type</span></span>|<span data-ttu-id="51dc0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51dc0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51dc0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51dc0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="51dc0-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51dc0-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="51dc0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51dc0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51dc0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51dc0-114">Not supported.</span></span>|
|<span data-ttu-id="51dc0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51dc0-115">Application</span></span>|<span data-ttu-id="51dc0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51dc0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51dc0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51dc0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/assign
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}/assign
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="51dc0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51dc0-118">Request headers</span></span>
|<span data-ttu-id="51dc0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51dc0-119">Header</span></span>|<span data-ttu-id="51dc0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51dc0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51dc0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="51dc0-121">Authorization</span></span>|<span data-ttu-id="51dc0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51dc0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51dc0-123">Accept</span><span class="sxs-lookup"><span data-stu-id="51dc0-123">Accept</span></span>|<span data-ttu-id="51dc0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="51dc0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51dc0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51dc0-125">Request body</span></span>
<span data-ttu-id="51dc0-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="51dc0-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="51dc0-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="51dc0-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="51dc0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51dc0-128">Property</span></span>|<span data-ttu-id="51dc0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="51dc0-129">Type</span></span>|<span data-ttu-id="51dc0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="51dc0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="51dc0-131">asignaciones</span><span class="sxs-lookup"><span data-stu-id="51dc0-131">assignments</span></span>|<span data-ttu-id="51dc0-132">Colección [targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="51dc0-132">[targetedManagedAppPolicyAssignment](../resources/intune-mam-targetedmanagedapppolicyassignment.md) collection</span></span>|<span data-ttu-id="51dc0-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="51dc0-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="51dc0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51dc0-134">Response</span></span>
<span data-ttu-id="51dc0-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="51dc0-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="51dc0-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51dc0-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="51dc0-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51dc0-137">Request</span></span>
<span data-ttu-id="51dc0-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51dc0-138">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="51dc0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51dc0-139">Response</span></span>
<span data-ttu-id="51dc0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51dc0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



