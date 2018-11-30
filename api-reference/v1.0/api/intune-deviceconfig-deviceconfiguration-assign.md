---
title: asignar acción
description: Todavía no documentado
ms.openlocfilehash: 615f8b760b908de1eb69aae2cdfbdf2eafdd64e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031435"
---
# <a name="assign-action"></a><span data-ttu-id="27924-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="27924-103">assign action</span></span>

> <span data-ttu-id="27924-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="27924-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="27924-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="27924-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="27924-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="27924-106">Prerequisites</span></span>
<span data-ttu-id="27924-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27924-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27924-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27924-109">Permission type</span></span>|<span data-ttu-id="27924-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27924-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="27924-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27924-111">Delegated (work or school account)</span></span>|<span data-ttu-id="27924-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27924-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="27924-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27924-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="27924-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27924-114">Not supported.</span></span>|
|<span data-ttu-id="27924-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27924-115">Application</span></span>|<span data-ttu-id="27924-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27924-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="27924-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27924-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="27924-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27924-118">Request headers</span></span>
|<span data-ttu-id="27924-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27924-119">Header</span></span>|<span data-ttu-id="27924-120">Valor</span><span class="sxs-lookup"><span data-stu-id="27924-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="27924-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="27924-121">Authorization</span></span>|<span data-ttu-id="27924-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="27924-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="27924-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="27924-123">Accept</span></span>|<span data-ttu-id="27924-124">application/json</span><span class="sxs-lookup"><span data-stu-id="27924-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="27924-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27924-125">Request body</span></span>
<span data-ttu-id="27924-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="27924-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="27924-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="27924-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="27924-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27924-128">Property</span></span>|<span data-ttu-id="27924-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="27924-129">Type</span></span>|<span data-ttu-id="27924-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="27924-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="27924-131">asignaciones</span><span class="sxs-lookup"><span data-stu-id="27924-131">assignments</span></span>|<span data-ttu-id="27924-132">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="27924-132">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="27924-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="27924-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="27924-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27924-134">Response</span></span>
<span data-ttu-id="27924-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27924-135">If successful, this action returns a `200 OK` response code and a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="27924-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27924-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="27924-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27924-137">Request</span></span>
<span data-ttu-id="27924-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27924-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assign

Content-type: application/json
Content-length: 277

{
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
      "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="27924-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27924-139">Response</span></span>
<span data-ttu-id="27924-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27924-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 271

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
      "id": "d59b6342-6342-d59b-4263-9bd542639bd5",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```


