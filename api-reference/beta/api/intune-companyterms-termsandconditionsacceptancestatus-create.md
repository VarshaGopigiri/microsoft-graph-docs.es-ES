---
title: Crear termsAndConditionsAcceptanceStatus
description: Cree un objeto termsAndConditionsAcceptanceStatus.
ms.openlocfilehash: 0c23689addf5c1c7a53f2d9f5a7c5f09918fd9f7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086487"
---
# <a name="create-termsandconditionsacceptancestatus"></a><span data-ttu-id="51de8-103">Crear termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="51de8-103">Create termsAndConditionsAcceptanceStatus</span></span>

> <span data-ttu-id="51de8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="51de8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="51de8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="51de8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="51de8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51de8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51de8-107">Cree un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="51de8-107">Create a new [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51de8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51de8-108">Prerequisites</span></span>
<span data-ttu-id="51de8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51de8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51de8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51de8-111">Permission type</span></span>|<span data-ttu-id="51de8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51de8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51de8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51de8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="51de8-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51de8-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="51de8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51de8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51de8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51de8-116">Not supported.</span></span>|
|<span data-ttu-id="51de8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51de8-117">Application</span></span>|<span data-ttu-id="51de8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51de8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51de8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51de8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="51de8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51de8-120">Request headers</span></span>
|<span data-ttu-id="51de8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51de8-121">Header</span></span>|<span data-ttu-id="51de8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="51de8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51de8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="51de8-123">Authorization</span></span>|<span data-ttu-id="51de8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51de8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51de8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="51de8-125">Accept</span></span>|<span data-ttu-id="51de8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="51de8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51de8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51de8-127">Request body</span></span>
<span data-ttu-id="51de8-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto termsAndConditionsAcceptanceStatus.</span><span class="sxs-lookup"><span data-stu-id="51de8-128">In the request body, supply a JSON representation for the termsAndConditionsAcceptanceStatus object.</span></span>

<span data-ttu-id="51de8-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto termsAndConditionsAcceptanceStatus.</span><span class="sxs-lookup"><span data-stu-id="51de8-129">The following table shows the properties that are required when you create the termsAndConditionsAcceptanceStatus.</span></span>

|<span data-ttu-id="51de8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51de8-130">Property</span></span>|<span data-ttu-id="51de8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="51de8-131">Type</span></span>|<span data-ttu-id="51de8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="51de8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="51de8-133">id</span><span class="sxs-lookup"><span data-stu-id="51de8-133">id</span></span>|<span data-ttu-id="51de8-134">String</span><span class="sxs-lookup"><span data-stu-id="51de8-134">String</span></span>|<span data-ttu-id="51de8-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="51de8-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="51de8-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="51de8-136">userDisplayName</span></span>|<span data-ttu-id="51de8-137">String</span><span class="sxs-lookup"><span data-stu-id="51de8-137">String</span></span>|<span data-ttu-id="51de8-138">Nombre para mostrar del usuario cuya aceptación representa la entidad.</span><span class="sxs-lookup"><span data-stu-id="51de8-138">Display name of the user whose acceptance the entity represents.</span></span>|
|<span data-ttu-id="51de8-139">acceptedVersion</span><span class="sxs-lookup"><span data-stu-id="51de8-139">acceptedVersion</span></span>|<span data-ttu-id="51de8-140">Int32</span><span class="sxs-lookup"><span data-stu-id="51de8-140">Int32</span></span>|<span data-ttu-id="51de8-141">Número de versión más reciente de los TyC aceptados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="51de8-141">Most recent version number of the T&C accepted by the user.</span></span>|
|<span data-ttu-id="51de8-142">acceptedDateTime</span><span class="sxs-lookup"><span data-stu-id="51de8-142">acceptedDateTime</span></span>|<span data-ttu-id="51de8-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="51de8-143">DateTimeOffset</span></span>|<span data-ttu-id="51de8-144">Fecha y hora en la que el usuario aceptó los términos por última vez.</span><span class="sxs-lookup"><span data-stu-id="51de8-144">DateTime when the terms were last accepted by the user.</span></span>|



## <a name="response"></a><span data-ttu-id="51de8-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51de8-145">Response</span></span>
<span data-ttu-id="51de8-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51de8-146">If successful, this method returns a `201 Created` response code and a [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51de8-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51de8-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="51de8-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51de8-148">Request</span></span>
<span data-ttu-id="51de8-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51de8-149">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```

### <a name="response"></a><span data-ttu-id="51de8-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51de8-150">Response</span></span>
<span data-ttu-id="51de8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51de8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 260

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "a045ce1a-ce1a-a045-1ace-45a01ace45a0",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```





