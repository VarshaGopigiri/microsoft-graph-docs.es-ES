# <a name="reportroot-getmailboxusagedetail"></a><span data-ttu-id="ddda7-101">reportRoot: getMailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="ddda7-101">reportRoot: getMailboxUsageDetail</span></span>

<span data-ttu-id="ddda7-102">Obtiene información sobre el uso de buzones.</span><span class="sxs-lookup"><span data-stu-id="ddda7-102">Get details about mailbox usage.</span></span>

> <span data-ttu-id="ddda7-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="ddda7-103">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="ddda7-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="ddda7-104">Permissions</span></span>

<span data-ttu-id="ddda7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ddda7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="ddda7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ddda7-107">Permission type</span></span>                        | <span data-ttu-id="ddda7-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ddda7-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ddda7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ddda7-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="ddda7-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ddda7-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ddda7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ddda7-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ddda7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ddda7-112">Not supported.</span></span>                           |
| <span data-ttu-id="ddda7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ddda7-113">Application</span></span>                            | <span data-ttu-id="ddda7-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ddda7-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ddda7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddda7-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageDetail(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="ddda7-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ddda7-116">Function parameters</span></span>

<span data-ttu-id="ddda7-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ddda7-117">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ddda7-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ddda7-118">Parameter</span></span> | <span data-ttu-id="ddda7-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddda7-119">Type</span></span>   | <span data-ttu-id="ddda7-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddda7-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ddda7-121">period</span><span class="sxs-lookup"><span data-stu-id="ddda7-121">period</span></span>    | <span data-ttu-id="ddda7-122">cadena</span><span class="sxs-lookup"><span data-stu-id="ddda7-122">string</span></span> | <span data-ttu-id="ddda7-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ddda7-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ddda7-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ddda7-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ddda7-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ddda7-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ddda7-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ddda7-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="ddda7-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddda7-127">Request headers</span></span>

| <span data-ttu-id="ddda7-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddda7-128">Name</span></span>          | <span data-ttu-id="ddda7-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddda7-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="ddda7-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="ddda7-130">Authorization</span></span> | <span data-ttu-id="ddda7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddda7-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="ddda7-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="ddda7-133">If-None-Match</span></span> | <span data-ttu-id="ddda7-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ddda7-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="ddda7-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ddda7-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ddda7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddda7-136">Response</span></span>

<span data-ttu-id="ddda7-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ddda7-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ddda7-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddda7-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ddda7-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ddda7-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ddda7-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ddda7-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ddda7-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ddda7-141">Report Refresh Date</span></span>
- <span data-ttu-id="ddda7-142">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="ddda7-142">User Principal Name</span></span>
- <span data-ttu-id="ddda7-143">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="ddda7-143">Display Name</span></span>
- <span data-ttu-id="ddda7-144">Eliminado</span><span class="sxs-lookup"><span data-stu-id="ddda7-144">Is Deleted</span></span>
- <span data-ttu-id="ddda7-145">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="ddda7-145">Deleted Date</span></span>
- <span data-ttu-id="ddda7-146">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="ddda7-146">Created Date</span></span>
- <span data-ttu-id="ddda7-147">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="ddda7-147">Last Activity Date</span></span>
- <span data-ttu-id="ddda7-148">Número de elementos</span><span class="sxs-lookup"><span data-stu-id="ddda7-148">Item Count</span></span>
- <span data-ttu-id="ddda7-149">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="ddda7-149">Storage Used (Byte)</span></span>
- <span data-ttu-id="ddda7-150">Cuota de advertencia de problema (bytes)</span><span class="sxs-lookup"><span data-stu-id="ddda7-150">Issue Warning Quota (Byte)</span></span>
- <span data-ttu-id="ddda7-151">Cuota de prohibición de envío (bytes)</span><span class="sxs-lookup"><span data-stu-id="ddda7-151">Prohibit Send Quota (Byte)</span></span>
- <span data-ttu-id="ddda7-152">Cuota de prohibición de envío o recepción (bytes)</span><span class="sxs-lookup"><span data-stu-id="ddda7-152">Prohibit Send/Receive Quota (Byte)</span></span>
- <span data-ttu-id="ddda7-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ddda7-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="ddda7-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddda7-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ddda7-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ddda7-155">Request</span></span>

<span data-ttu-id="ddda7-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddda7-156">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getmailboxusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="ddda7-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddda7-157">Response</span></span>

<span data-ttu-id="ddda7-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddda7-158">The following is an example of the response.</span></span>

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

<span data-ttu-id="ddda7-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ddda7-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Created Date,Last Activity Date,Item Count,Storage Used (Byte),Issue Warning Quota (Byte),Prohibit Send Quota (Byte),Prohibit Send/Receive Quota (Byte),Report Period
```
