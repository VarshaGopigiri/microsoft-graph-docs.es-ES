# <a name="reportroot-getmailboxusagedetail"></a><span data-ttu-id="3cb9a-101">reportRoot: getMailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="3cb9a-101">reportRoot: getMailboxUsageDetail</span></span>

<span data-ttu-id="3cb9a-102">Obtiene información sobre el uso de buzones.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-102">Get details about mailbox usage.</span></span>

> <span data-ttu-id="3cb9a-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="3cb9a-103">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="3cb9a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="3cb9a-104">Permissions</span></span>

<span data-ttu-id="3cb9a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3cb9a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="3cb9a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3cb9a-107">Permission type</span></span>                        | <span data-ttu-id="3cb9a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="3cb9a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="3cb9a-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-110">Not supported.</span></span>                           |
| <span data-ttu-id="3cb9a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3cb9a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-112">Not supported.</span></span>                           |
| <span data-ttu-id="3cb9a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3cb9a-113">Application</span></span>                            | <span data-ttu-id="3cb9a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3cb9a-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3cb9a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3cb9a-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageDetail(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="3cb9a-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3cb9a-116">Request parameters</span></span>

<span data-ttu-id="3cb9a-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="3cb9a-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3cb9a-118">Parameter</span></span> | <span data-ttu-id="3cb9a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3cb9a-119">Type</span></span>   | <span data-ttu-id="3cb9a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cb9a-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="3cb9a-121">period</span><span class="sxs-lookup"><span data-stu-id="3cb9a-121">period</span></span>    | <span data-ttu-id="3cb9a-122">cadena</span><span class="sxs-lookup"><span data-stu-id="3cb9a-122">string</span></span> | <span data-ttu-id="3cb9a-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="3cb9a-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="3cb9a-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="3cb9a-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="3cb9a-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3cb9a-127">Request headers</span></span>

| <span data-ttu-id="3cb9a-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="3cb9a-128">Name</span></span>          | <span data-ttu-id="3cb9a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cb9a-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="3cb9a-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="3cb9a-130">Authorization</span></span> | <span data-ttu-id="3cb9a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="3cb9a-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="3cb9a-133">If-None-Match</span></span> | <span data-ttu-id="3cb9a-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="3cb9a-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="3cb9a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3cb9a-136">Response</span></span>

<span data-ttu-id="3cb9a-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="3cb9a-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="3cb9a-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="3cb9a-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="3cb9a-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="3cb9a-141">Report Refresh Date</span></span>
- <span data-ttu-id="3cb9a-142">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="3cb9a-142">User Principal Name</span></span>
- <span data-ttu-id="3cb9a-143">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="3cb9a-143">Display Name</span></span>
- <span data-ttu-id="3cb9a-144">Eliminado</span><span class="sxs-lookup"><span data-stu-id="3cb9a-144">Is Deleted</span></span>
- <span data-ttu-id="3cb9a-145">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="3cb9a-145">Deleted Date</span></span>
- <span data-ttu-id="3cb9a-146">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="3cb9a-146">Created Date</span></span>
- <span data-ttu-id="3cb9a-147">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="3cb9a-147">Last Activity Date</span></span>
- <span data-ttu-id="3cb9a-148">Número de elementos</span><span class="sxs-lookup"><span data-stu-id="3cb9a-148">Item Count</span></span>
- <span data-ttu-id="3cb9a-149">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-149">Storage Used (Byte)</span></span>
- <span data-ttu-id="3cb9a-150">Cuota de advertencia de problema (bytes)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-150">Issue Warning Quota (Byte)</span></span>
- <span data-ttu-id="3cb9a-151">Cuota de prohibición de envío (bytes)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-151">Prohibit Send Quota (Byte)</span></span>
- <span data-ttu-id="3cb9a-152">Cuota de prohibición de envío o recepción (bytes)</span><span class="sxs-lookup"><span data-stu-id="3cb9a-152">Prohibit Send/Receive Quota (Byte)</span></span>
- <span data-ttu-id="3cb9a-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="3cb9a-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="3cb9a-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3cb9a-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="3cb9a-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3cb9a-155">Request</span></span>

<span data-ttu-id="3cb9a-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-156">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="3cb9a-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3cb9a-157">Response</span></span>

<span data-ttu-id="3cb9a-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-158">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="3cb9a-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="3cb9a-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Created Date,Last Activity Date,Item Count,Storage Used (Byte),Issue Warning Quota (Byte),Prohibit Send Quota (Byte),Prohibit Send/Receive Quota (Byte),Report Period
```
