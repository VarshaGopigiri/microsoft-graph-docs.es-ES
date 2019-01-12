---
title: Actualizar onPremisesConditionalAccessSettings
description: Actualice las propiedades de un objeto onPremisesConditionalAccessSettings.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 51b27d551f4cd34c8472781b750bebc87941a9ee
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943945"
---
# <a name="update-onpremisesconditionalaccesssettings"></a><span data-ttu-id="00e84-103">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="00e84-103">Update onPremisesConditionalAccessSettings</span></span>

> <span data-ttu-id="00e84-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00e84-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00e84-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00e84-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="00e84-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00e84-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00e84-107">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="00e84-107">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="00e84-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="00e84-108">Prerequisites</span></span>
<span data-ttu-id="00e84-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00e84-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="00e84-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00e84-111">Permission type</span></span>|<span data-ttu-id="00e84-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00e84-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="00e84-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00e84-113">Delegated (work or school account)</span></span>|<span data-ttu-id="00e84-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00e84-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="00e84-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00e84-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="00e84-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00e84-116">Not supported.</span></span>|
|<span data-ttu-id="00e84-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00e84-117">Application</span></span>|<span data-ttu-id="00e84-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00e84-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="00e84-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00e84-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/conditionalAccessSettings
PATCH /deviceManagement/exchangeOnPremisesPolicy/conditionalAccessSettings
```

## <a name="request-headers"></a><span data-ttu-id="00e84-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00e84-120">Request headers</span></span>
|<span data-ttu-id="00e84-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00e84-121">Header</span></span>|<span data-ttu-id="00e84-122">Valor</span><span class="sxs-lookup"><span data-stu-id="00e84-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="00e84-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="00e84-123">Authorization</span></span>|<span data-ttu-id="00e84-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="00e84-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="00e84-125">Accept</span><span class="sxs-lookup"><span data-stu-id="00e84-125">Accept</span></span>|<span data-ttu-id="00e84-126">application/json</span><span class="sxs-lookup"><span data-stu-id="00e84-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="00e84-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00e84-127">Request body</span></span>
<span data-ttu-id="00e84-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="00e84-128">In the request body, supply a JSON representation for the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>

<span data-ttu-id="00e84-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="00e84-129">The following table shows the properties that are required when you create the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span></span>

|<span data-ttu-id="00e84-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00e84-130">Property</span></span>|<span data-ttu-id="00e84-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="00e84-131">Type</span></span>|<span data-ttu-id="00e84-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="00e84-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00e84-133">id</span><span class="sxs-lookup"><span data-stu-id="00e84-133">id</span></span>|<span data-ttu-id="00e84-134">String</span><span class="sxs-lookup"><span data-stu-id="00e84-134">String</span></span>|<span data-ttu-id="00e84-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="00e84-135">Not yet documented</span></span>|
|<span data-ttu-id="00e84-136">enabled</span><span class="sxs-lookup"><span data-stu-id="00e84-136">enabled</span></span>|<span data-ttu-id="00e84-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="00e84-137">Boolean</span></span>|<span data-ttu-id="00e84-138">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="00e84-138">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="00e84-139">includedGroups</span><span class="sxs-lookup"><span data-stu-id="00e84-139">includedGroups</span></span>|<span data-ttu-id="00e84-140">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="00e84-140">Guid collection</span></span>|<span data-ttu-id="00e84-141">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="00e84-141">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="00e84-142">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="00e84-142">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="00e84-143">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="00e84-143">excludedGroups</span></span>|<span data-ttu-id="00e84-144">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="00e84-144">Guid collection</span></span>|<span data-ttu-id="00e84-145">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="00e84-145">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="00e84-146">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="00e84-146">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="00e84-147">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="00e84-147">overrideDefaultRule</span></span>|<span data-ttu-id="00e84-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="00e84-148">Boolean</span></span>|<span data-ttu-id="00e84-149">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="00e84-149">Override the default access rule when allowing a device to ensure access is granted.</span></span>|



## <a name="response"></a><span data-ttu-id="00e84-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00e84-150">Response</span></span>
<span data-ttu-id="00e84-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00e84-151">If successful, this method returns a `200 OK` response code and an updated [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="00e84-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00e84-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="00e84-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00e84-153">Request</span></span>
<span data-ttu-id="00e84-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00e84-154">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/conditionalAccessSettings
Content-type: application/json
Content-length: 201

{
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

### <a name="response"></a><span data-ttu-id="00e84-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00e84-155">Response</span></span>
<span data-ttu-id="00e84-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="00e84-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





