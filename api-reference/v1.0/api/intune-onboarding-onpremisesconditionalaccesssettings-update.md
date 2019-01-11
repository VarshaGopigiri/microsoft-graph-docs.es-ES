---
title: Actualizar onPremisesConditionalAccessSettings
description: Actualice las propiedades de un objeto onPremisesConditionalAccessSettings.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 761da1d549430c1f49f2d68b05194bffea661618
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889785"
---
# <a name="update-onpremisesconditionalaccesssettings"></a><span data-ttu-id="135b5-103">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="135b5-103">Update onPremisesConditionalAccessSettings</span></span>

> <span data-ttu-id="135b5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="135b5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="135b5-105">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="135b5-105">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="135b5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="135b5-106">Prerequisites</span></span>
<span data-ttu-id="135b5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="135b5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="135b5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="135b5-109">Permission type</span></span>|<span data-ttu-id="135b5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="135b5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="135b5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="135b5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="135b5-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="135b5-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="135b5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="135b5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="135b5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="135b5-114">Not supported.</span></span>|
|<span data-ttu-id="135b5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="135b5-115">Application</span></span>|<span data-ttu-id="135b5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="135b5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="135b5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="135b5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/conditionalAccessSettings
```

## <a name="request-headers"></a><span data-ttu-id="135b5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="135b5-118">Request headers</span></span>
|<span data-ttu-id="135b5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="135b5-119">Header</span></span>|<span data-ttu-id="135b5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="135b5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="135b5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="135b5-121">Authorization</span></span>|<span data-ttu-id="135b5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="135b5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="135b5-123">Accept</span><span class="sxs-lookup"><span data-stu-id="135b5-123">Accept</span></span>|<span data-ttu-id="135b5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="135b5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="135b5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="135b5-125">Request body</span></span>
<span data-ttu-id="135b5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="135b5-126">In the request body, supply a JSON representation for the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>

<span data-ttu-id="135b5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="135b5-127">The following table shows the properties that are required when you create the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span></span>

|<span data-ttu-id="135b5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="135b5-128">Property</span></span>|<span data-ttu-id="135b5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="135b5-129">Type</span></span>|<span data-ttu-id="135b5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="135b5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="135b5-131">id</span><span class="sxs-lookup"><span data-stu-id="135b5-131">id</span></span>|<span data-ttu-id="135b5-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="135b5-132">String</span></span>|<span data-ttu-id="135b5-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="135b5-133">Not yet documented</span></span>|
|<span data-ttu-id="135b5-134">enabled</span><span class="sxs-lookup"><span data-stu-id="135b5-134">enabled</span></span>|<span data-ttu-id="135b5-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="135b5-135">Boolean</span></span>|<span data-ttu-id="135b5-136">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="135b5-136">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="135b5-137">includedGroups</span><span class="sxs-lookup"><span data-stu-id="135b5-137">includedGroups</span></span>|<span data-ttu-id="135b5-138">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="135b5-138">Guid collection</span></span>|<span data-ttu-id="135b5-139">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="135b5-139">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="135b5-140">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="135b5-140">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="135b5-141">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="135b5-141">excludedGroups</span></span>|<span data-ttu-id="135b5-142">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="135b5-142">Guid collection</span></span>|<span data-ttu-id="135b5-143">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="135b5-143">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="135b5-144">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="135b5-144">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="135b5-145">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="135b5-145">overrideDefaultRule</span></span>|<span data-ttu-id="135b5-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="135b5-146">Boolean</span></span>|<span data-ttu-id="135b5-147">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="135b5-147">Override the default access rule when allowing a device to ensure access is granted.</span></span>|



## <a name="response"></a><span data-ttu-id="135b5-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="135b5-148">Response</span></span>
<span data-ttu-id="135b5-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="135b5-149">If successful, this method returns a `200 OK` response code and an updated [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="135b5-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="135b5-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="135b5-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="135b5-151">Request</span></span>
<span data-ttu-id="135b5-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="135b5-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/conditionalAccessSettings
Content-type: application/json
Content-length: 275

{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "enabled": true,
  "includedGroups": [
    "77c9d466-d466-77c9-66d4-c97766d4c977"
  ],
  "excludedGroups": [
    "2a0afae4-fae4-2a0a-e4fa-0a2ae4fa0a2a"
  ],
  "overrideDefaultRule": true
}
```

### <a name="response"></a><span data-ttu-id="135b5-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="135b5-153">Response</span></span>
<span data-ttu-id="135b5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="135b5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 324

{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "id": "a0efde21-de21-a0ef-21de-efa021deefa0",
  "enabled": true,
  "includedGroups": [
    "77c9d466-d466-77c9-66d4-c97766d4c977"
  ],
  "excludedGroups": [
    "2a0afae4-fae4-2a0a-e4fa-0a2ae4fa0a2a"
  ],
  "overrideDefaultRule": true
}
```



