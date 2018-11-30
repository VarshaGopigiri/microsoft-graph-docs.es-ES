---
title: 'reportRoot: getOffice365ActivationCounts'
description: Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio.
ms.openlocfilehash: efceb1d1096192cd66e8e0cde2bc6d4e4890f7fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030128"
---
# <a name="reportroot-getoffice365activationcounts"></a><span data-ttu-id="0fc63-103">reportRoot: getOffice365ActivationCounts</span><span class="sxs-lookup"><span data-stu-id="0fc63-103">reportRoot: getOffice365ActivationCounts</span></span>

<span data-ttu-id="0fc63-104">Obtiene el número de activaciones de Office 365 en dispositivos y equipos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="0fc63-104">Get the count of Office 365 activations on desktops and devices.</span></span>

> <span data-ttu-id="0fc63-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="0fc63-105">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="0fc63-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="0fc63-106">Permissions</span></span>

<span data-ttu-id="0fc63-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0fc63-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0fc63-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0fc63-109">Permission type</span></span>                        | <span data-ttu-id="0fc63-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0fc63-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="0fc63-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0fc63-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="0fc63-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0fc63-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="0fc63-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0fc63-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0fc63-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0fc63-114">Not supported.</span></span>                           |
| <span data-ttu-id="0fc63-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0fc63-115">Application</span></span>                            | <span data-ttu-id="0fc63-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0fc63-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="0fc63-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0fc63-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationCounts
```

## <a name="request-headers"></a><span data-ttu-id="0fc63-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0fc63-118">Request headers</span></span>

| <span data-ttu-id="0fc63-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="0fc63-119">Name</span></span>          | <span data-ttu-id="0fc63-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc63-120">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="0fc63-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="0fc63-121">Authorization</span></span> | <span data-ttu-id="0fc63-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0fc63-p102">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="0fc63-124">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="0fc63-124">If-None-Match</span></span> | <span data-ttu-id="0fc63-125">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="0fc63-125">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="0fc63-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0fc63-126">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="0fc63-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fc63-127">Response</span></span>

<span data-ttu-id="0fc63-128">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="0fc63-128">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="0fc63-129">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fc63-129">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="0fc63-130">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="0fc63-130">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="0fc63-131">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="0fc63-131">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="0fc63-132">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="0fc63-132">Report Refresh Date</span></span>
- <span data-ttu-id="0fc63-133">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="0fc63-133">Product Type</span></span>
- <span data-ttu-id="0fc63-134">Windows</span><span class="sxs-lookup"><span data-stu-id="0fc63-134">Windows</span></span>
- <span data-ttu-id="0fc63-135">Mac</span><span class="sxs-lookup"><span data-stu-id="0fc63-135">Mac</span></span>
- <span data-ttu-id="0fc63-136">Android</span><span class="sxs-lookup"><span data-stu-id="0fc63-136">Android</span></span>
- <span data-ttu-id="0fc63-137">iOS</span><span class="sxs-lookup"><span data-stu-id="0fc63-137">iOS</span></span>
- <span data-ttu-id="0fc63-138">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="0fc63-138">Windows 10 Mobile</span></span>

## <a name="example"></a><span data-ttu-id="0fc63-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0fc63-139">Example</span></span>

#### <a name="request"></a><span data-ttu-id="0fc63-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0fc63-140">Request</span></span>

<span data-ttu-id="0fc63-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0fc63-141">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activationcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActivationCounts
```

#### <a name="response"></a><span data-ttu-id="0fc63-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fc63-142">Response</span></span>

<span data-ttu-id="0fc63-143">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fc63-143">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="0fc63-144">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="0fc63-144">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Product Type,Windows,Mac,Android,iOS,Windows 10 Mobile
```
