---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 6812f3c1879c331cc27aeb25ea4516af080252b7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315305"
---
# <a name="assign-action"></a><span data-ttu-id="49334-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="49334-103">assign action</span></span>

> <span data-ttu-id="49334-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="49334-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="49334-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="49334-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="49334-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="49334-106">Prerequisites</span></span>
<span data-ttu-id="49334-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49334-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49334-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49334-109">Permission type</span></span>|<span data-ttu-id="49334-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49334-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="49334-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49334-111">Delegated (work or school account)</span></span>|<span data-ttu-id="49334-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49334-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="49334-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49334-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="49334-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49334-114">Not supported.</span></span>|
|<span data-ttu-id="49334-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49334-115">Application</span></span>|<span data-ttu-id="49334-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49334-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="49334-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49334-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="49334-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49334-118">Request headers</span></span>
|<span data-ttu-id="49334-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49334-119">Header</span></span>|<span data-ttu-id="49334-120">Valor</span><span class="sxs-lookup"><span data-stu-id="49334-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="49334-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="49334-121">Authorization</span></span>|<span data-ttu-id="49334-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="49334-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="49334-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="49334-123">Accept</span></span>|<span data-ttu-id="49334-124">application/json</span><span class="sxs-lookup"><span data-stu-id="49334-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="49334-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49334-125">Request body</span></span>
<span data-ttu-id="49334-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="49334-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="49334-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="49334-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="49334-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49334-128">Property</span></span>|<span data-ttu-id="49334-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="49334-129">Type</span></span>|<span data-ttu-id="49334-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="49334-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="49334-131">enrollmentConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="49334-131">enrollmentConfigurationAssignments</span></span>|<span data-ttu-id="49334-132">Colección [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="49334-132">[enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md) collection</span></span>|<span data-ttu-id="49334-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="49334-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="49334-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49334-134">Response</span></span>
<span data-ttu-id="49334-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="49334-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="49334-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49334-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="49334-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49334-137">Request</span></span>
<span data-ttu-id="49334-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49334-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assign

Content-type: application/json
Content-length: 304

{
  "enrollmentConfigurationAssignments": [
    {
      "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
      "id": "705b021c-021c-705b-1c02-5b701c025b70",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="49334-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49334-139">Response</span></span>
<span data-ttu-id="49334-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49334-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



