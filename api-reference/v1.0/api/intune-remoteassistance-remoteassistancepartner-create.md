---
title: Crear remoteAssistancePartner
description: Cree un objeto remoteAssistancePartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a9081af7c6bc79540eb0a1593f0645771346f539
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951568"
---
# <a name="create-remoteassistancepartner"></a><span data-ttu-id="43f3b-103">Crear remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="43f3b-103">Create remoteAssistancePartner</span></span>

> <span data-ttu-id="43f3b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="43f3b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="43f3b-105">Cree un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="43f3b-105">Create a new [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="43f3b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="43f3b-106">Prerequisites</span></span>
<span data-ttu-id="43f3b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43f3b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43f3b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43f3b-109">Permission type</span></span>|<span data-ttu-id="43f3b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43f3b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="43f3b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43f3b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="43f3b-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="43f3b-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="43f3b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43f3b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="43f3b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43f3b-114">Not supported.</span></span>|
|<span data-ttu-id="43f3b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43f3b-115">Application</span></span>|<span data-ttu-id="43f3b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43f3b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="43f3b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43f3b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/remoteAssistancePartners
```

## <a name="request-headers"></a><span data-ttu-id="43f3b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43f3b-118">Request headers</span></span>
|<span data-ttu-id="43f3b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43f3b-119">Header</span></span>|<span data-ttu-id="43f3b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43f3b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="43f3b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="43f3b-121">Authorization</span></span>|<span data-ttu-id="43f3b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="43f3b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="43f3b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="43f3b-123">Accept</span></span>|<span data-ttu-id="43f3b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="43f3b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="43f3b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43f3b-125">Request body</span></span>
<span data-ttu-id="43f3b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto remoteAssistancePartner.</span><span class="sxs-lookup"><span data-stu-id="43f3b-126">In the request body, supply a JSON representation for the remoteAssistancePartner object.</span></span>

<span data-ttu-id="43f3b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto remoteAssistancePartner.</span><span class="sxs-lookup"><span data-stu-id="43f3b-127">The following table shows the properties that are required when you create the remoteAssistancePartner.</span></span>

|<span data-ttu-id="43f3b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43f3b-128">Property</span></span>|<span data-ttu-id="43f3b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="43f3b-129">Type</span></span>|<span data-ttu-id="43f3b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="43f3b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="43f3b-131">id</span><span class="sxs-lookup"><span data-stu-id="43f3b-131">id</span></span>|<span data-ttu-id="43f3b-132">String</span><span class="sxs-lookup"><span data-stu-id="43f3b-132">String</span></span>|<span data-ttu-id="43f3b-133">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="43f3b-133">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="43f3b-134">displayName</span><span class="sxs-lookup"><span data-stu-id="43f3b-134">displayName</span></span>|<span data-ttu-id="43f3b-135">String</span><span class="sxs-lookup"><span data-stu-id="43f3b-135">String</span></span>|<span data-ttu-id="43f3b-136">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="43f3b-136">Display name of the partner.</span></span>|
|<span data-ttu-id="43f3b-137">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="43f3b-137">onboardingUrl</span></span>|<span data-ttu-id="43f3b-138">String</span><span class="sxs-lookup"><span data-stu-id="43f3b-138">String</span></span>|<span data-ttu-id="43f3b-139">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="43f3b-139">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="43f3b-140">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="43f3b-140">onboardingStatus</span></span>|[<span data-ttu-id="43f3b-141">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="43f3b-141">remoteAssistanceOnboardingStatus</span></span>](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|<span data-ttu-id="43f3b-142">TBD.</span><span class="sxs-lookup"><span data-stu-id="43f3b-142">TBD.</span></span> <span data-ttu-id="43f3b-143">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="43f3b-143">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="43f3b-144">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="43f3b-144">lastConnectionDateTime</span></span>|<span data-ttu-id="43f3b-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="43f3b-145">DateTimeOffset</span></span>|<span data-ttu-id="43f3b-146">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="43f3b-146">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="43f3b-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43f3b-147">Response</span></span>
<span data-ttu-id="43f3b-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43f3b-148">If successful, this method returns a `201 Created` response code and a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="43f3b-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43f3b-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="43f3b-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43f3b-150">Request</span></span>
<span data-ttu-id="43f3b-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43f3b-151">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners
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

### <a name="response"></a><span data-ttu-id="43f3b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43f3b-152">Response</span></span>
<span data-ttu-id="43f3b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43f3b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



