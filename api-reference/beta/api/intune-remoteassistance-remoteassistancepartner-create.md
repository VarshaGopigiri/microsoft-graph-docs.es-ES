---
title: Crear remoteAssistancePartner
description: Cree un objeto remoteAssistancePartner.
ms.openlocfilehash: 1d6630622a3115cc7429547677c38e95bf96893a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085725"
---
# <a name="create-remoteassistancepartner"></a><span data-ttu-id="e2d01-103">Crear remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="e2d01-103">Create remoteAssistancePartner</span></span>

> <span data-ttu-id="e2d01-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2d01-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2d01-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2d01-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e2d01-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e2d01-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e2d01-107">Cree un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="e2d01-107">Create a new [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e2d01-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e2d01-108">Prerequisites</span></span>
<span data-ttu-id="e2d01-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e2d01-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e2d01-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2d01-111">Permission type</span></span>|<span data-ttu-id="e2d01-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2d01-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e2d01-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2d01-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e2d01-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e2d01-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e2d01-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2d01-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e2d01-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2d01-116">Not supported.</span></span>|
|<span data-ttu-id="e2d01-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2d01-117">Application</span></span>|<span data-ttu-id="e2d01-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2d01-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e2d01-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2d01-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/remoteAssistancePartners
```

## <a name="request-headers"></a><span data-ttu-id="e2d01-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2d01-120">Request headers</span></span>
|<span data-ttu-id="e2d01-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2d01-121">Header</span></span>|<span data-ttu-id="e2d01-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e2d01-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e2d01-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e2d01-123">Authorization</span></span>|<span data-ttu-id="e2d01-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e2d01-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e2d01-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e2d01-125">Accept</span></span>|<span data-ttu-id="e2d01-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e2d01-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e2d01-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2d01-127">Request body</span></span>
<span data-ttu-id="e2d01-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto remoteAssistancePartner.</span><span class="sxs-lookup"><span data-stu-id="e2d01-128">In the request body, supply a JSON representation for the remoteAssistancePartner object.</span></span>

<span data-ttu-id="e2d01-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto remoteAssistancePartner.</span><span class="sxs-lookup"><span data-stu-id="e2d01-129">The following table shows the properties that are required when you create the remoteAssistancePartner.</span></span>

|<span data-ttu-id="e2d01-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2d01-130">Property</span></span>|<span data-ttu-id="e2d01-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2d01-131">Type</span></span>|<span data-ttu-id="e2d01-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2d01-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e2d01-133">id</span><span class="sxs-lookup"><span data-stu-id="e2d01-133">id</span></span>|<span data-ttu-id="e2d01-134">String</span><span class="sxs-lookup"><span data-stu-id="e2d01-134">String</span></span>|<span data-ttu-id="e2d01-135">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="e2d01-135">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="e2d01-136">displayName</span><span class="sxs-lookup"><span data-stu-id="e2d01-136">displayName</span></span>|<span data-ttu-id="e2d01-137">String</span><span class="sxs-lookup"><span data-stu-id="e2d01-137">String</span></span>|<span data-ttu-id="e2d01-138">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="e2d01-138">Display name of the partner.</span></span>|
|<span data-ttu-id="e2d01-139">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="e2d01-139">onboardingUrl</span></span>|<span data-ttu-id="e2d01-140">String</span><span class="sxs-lookup"><span data-stu-id="e2d01-140">String</span></span>|<span data-ttu-id="e2d01-141">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="e2d01-141">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="e2d01-142">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="e2d01-142">onboardingStatus</span></span>|[<span data-ttu-id="e2d01-143">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="e2d01-143">remoteAssistanceOnboardingStatus</span></span>](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|<span data-ttu-id="e2d01-144">TBD.</span><span class="sxs-lookup"><span data-stu-id="e2d01-144">TBD.</span></span> <span data-ttu-id="e2d01-145">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="e2d01-145">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="e2d01-146">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="e2d01-146">lastConnectionDateTime</span></span>|<span data-ttu-id="e2d01-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e2d01-147">DateTimeOffset</span></span>|<span data-ttu-id="e2d01-148">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="e2d01-148">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="e2d01-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2d01-149">Response</span></span>
<span data-ttu-id="e2d01-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2d01-150">If successful, this method returns a `201 Created` response code and a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e2d01-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2d01-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="e2d01-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2d01-152">Request</span></span>
<span data-ttu-id="e2d01-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2d01-153">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/remoteAssistancePartners
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

### <a name="response"></a><span data-ttu-id="e2d01-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2d01-154">Response</span></span>
<span data-ttu-id="e2d01-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2d01-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




