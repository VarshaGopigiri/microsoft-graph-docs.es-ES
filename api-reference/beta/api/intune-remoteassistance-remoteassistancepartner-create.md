---
title: Crear remoteAssistancePartner
description: Cree un objeto remoteAssistancePartner.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2b8d1de08fd8da0be55515fd69717d703fc96e42
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827478"
---
# <a name="create-remoteassistancepartner"></a><span data-ttu-id="34c30-103">Crear remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="34c30-103">Create remoteAssistancePartner</span></span>

> <span data-ttu-id="34c30-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34c30-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34c30-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34c30-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="34c30-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="34c30-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="34c30-107">Cree un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="34c30-107">Create a new [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="34c30-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="34c30-108">Prerequisites</span></span>
<span data-ttu-id="34c30-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="34c30-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="34c30-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34c30-111">Permission type</span></span>|<span data-ttu-id="34c30-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34c30-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="34c30-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34c30-113">Delegated (work or school account)</span></span>|<span data-ttu-id="34c30-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34c30-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="34c30-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34c30-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="34c30-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34c30-116">Not supported.</span></span>|
|<span data-ttu-id="34c30-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34c30-117">Application</span></span>|<span data-ttu-id="34c30-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34c30-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="34c30-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34c30-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/remoteAssistancePartners
```

## <a name="request-headers"></a><span data-ttu-id="34c30-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34c30-120">Request headers</span></span>
|<span data-ttu-id="34c30-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34c30-121">Header</span></span>|<span data-ttu-id="34c30-122">Valor</span><span class="sxs-lookup"><span data-stu-id="34c30-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="34c30-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="34c30-123">Authorization</span></span>|<span data-ttu-id="34c30-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="34c30-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="34c30-125">Accept</span><span class="sxs-lookup"><span data-stu-id="34c30-125">Accept</span></span>|<span data-ttu-id="34c30-126">application/json</span><span class="sxs-lookup"><span data-stu-id="34c30-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="34c30-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34c30-127">Request body</span></span>
<span data-ttu-id="34c30-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto remoteAssistancePartner.</span><span class="sxs-lookup"><span data-stu-id="34c30-128">In the request body, supply a JSON representation for the remoteAssistancePartner object.</span></span>

<span data-ttu-id="34c30-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto remoteAssistancePartner.</span><span class="sxs-lookup"><span data-stu-id="34c30-129">The following table shows the properties that are required when you create the remoteAssistancePartner.</span></span>

|<span data-ttu-id="34c30-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34c30-130">Property</span></span>|<span data-ttu-id="34c30-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c30-131">Type</span></span>|<span data-ttu-id="34c30-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c30-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="34c30-133">id</span><span class="sxs-lookup"><span data-stu-id="34c30-133">id</span></span>|<span data-ttu-id="34c30-134">String</span><span class="sxs-lookup"><span data-stu-id="34c30-134">String</span></span>|<span data-ttu-id="34c30-135">Identificador único del partner.</span><span class="sxs-lookup"><span data-stu-id="34c30-135">Unique identifier of the partner.</span></span>|
|<span data-ttu-id="34c30-136">displayName</span><span class="sxs-lookup"><span data-stu-id="34c30-136">displayName</span></span>|<span data-ttu-id="34c30-137">String</span><span class="sxs-lookup"><span data-stu-id="34c30-137">String</span></span>|<span data-ttu-id="34c30-138">Nombre para mostrar del partner.</span><span class="sxs-lookup"><span data-stu-id="34c30-138">Display name of the partner.</span></span>|
|<span data-ttu-id="34c30-139">onboardingUrl</span><span class="sxs-lookup"><span data-stu-id="34c30-139">onboardingUrl</span></span>|<span data-ttu-id="34c30-140">String</span><span class="sxs-lookup"><span data-stu-id="34c30-140">String</span></span>|<span data-ttu-id="34c30-141">Dirección URL del portal de integración del partner, donde un administrador puede configurar el servicio de Asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="34c30-141">URL of the partner's onboarding portal, where an administrator can configure their Remote Assistance service.</span></span>|
|<span data-ttu-id="34c30-142">onboardingStatus</span><span class="sxs-lookup"><span data-stu-id="34c30-142">onboardingStatus</span></span>|[<span data-ttu-id="34c30-143">remoteAssistanceOnboardingStatus</span><span class="sxs-lookup"><span data-stu-id="34c30-143">remoteAssistanceOnboardingStatus</span></span>](../resources/intune-remoteassistance-remoteassistanceonboardingstatus.md)|<span data-ttu-id="34c30-144">TBD.</span><span class="sxs-lookup"><span data-stu-id="34c30-144">TBD.</span></span> <span data-ttu-id="34c30-145">Los valores posibles son: `notOnboarded`, `onboarding` y `onboarded`.</span><span class="sxs-lookup"><span data-stu-id="34c30-145">Possible values are: `notOnboarded`, `onboarding`, `onboarded`.</span></span>|
|<span data-ttu-id="34c30-146">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="34c30-146">lastConnectionDateTime</span></span>|<span data-ttu-id="34c30-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="34c30-147">DateTimeOffset</span></span>|<span data-ttu-id="34c30-148">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="34c30-148">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="34c30-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34c30-149">Response</span></span>
<span data-ttu-id="34c30-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34c30-150">If successful, this method returns a `201 Created` response code and a [remoteAssistancePartner](../resources/intune-remoteassistance-remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="34c30-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34c30-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="34c30-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34c30-152">Request</span></span>
<span data-ttu-id="34c30-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34c30-153">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="34c30-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34c30-154">Response</span></span>
<span data-ttu-id="34c30-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34c30-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





