---
title: 'reportRoot: getOffice365ActivationsUserDetail'
description: Obtiene información sobre qué usuarios activaron Office 365.
localization_priority: Normal
ms.openlocfilehash: 8266d853e4da7935f66845bb5968ec49ba2ed80f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855625"
---
# <a name="reportroot-getoffice365activationsuserdetail"></a><span data-ttu-id="7074b-103">reportRoot: getOffice365ActivationsUserDetail</span><span class="sxs-lookup"><span data-stu-id="7074b-103">reportRoot: getOffice365ActivationsUserDetail</span></span>

<span data-ttu-id="7074b-104">Obtiene información sobre qué usuarios activaron Office 365.</span><span class="sxs-lookup"><span data-stu-id="7074b-104">Get details about users who have activated Office 365.</span></span>

> <span data-ttu-id="7074b-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="7074b-105">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="7074b-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="7074b-106">Permissions</span></span>

<span data-ttu-id="7074b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7074b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7074b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7074b-109">Permission type</span></span>                        | <span data-ttu-id="7074b-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7074b-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7074b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7074b-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="7074b-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7074b-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7074b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7074b-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7074b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7074b-114">Not supported.</span></span>                           |
| <span data-ttu-id="7074b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7074b-115">Application</span></span>                            | <span data-ttu-id="7074b-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7074b-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7074b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7074b-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationsUserDetail
```

## <a name="request-headers"></a><span data-ttu-id="7074b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7074b-118">Request headers</span></span>

| <span data-ttu-id="7074b-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="7074b-119">Name</span></span>          | <span data-ttu-id="7074b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="7074b-120">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="7074b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="7074b-121">Authorization</span></span> | <span data-ttu-id="7074b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7074b-p102">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="7074b-124">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="7074b-124">If-None-Match</span></span> | <span data-ttu-id="7074b-125">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="7074b-125">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="7074b-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7074b-126">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="7074b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7074b-127">Response</span></span>

<span data-ttu-id="7074b-128">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7074b-128">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7074b-129">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7074b-129">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7074b-130">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7074b-130">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7074b-131">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7074b-131">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7074b-132">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7074b-132">Report Refresh Date</span></span>
- <span data-ttu-id="7074b-133">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="7074b-133">User Principal Name</span></span>
- <span data-ttu-id="7074b-134">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="7074b-134">Display Name</span></span>
- <span data-ttu-id="7074b-135">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="7074b-135">Product Type</span></span>
- <span data-ttu-id="7074b-136">Fecha de la última activación</span><span class="sxs-lookup"><span data-stu-id="7074b-136">Last Activated Date</span></span>
- <span data-ttu-id="7074b-137">Windows</span><span class="sxs-lookup"><span data-stu-id="7074b-137">Windows</span></span>
- <span data-ttu-id="7074b-138">Mac</span><span class="sxs-lookup"><span data-stu-id="7074b-138">Mac</span></span>
- <span data-ttu-id="7074b-139">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="7074b-139">Windows 10 Mobile</span></span>
- <span data-ttu-id="7074b-140">iOS</span><span class="sxs-lookup"><span data-stu-id="7074b-140">iOS</span></span>
- <span data-ttu-id="7074b-141">Android</span><span class="sxs-lookup"><span data-stu-id="7074b-141">Android</span></span>
- <span data-ttu-id="7074b-142">Activa en un equipo compartido</span><span class="sxs-lookup"><span data-stu-id="7074b-142">Activated On Shared Computer</span></span>

## <a name="example"></a><span data-ttu-id="7074b-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7074b-143">Example</span></span>

#### <a name="request"></a><span data-ttu-id="7074b-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7074b-144">Request</span></span>

<span data-ttu-id="7074b-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7074b-145">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activationsuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActivationsUserDetail
```

#### <a name="response"></a><span data-ttu-id="7074b-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7074b-146">Response</span></span>

<span data-ttu-id="7074b-147">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7074b-147">The following is an example of the response.</span></span>

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

<span data-ttu-id="7074b-148">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7074b-148">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Product Type,Last Activated Date,Windows,Mac,Windows 10 Mobile,iOS,Android,Activated On Shared Computer
```
