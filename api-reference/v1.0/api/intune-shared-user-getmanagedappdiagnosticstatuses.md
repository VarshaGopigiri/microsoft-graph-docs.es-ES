---
title: Función getManagedAppDiagnosticStatuses
description: Obtiene estados de validación de diagnósticos de un usuario determinado.
ms.openlocfilehash: 9ba27e90de7faff043e1acbb755bc2c9d36c43fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031613"
---
# <a name="getmanagedappdiagnosticstatuses-function"></a><span data-ttu-id="b2912-103">Función getManagedAppDiagnosticStatuses</span><span class="sxs-lookup"><span data-stu-id="b2912-103">getManagedAppDiagnosticStatuses function</span></span>

> <span data-ttu-id="b2912-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2912-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2912-105">Obtiene estados de validación de diagnósticos de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="b2912-105">Gets diagnostics validation status for a given user.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b2912-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2912-106">Prerequisites</span></span>
<span data-ttu-id="b2912-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b2912-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b2912-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2912-109">Permission type</span></span>|<span data-ttu-id="b2912-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2912-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b2912-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2912-111">Delegated (work or school account)</span></span>| <span data-ttu-id="b2912-112">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="b2912-112">_varies by context_</span></span>|
| <span data-ttu-id="b2912-113">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="b2912-113">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="b2912-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b2912-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
|<span data-ttu-id="b2912-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2912-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b2912-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2912-116">Not supported.</span></span>|
|<span data-ttu-id="b2912-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2912-117">Application</span></span>|<span data-ttu-id="b2912-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2912-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b2912-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2912-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/getManagedAppDiagnosticStatuses
```

## <a name="request-headers"></a><span data-ttu-id="b2912-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2912-120">Request headers</span></span>
|<span data-ttu-id="b2912-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2912-121">Header</span></span>|<span data-ttu-id="b2912-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b2912-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b2912-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b2912-123">Authorization</span></span>|<span data-ttu-id="b2912-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b2912-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b2912-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b2912-125">Accept</span></span>|<span data-ttu-id="b2912-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b2912-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b2912-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2912-127">Request body</span></span>
<span data-ttu-id="b2912-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b2912-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b2912-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2912-129">Response</span></span>
<span data-ttu-id="b2912-130">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [managedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2912-130">If successful, this function returns a `200 OK` response code and a [managedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2912-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2912-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="b2912-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2912-132">Request</span></span>
<span data-ttu-id="b2912-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2912-133">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}/getManagedAppDiagnosticStatuses
```

### <a name="response"></a><span data-ttu-id="b2912-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2912-134">Response</span></span>
<span data-ttu-id="b2912-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2912-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 249

{
  "value": [
    {
      "@odata.type": "microsoft.graph.managedAppDiagnosticStatus",
      "validationName": "Validation Name value",
      "state": "State value",
      "mitigationInstruction": "Mitigation Instruction value"
    }
  ]
}
```



