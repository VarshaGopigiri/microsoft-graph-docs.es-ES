---
title: 'reportRoot: getOneDriveUsageStorage'
description: Obtiene las tendencias sobre la cantidad de almacenamiento que usa en OneDrive para la Empresa.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 61982c9013d5827fa9b47e4c98d453e4cf8f2b94
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27936056"
---
# <a name="reportroot-getonedriveusagestorage"></a><span data-ttu-id="b08f7-103">reportRoot: getOneDriveUsageStorage</span><span class="sxs-lookup"><span data-stu-id="b08f7-103">reportRoot: getOneDriveUsageStorage</span></span>

<span data-ttu-id="b08f7-104">Obtiene las tendencias sobre la cantidad de almacenamiento que usa en OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="b08f7-104">Get the trend on the amount of storage you are using in OneDrive for Business.</span></span>

> <span data-ttu-id="b08f7-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span><span class="sxs-lookup"><span data-stu-id="b08f7-105">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="b08f7-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="b08f7-106">Permissions</span></span>

<span data-ttu-id="b08f7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b08f7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b08f7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b08f7-109">Permission type</span></span>                        | <span data-ttu-id="b08f7-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b08f7-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="b08f7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b08f7-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="b08f7-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b08f7-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="b08f7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b08f7-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b08f7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b08f7-114">Not supported.</span></span>                           |
| <span data-ttu-id="b08f7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b08f7-115">Application</span></span>                            | <span data-ttu-id="b08f7-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b08f7-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="b08f7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b08f7-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageStorage(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="b08f7-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="b08f7-118">Function parameters</span></span>

<span data-ttu-id="b08f7-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="b08f7-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="b08f7-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b08f7-120">Parameter</span></span> | <span data-ttu-id="b08f7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b08f7-121">Type</span></span>   | <span data-ttu-id="b08f7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b08f7-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="b08f7-123">period</span><span class="sxs-lookup"><span data-stu-id="b08f7-123">period</span></span>    | <span data-ttu-id="b08f7-124">cadena</span><span class="sxs-lookup"><span data-stu-id="b08f7-124">string</span></span> | <span data-ttu-id="b08f7-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b08f7-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="b08f7-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="b08f7-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="b08f7-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b08f7-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="b08f7-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="b08f7-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="b08f7-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b08f7-129">Request headers</span></span>

| <span data-ttu-id="b08f7-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="b08f7-130">Name</span></span>          | <span data-ttu-id="b08f7-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b08f7-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="b08f7-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="b08f7-132">Authorization</span></span> | <span data-ttu-id="b08f7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b08f7-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="b08f7-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="b08f7-135">If-None-Match</span></span> | <span data-ttu-id="b08f7-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="b08f7-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="b08f7-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b08f7-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="b08f7-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b08f7-138">Response</span></span>

<span data-ttu-id="b08f7-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="b08f7-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="b08f7-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b08f7-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="b08f7-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="b08f7-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="b08f7-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="b08f7-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="b08f7-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="b08f7-143">Report Refresh Date</span></span>
- <span data-ttu-id="b08f7-144">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="b08f7-144">Site Type</span></span>
- <span data-ttu-id="b08f7-145">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="b08f7-145">Storage Used (Byte)</span></span>
- <span data-ttu-id="b08f7-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="b08f7-146">Report Date</span></span>
- <span data-ttu-id="b08f7-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="b08f7-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="b08f7-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b08f7-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b08f7-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b08f7-149">Request</span></span>

<span data-ttu-id="b08f7-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b08f7-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getonedriveusagestorage"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageStorage(period='D7')
```

#### <a name="response"></a><span data-ttu-id="b08f7-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b08f7-151">Response</span></span>

<span data-ttu-id="b08f7-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b08f7-152">The following is an example of the response.</span></span>

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

<span data-ttu-id="b08f7-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="b08f7-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Storage Used (Byte),Report Date,Report Period
```
