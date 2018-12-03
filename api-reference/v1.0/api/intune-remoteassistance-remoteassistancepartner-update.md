---
title: Actualizar remoteAssistancePartner
description: Actualice las propiedades de un objeto remoteAssistancePartner.
ms.openlocfilehash: beb43a9d3035178dfb9b5cfa84476a4d1da68b22
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029123"
---
# <a name="update-remoteassistancepartner"></a><span data-ttu-id="4c8d0-103">Actualizar remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="4c8d0-103">Update remoteAssistancePartner</span></span>

> <span data-ttu-id="4c8d0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4c8d0-105">Actualice las propiedades de un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="4c8d0-105">Update the properties of a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4c8d0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4c8d0-106">Prerequisites</span></span>
<span data-ttu-id="4c8d0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c8d0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c8d0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c8d0-109">Permission type</span></span>|<span data-ttu-id="4c8d0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c8d0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4c8d0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c8d0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4c8d0-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4c8d0-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="4c8d0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c8d0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4c8d0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-114">Not supported.</span></span>|
|<span data-ttu-id="4c8d0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c8d0-115">Application</span></span>|<span data-ttu-id="4c8d0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4c8d0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c8d0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="4c8d0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8d0-118">Request headers</span></span>
|<span data-ttu-id="4c8d0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c8d0-119">Header</span></span>|<span data-ttu-id="4c8d0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4c8d0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4c8d0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4c8d0-121">Authorization</span></span>|<span data-ttu-id="4c8d0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4c8d0-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4c8d0-123">Accept</span></span>|<span data-ttu-id="4c8d0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4c8d0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c8d0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8d0-125">Request body</span></span>
<span data-ttu-id="4c8d0-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="4c8d0-126">In the request body, supply a JSON representation for the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>

<span data-ttu-id="4c8d0-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="4c8d0-127">The following table shows the properties that are required when you create the [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span></span>

|<span data-ttu-id="4c8d0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c8d0-128">Property</span></span>|<span data-ttu-id="4c8d0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c8d0-129">Type</span></span>|<span data-ttu-id="4c8d0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c8d0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4c8d0-131">id</span><span class="sxs-lookup"><span data-stu-id="4c8d0-131">id</span></span>|<span data-ttu-id="4c8d0-132">String</span><span class="sxs-lookup"><span data-stu-id="4c8d0-132">String</span></span>|<span data-ttu-id="4c8d0-133">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-133">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="4c8d0-134">displayName</span><span class="sxs-lookup"><span data-stu-id="4c8d0-134">displayName</span></span>|<span data-ttu-id="4c8d0-135">String</span><span class="sxs-lookup"><span data-stu-id="4c8d0-135">String</span></span>|<span data-ttu-id="4c8d0-136">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-136">Display name of the partner.</span></span>|
|<span data-ttu-id="4c8d0-137">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="4c8d0-137">onboardingUrl</span></span>|<span data-ttu-id="4c8d0-138">String</span><span class="sxs-lookup"><span data-stu-id="4c8d0-138">String</span></span>|<span data-ttu-id="4c8d0-139">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-139">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="4c8d0-140">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="4c8d0-140">onboardingStatus</span></span>|[<span data-ttu-id="4c8d0-141">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="4c8d0-141">remoteAssistanceOnboardingStatus</span></span>](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|<span data-ttu-id="4c8d0-142">TBD.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-142">TBD.</span></span> <span data-ttu-id="4c8d0-143">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-143">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="4c8d0-144">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="4c8d0-144">lastConnectionDateTime</span></span>|<span data-ttu-id="4c8d0-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4c8d0-145">DateTimeOffset</span></span>|<span data-ttu-id="4c8d0-146">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-146">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="4c8d0-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c8d0-147">Response</span></span>
<span data-ttu-id="4c8d0-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-148">If successful, this method returns a `200 OK` response code and an updated [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c8d0-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c8d0-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="4c8d0-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8d0-150">Request</span></span>
<span data-ttu-id="4c8d0-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-151">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
Content-type: application/json
Content-length: 266

{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "displayName": "Display Name value",
  "onboardingUrl": "https://example.com/onboardingUrl/",
  "onboardingStatus": "onboarding",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="4c8d0-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c8d0-152">Response</span></span>
<span data-ttu-id="4c8d0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4c8d0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 315

{
  "@odata.type": "#microsoft.graph.remoteAssistancePartner",
  "id": "7443c8b9-c8b9-7443-b9c8-4374b9c84374",
  "displayName": "Display Name value",
  "onboardingUrl": "https://example.com/onboardingUrl/",
  "onboardingStatus": "onboarding",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```


