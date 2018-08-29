# <a name="reportroot-getmailboxusagequotastatusmailboxcounts"></a><span data-ttu-id="c591a-101">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="c591a-101">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span></span>

<span data-ttu-id="c591a-102">Obtiene el número de buzones de usuario en cada categoría de cuota.</span><span class="sxs-lookup"><span data-stu-id="c591a-102">Get the count of user mailboxes in each quota category.</span></span>

> <span data-ttu-id="c591a-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="c591a-103">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="c591a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="c591a-104">Permissions</span></span>

<span data-ttu-id="c591a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c591a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="c591a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c591a-107">Permission type</span></span>                        | <span data-ttu-id="c591a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c591a-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c591a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c591a-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="c591a-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c591a-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="c591a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c591a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c591a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c591a-112">Not supported.</span></span>                           |
| <span data-ttu-id="c591a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c591a-113">Application</span></span>                            | <span data-ttu-id="c591a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c591a-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c591a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c591a-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageQuotaStatusMailboxCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="c591a-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c591a-116">Request parameters</span></span>

<span data-ttu-id="c591a-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="c591a-117">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="c591a-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c591a-118">Parameter</span></span> | <span data-ttu-id="c591a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c591a-119">Type</span></span>   | <span data-ttu-id="c591a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c591a-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c591a-121">period</span><span class="sxs-lookup"><span data-stu-id="c591a-121">period</span></span>    | <span data-ttu-id="c591a-122">cadena</span><span class="sxs-lookup"><span data-stu-id="c591a-122">string</span></span> | <span data-ttu-id="c591a-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c591a-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c591a-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="c591a-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c591a-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c591a-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c591a-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="c591a-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="c591a-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c591a-127">Request headers</span></span>

| <span data-ttu-id="c591a-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="c591a-128">Name</span></span>          | <span data-ttu-id="c591a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c591a-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="c591a-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="c591a-130">Authorization</span></span> | <span data-ttu-id="c591a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c591a-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="c591a-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="c591a-133">If-None-Match</span></span> | <span data-ttu-id="c591a-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="c591a-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="c591a-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c591a-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="c591a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c591a-136">Response</span></span>

<span data-ttu-id="c591a-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="c591a-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c591a-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c591a-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c591a-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="c591a-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="c591a-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c591a-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c591a-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="c591a-141">Report Refresh Date</span></span>
- <span data-ttu-id="c591a-142">Por debajo del límite</span><span class="sxs-lookup"><span data-stu-id="c591a-142">Under Limit</span></span>
- <span data-ttu-id="c591a-143">Advertencia emitida</span><span class="sxs-lookup"><span data-stu-id="c591a-143">Warning Issued</span></span>
- <span data-ttu-id="c591a-144">Envío prohibido</span><span class="sxs-lookup"><span data-stu-id="c591a-144">Send Prohibited</span></span>
- <span data-ttu-id="c591a-145">Envío o recepción prohibidos</span><span class="sxs-lookup"><span data-stu-id="c591a-145">Send/Receive Prohibited</span></span>
- <span data-ttu-id="c591a-146">Indeterminado</span><span class="sxs-lookup"><span data-stu-id="c591a-146">Indeterminate</span></span>
- <span data-ttu-id="c591a-147">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="c591a-147">Report Date</span></span>
- <span data-ttu-id="c591a-148">Período del informe</span><span class="sxs-lookup"><span data-stu-id="c591a-148">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="c591a-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c591a-149">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c591a-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c591a-150">Request</span></span>

<span data-ttu-id="c591a-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c591a-151">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getmailboxusagequotastatusmailboxcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageQuotaStatusMailboxCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="c591a-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c591a-152">Response</span></span>

<span data-ttu-id="c591a-153">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c591a-153">The following is an example of the response.</span></span>

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

<span data-ttu-id="c591a-154">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="c591a-154">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Under Limit,Warning Issued,Send Prohibited,Send/Receive Prohibited,Indeterminate,Report Date,Report Period
```
