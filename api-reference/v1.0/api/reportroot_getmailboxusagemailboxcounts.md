# <a name="reportroot-getmailboxusagemailboxcounts"></a><span data-ttu-id="7a07a-101">reportRoot: getMailboxUsageMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="7a07a-101">reportRoot: getMailboxUsageMailboxCounts</span></span>

<span data-ttu-id="7a07a-102">Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe.</span><span class="sxs-lookup"><span data-stu-id="7a07a-102">Get the total number of user mailboxes in your organization and how many are active each day of the reporting period.</span></span> <span data-ttu-id="7a07a-103">Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7a07a-103">A mailbox is considered active if the user sent or read any email.</span></span>

> <span data-ttu-id="7a07a-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones]((https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729)).</span><span class="sxs-lookup"><span data-stu-id="7a07a-104">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage]((https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729)).</span></span>

## <a name="permissions"></a><span data-ttu-id="7a07a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7a07a-105">Permissions</span></span>

<span data-ttu-id="7a07a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7a07a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="7a07a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a07a-108">Permission type</span></span>                        | <span data-ttu-id="7a07a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a07a-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7a07a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a07a-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="7a07a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a07a-111">Not supported.</span></span>                           |
| <span data-ttu-id="7a07a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a07a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7a07a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a07a-113">Not supported.</span></span>                           |
| <span data-ttu-id="7a07a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a07a-114">Application</span></span>                            | <span data-ttu-id="7a07a-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7a07a-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7a07a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a07a-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageMailboxCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="7a07a-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7a07a-117">Request parameters</span></span>

<span data-ttu-id="7a07a-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="7a07a-118">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="7a07a-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7a07a-119">Parameter</span></span> | <span data-ttu-id="7a07a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a07a-120">Type</span></span>   | <span data-ttu-id="7a07a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a07a-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="7a07a-122">period</span><span class="sxs-lookup"><span data-stu-id="7a07a-122">Period</span></span>    | <span data-ttu-id="7a07a-123">cadena</span><span class="sxs-lookup"><span data-stu-id="7a07a-123">string</span></span> | <span data-ttu-id="7a07a-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7a07a-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="7a07a-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="7a07a-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="7a07a-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7a07a-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="7a07a-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7a07a-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="7a07a-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a07a-128">Request headers</span></span>

| <span data-ttu-id="7a07a-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a07a-129">Name</span></span>          | <span data-ttu-id="7a07a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a07a-130">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="7a07a-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="7a07a-131">Authorization</span></span> | <span data-ttu-id="7a07a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7a07a-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="7a07a-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="7a07a-134">if-none-match</span></span> | <span data-ttu-id="7a07a-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="7a07a-135">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `304 Not Modified` response is returned.</span></span> <span data-ttu-id="7a07a-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7a07a-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="7a07a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a07a-137">Response</span></span>

<span data-ttu-id="7a07a-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7a07a-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7a07a-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a07a-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7a07a-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7a07a-140">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

<span data-ttu-id="7a07a-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7a07a-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7a07a-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7a07a-142">Report Refresh Date</span></span>
- <span data-ttu-id="7a07a-143">Total</span><span class="sxs-lookup"><span data-stu-id="7a07a-143">total</span></span>
- <span data-ttu-id="7a07a-144">Activo</span><span class="sxs-lookup"><span data-stu-id="7a07a-144">Active</span></span>
- <span data-ttu-id="7a07a-145">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="7a07a-145">Report Date</span></span>
- <span data-ttu-id="7a07a-146">Período del informe</span><span class="sxs-lookup"><span data-stu-id="7a07a-146">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="7a07a-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a07a-147">Example</span></span>

#### <a name="request"></a><span data-ttu-id="7a07a-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a07a-148">Request</span></span>

<span data-ttu-id="7a07a-149">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a07a-149">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagemailboxcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageMailboxCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="7a07a-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a07a-150">Response</span></span>

<span data-ttu-id="7a07a-151">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a07a-151">Here is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="7a07a-152">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a07a-152">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Total,Active,Report Date,Report Period
```
