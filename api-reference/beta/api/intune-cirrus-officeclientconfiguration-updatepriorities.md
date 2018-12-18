---
title: acción updatePriorities
description: Actualizar las prioridades de directiva.
author: tfitzmac
ms.openlocfilehash: d8c493200d5ed1c0e6eb2228a1e74337237e73e9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302593"
---
# <a name="updatepriorities-action"></a><span data-ttu-id="2806c-103">acción updatePriorities</span><span class="sxs-lookup"><span data-stu-id="2806c-103">updatePriorities action</span></span>

> <span data-ttu-id="2806c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2806c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2806c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2806c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2806c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2806c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2806c-107">Actualizar las prioridades de directiva.</span><span class="sxs-lookup"><span data-stu-id="2806c-107">Update policy priorities.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2806c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2806c-108">Prerequisites</span></span>
<span data-ttu-id="2806c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2806c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2806c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2806c-111">Permission type</span></span>|<span data-ttu-id="2806c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2806c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2806c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2806c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2806c-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2806c-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2806c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2806c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2806c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2806c-116">Not supported.</span></span>|
|<span data-ttu-id="2806c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2806c-117">Application</span></span>|<span data-ttu-id="2806c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2806c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2806c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2806c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /officeConfiguration/clientConfigurations/microsoft.management.services.api.updatePriorities
```

## <a name="request-headers"></a><span data-ttu-id="2806c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2806c-120">Request headers</span></span>
|<span data-ttu-id="2806c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2806c-121">Header</span></span>|<span data-ttu-id="2806c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2806c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2806c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2806c-123">Authorization</span></span>|<span data-ttu-id="2806c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2806c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2806c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2806c-125">Accept</span></span>|<span data-ttu-id="2806c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2806c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2806c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2806c-127">Request body</span></span>
<span data-ttu-id="2806c-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="2806c-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="2806c-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="2806c-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="2806c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2806c-130">Property</span></span>|<span data-ttu-id="2806c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2806c-131">Type</span></span>|<span data-ttu-id="2806c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2806c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2806c-133">officeConfigurationPolicyIds</span><span class="sxs-lookup"><span data-stu-id="2806c-133">officeConfigurationPolicyIds</span></span>|<span data-ttu-id="2806c-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="2806c-134">String collection</span></span>|<span data-ttu-id="2806c-135">Lista de identificadores de directiva de configuración de office</span><span class="sxs-lookup"><span data-stu-id="2806c-135">List of office configuration policy ids</span></span>|
|<span data-ttu-id="2806c-136">officeConfigurationPriorities</span><span class="sxs-lookup"><span data-stu-id="2806c-136">officeConfigurationPriorities</span></span>|<span data-ttu-id="2806c-137">Colección de Int32</span><span class="sxs-lookup"><span data-stu-id="2806c-137">Int32 collection</span></span>|<span data-ttu-id="2806c-138">Lista de las prioridades de configuración de office</span><span class="sxs-lookup"><span data-stu-id="2806c-138">List of office configuration priorities</span></span>|



## <a name="response"></a><span data-ttu-id="2806c-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2806c-139">Response</span></span>
<span data-ttu-id="2806c-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="2806c-140">If successful, this action returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="2806c-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2806c-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="2806c-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2806c-142">Request</span></span>
<span data-ttu-id="2806c-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2806c-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/microsoft.management.services.api.updatePriorities

Content-type: application/json
Content-length: 143

{
  "officeConfigurationPolicyIds": [
    "Office Configuration Policy Ids value"
  ],
  "officeConfigurationPriorities": [
    13
  ]
}
```

### <a name="response"></a><span data-ttu-id="2806c-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2806c-144">Response</span></span>
<span data-ttu-id="2806c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2806c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
```



