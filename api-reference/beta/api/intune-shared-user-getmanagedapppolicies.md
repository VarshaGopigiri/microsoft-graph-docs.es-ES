---
title: Función getManagedAppPolicies
description: Obtiene las restricciones de aplicaciones de un usuario determinado.
author: tfitzmac
ms.openlocfilehash: 9b0729e986a7ab3434d2682d157e45f543d558a6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354799"
---
# <a name="getmanagedapppolicies-function"></a><span data-ttu-id="499dc-103">Función getManagedAppPolicies</span><span class="sxs-lookup"><span data-stu-id="499dc-103">getManagedAppPolicies function</span></span>

> <span data-ttu-id="499dc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="499dc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="499dc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="499dc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="499dc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="499dc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="499dc-107">Obtiene las restricciones de aplicaciones de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="499dc-107">Gets app restrictions for a given user.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="499dc-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="499dc-108">Prerequisites</span></span>

<span data-ttu-id="499dc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="499dc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="499dc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="499dc-111">Permission type</span></span>|<span data-ttu-id="499dc-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="499dc-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="499dc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="499dc-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="499dc-114">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="499dc-114">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="499dc-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="499dc-115">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="499dc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="499dc-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="499dc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="499dc-117">Not supported.</span></span>|
|<span data-ttu-id="499dc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="499dc-118">Application</span></span>|<span data-ttu-id="499dc-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="499dc-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="499dc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="499dc-120">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedAppPolicies
```

## <a name="request-headers"></a><span data-ttu-id="499dc-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="499dc-121">Request headers</span></span>

|<span data-ttu-id="499dc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="499dc-122">Header</span></span>|<span data-ttu-id="499dc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="499dc-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="499dc-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="499dc-124">Authorization</span></span>|<span data-ttu-id="499dc-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="499dc-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="499dc-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="499dc-126">Accept</span></span>|<span data-ttu-id="499dc-127">application/json</span><span class="sxs-lookup"><span data-stu-id="499dc-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="499dc-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="499dc-128">Request body</span></span>

<span data-ttu-id="499dc-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="499dc-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="499dc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="499dc-130">Response</span></span>

<span data-ttu-id="499dc-131">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="499dc-131">If successful, this function returns a `200 OK` response code and a [managedAppPolicy](../resources/intune-mam-managedapppolicy.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="499dc-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="499dc-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="499dc-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="499dc-133">Request</span></span>

<span data-ttu-id="499dc-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="499dc-134">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users/{usersId}/getManagedAppPolicies
```

### <a name="response"></a><span data-ttu-id="499dc-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="499dc-135">Response</span></span>

<span data-ttu-id="499dc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="499dc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 401

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppPolicy",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "3c7b9675-9675-3c7b-7596-7b3c75967b3c",
      "version": "Version value"
    }
  ]
}
```






