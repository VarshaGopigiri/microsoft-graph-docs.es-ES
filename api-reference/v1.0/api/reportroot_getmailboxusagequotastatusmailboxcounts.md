# <a name="reportroot-getmailboxusagequotastatusmailboxcounts"></a><span data-ttu-id="8f886-101">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="8f886-101">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span></span>

<span data-ttu-id="8f886-102">Obtiene el número de buzones de usuario en cada categoría de cuota.</span><span class="sxs-lookup"><span data-stu-id="8f886-102">Get the count of user mailboxes in each quota category.</span></span>

> <span data-ttu-id="8f886-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones]((https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729)).</span><span class="sxs-lookup"><span data-stu-id="8f886-103">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage]((https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729)).</span></span>

## <a name="permissions"></a><span data-ttu-id="8f886-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f886-104">Permissions</span></span>

<span data-ttu-id="8f886-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8f886-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="8f886-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f886-107">Permission type</span></span>                        | <span data-ttu-id="8f886-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f886-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="8f886-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f886-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="8f886-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f886-110">Not supported.</span></span>                           |
| <span data-ttu-id="8f886-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f886-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f886-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f886-112">Not supported.</span></span>                           |
| <span data-ttu-id="8f886-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f886-113">Application</span></span>                            | <span data-ttu-id="8f886-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="8f886-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="8f886-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f886-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageQuotaStatusMailboxCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="8f886-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f886-116">Request parameters</span></span>

<span data-ttu-id="8f886-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="8f886-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="8f886-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8f886-118">Parameter</span></span> | <span data-ttu-id="8f886-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f886-119">Type</span></span>   | <span data-ttu-id="8f886-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f886-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="8f886-121">period</span><span class="sxs-lookup"><span data-stu-id="8f886-121">Period</span></span>    | <span data-ttu-id="8f886-122">cadena</span><span class="sxs-lookup"><span data-stu-id="8f886-122">string</span></span> | <span data-ttu-id="8f886-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="8f886-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="8f886-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="8f886-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="8f886-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="8f886-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="8f886-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f886-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="8f886-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f886-127">Request headers</span></span>

| <span data-ttu-id="8f886-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f886-128">Name</span></span>          | <span data-ttu-id="8f886-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f886-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="8f886-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f886-130">Authorization</span></span> | <span data-ttu-id="8f886-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f886-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="8f886-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="8f886-133">if-none-match</span></span> | <span data-ttu-id="8f886-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="8f886-134">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="8f886-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8f886-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="8f886-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f886-136">Response</span></span>

<span data-ttu-id="8f886-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="8f886-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="8f886-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f886-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="8f886-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="8f886-139">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="8f886-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="8f886-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="8f886-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="8f886-141">Report Refresh Date</span></span>
- <span data-ttu-id="8f886-142">Por debajo del límite</span><span class="sxs-lookup"><span data-stu-id="8f886-142">Under Limit</span></span>
- <span data-ttu-id="8f886-143">Advertencia emitida</span><span class="sxs-lookup"><span data-stu-id="8f886-143">Warning Issued</span></span>
- <span data-ttu-id="8f886-144">Envío prohibido</span><span class="sxs-lookup"><span data-stu-id="8f886-144">Send Prohibited</span></span>
- <span data-ttu-id="8f886-145">Envío o recepción prohibidos</span><span class="sxs-lookup"><span data-stu-id="8f886-145">Send/Receive Prohibited</span></span>
- <span data-ttu-id="8f886-146">Indeterminado</span><span class="sxs-lookup"><span data-stu-id="8f886-146">Indeterminate</span></span>
- <span data-ttu-id="8f886-147">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="8f886-147">Report Date</span></span>
- <span data-ttu-id="8f886-148">Período del informe</span><span class="sxs-lookup"><span data-stu-id="8f886-148">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="8f886-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f886-149">Example</span></span>

#### <a name="request"></a><span data-ttu-id="8f886-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f886-150">Request</span></span>

<span data-ttu-id="8f886-151">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f886-151">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagequotastatusmailboxcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageQuotaStatusMailboxCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="8f886-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f886-152">Response</span></span>

<span data-ttu-id="8f886-153">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f886-153">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="8f886-154">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f886-154">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Under Limit,Warning Issued,Send Prohibited,Send/Receive Prohibited,Indeterminate,Report Date,Report Period
```
