---
title: Crear termsAndConditionsAcceptanceStatus
description: Cree un objeto termsAndConditionsAcceptanceStatus.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c7ab313bb58e83c2d5ca9804fb84d95e807a4841
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863199"
---
# <a name="create-termsandconditionsacceptancestatus"></a><span data-ttu-id="fdc10-103">Crear termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="fdc10-103">Create termsAndConditionsAcceptanceStatus</span></span>

> <span data-ttu-id="fdc10-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fdc10-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fdc10-105">Cree un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="fdc10-105">Create a new [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fdc10-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fdc10-106">Prerequisites</span></span>
<span data-ttu-id="fdc10-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fdc10-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fdc10-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdc10-109">Permission type</span></span>|<span data-ttu-id="fdc10-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdc10-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fdc10-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdc10-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fdc10-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fdc10-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="fdc10-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdc10-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fdc10-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdc10-114">Not supported.</span></span>|
|<span data-ttu-id="fdc10-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdc10-115">Application</span></span>|<span data-ttu-id="fdc10-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdc10-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fdc10-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdc10-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="fdc10-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fdc10-118">Request headers</span></span>
|<span data-ttu-id="fdc10-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdc10-119">Header</span></span>|<span data-ttu-id="fdc10-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fdc10-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fdc10-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fdc10-121">Authorization</span></span>|<span data-ttu-id="fdc10-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fdc10-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fdc10-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fdc10-123">Accept</span></span>|<span data-ttu-id="fdc10-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fdc10-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fdc10-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fdc10-125">Request body</span></span>
<span data-ttu-id="fdc10-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto termsAndConditionsAcceptanceStatus.</span><span class="sxs-lookup"><span data-stu-id="fdc10-126">In the request body, supply a JSON representation for the termsAndConditionsAcceptanceStatus object.</span></span>

<span data-ttu-id="fdc10-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto termsAndConditionsAcceptanceStatus.</span><span class="sxs-lookup"><span data-stu-id="fdc10-127">The following table shows the properties that are required when you create the termsAndConditionsAcceptanceStatus.</span></span>

|<span data-ttu-id="fdc10-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fdc10-128">Property</span></span>|<span data-ttu-id="fdc10-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdc10-129">Type</span></span>|<span data-ttu-id="fdc10-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdc10-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fdc10-131">id</span><span class="sxs-lookup"><span data-stu-id="fdc10-131">id</span></span>|<span data-ttu-id="fdc10-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="fdc10-132">String</span></span>|<span data-ttu-id="fdc10-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fdc10-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="fdc10-134">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="fdc10-134">userDisplayName</span></span>|<span data-ttu-id="fdc10-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="fdc10-135">String</span></span>|<span data-ttu-id="fdc10-136">Nombre para mostrar del usuario cuya aceptación representa la entidad.</span><span class="sxs-lookup"><span data-stu-id="fdc10-136">Display name of the user whose acceptance the entity represents.</span></span>|
|<span data-ttu-id="fdc10-137">acceptedVersion</span><span class="sxs-lookup"><span data-stu-id="fdc10-137">acceptedVersion</span></span>|<span data-ttu-id="fdc10-138">Int32</span><span class="sxs-lookup"><span data-stu-id="fdc10-138">Int32</span></span>|<span data-ttu-id="fdc10-139">Número de versión más reciente de los TyC aceptados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="fdc10-139">Most recent version number of the T&C accepted by the user.</span></span>|
|<span data-ttu-id="fdc10-140">acceptedDateTime</span><span class="sxs-lookup"><span data-stu-id="fdc10-140">acceptedDateTime</span></span>|<span data-ttu-id="fdc10-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fdc10-141">DateTimeOffset</span></span>|<span data-ttu-id="fdc10-142">Fecha y hora en la que el usuario aceptó los términos por última vez.</span><span class="sxs-lookup"><span data-stu-id="fdc10-142">DateTime when the terms were last accepted by the user.</span></span>|



## <a name="response"></a><span data-ttu-id="fdc10-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdc10-143">Response</span></span>
<span data-ttu-id="fdc10-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fdc10-144">If successful, this method returns a `201 Created` response code and a [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fdc10-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdc10-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="fdc10-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fdc10-146">Request</span></span>
<span data-ttu-id="fdc10-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fdc10-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses
Content-type: application/json
Content-length: 211

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "userDisplayName": "User Display Name value",
  "acceptedVersion": 15,
  "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
}
```

### <a name="response"></a><span data-ttu-id="fdc10-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdc10-148">Response</span></span>
<span data-ttu-id="fdc10-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fdc10-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



