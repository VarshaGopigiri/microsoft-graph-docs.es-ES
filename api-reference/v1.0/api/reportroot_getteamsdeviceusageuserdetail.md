# <a name="reportroot-getteamsdeviceusageuserdetail"></a><span data-ttu-id="9aa38-101">reportRoot: getTeamsDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="9aa38-101">reportRoot: getTeamsDeviceUsageUserDetail</span></span>

<span data-ttu-id="9aa38-102">Obtenga información sobre el uso de los dispositivos de Microsoft Teams por usuario.</span><span class="sxs-lookup"><span data-stu-id="9aa38-102">Get details about Yammer device usage by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="9aa38-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9aa38-103">Permissions</span></span>

<span data-ttu-id="9aa38-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9aa38-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="9aa38-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9aa38-106">Permission type</span></span>                        | <span data-ttu-id="9aa38-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9aa38-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="9aa38-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9aa38-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="9aa38-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9aa38-109">Not supported.</span></span>                           |
| <span data-ttu-id="9aa38-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9aa38-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9aa38-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9aa38-111">Not supported.</span></span>                           |
| <span data-ttu-id="9aa38-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9aa38-112">Application</span></span>                            | <span data-ttu-id="9aa38-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="9aa38-113">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="9aa38-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9aa38-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageUserDetail(period='{period_value}')
GET /reports/getTeamsDeviceUsageUserDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="9aa38-115">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9aa38-115">Request parameters</span></span>

<span data-ttu-id="9aa38-116">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="9aa38-116">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="9aa38-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9aa38-117">Parameter</span></span> | <span data-ttu-id="9aa38-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="9aa38-118">Type</span></span>   | <span data-ttu-id="9aa38-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aa38-119">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="9aa38-120">period</span><span class="sxs-lookup"><span data-stu-id="9aa38-120">period</span></span>    | <span data-ttu-id="9aa38-121">cadena</span><span class="sxs-lookup"><span data-stu-id="9aa38-121">string</span></span> | <span data-ttu-id="9aa38-122">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="9aa38-122">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="9aa38-123">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="9aa38-123">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="9aa38-124">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="9aa38-124">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="9aa38-125">date</span><span class="sxs-lookup"><span data-stu-id="9aa38-125">date</span></span>      | <span data-ttu-id="9aa38-126">Fecha</span><span class="sxs-lookup"><span data-stu-id="9aa38-126">Date</span></span>   | <span data-ttu-id="9aa38-127">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="9aa38-127">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="9aa38-128">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="9aa38-128">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="9aa38-129">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="9aa38-129">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="9aa38-130">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="9aa38-130">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9aa38-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9aa38-131">Request headers</span></span>

| <span data-ttu-id="9aa38-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="9aa38-132">Name</span></span>          | <span data-ttu-id="9aa38-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aa38-133">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="9aa38-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="9aa38-134">Authorization</span></span> | <span data-ttu-id="9aa38-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9aa38-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="9aa38-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9aa38-137">Response</span></span>

<span data-ttu-id="9aa38-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="9aa38-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="9aa38-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9aa38-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="9aa38-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="9aa38-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="9aa38-141">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="9aa38-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="9aa38-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="9aa38-142">Report Refresh Date</span></span>
- <span data-ttu-id="9aa38-143">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="9aa38-143">User Principal Name</span></span>
- <span data-ttu-id="9aa38-144">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="9aa38-144">Last Activity Date</span></span>
- <span data-ttu-id="9aa38-145">Eliminado</span><span class="sxs-lookup"><span data-stu-id="9aa38-145">Is Deleted</span></span>
- <span data-ttu-id="9aa38-146">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="9aa38-146">Deleted Date</span></span>
- <span data-ttu-id="9aa38-147">Web usada</span><span class="sxs-lookup"><span data-stu-id="9aa38-147">Used Web</span></span>
- <span data-ttu-id="9aa38-148">Windows Phone usado</span><span class="sxs-lookup"><span data-stu-id="9aa38-148">Used Windows Phone</span></span>
- <span data-ttu-id="9aa38-149">iOS usado</span><span class="sxs-lookup"><span data-stu-id="9aa38-149">Used iOS</span></span>
- <span data-ttu-id="9aa38-150">Mac usado</span><span class="sxs-lookup"><span data-stu-id="9aa38-150">Used Mac</span></span>
- <span data-ttu-id="9aa38-151">Teléfono Android usado</span><span class="sxs-lookup"><span data-stu-id="9aa38-151">Used Android Phone</span></span>
- <span data-ttu-id="9aa38-152">Windows usado</span><span class="sxs-lookup"><span data-stu-id="9aa38-152">Used Windows</span></span>
- <span data-ttu-id="9aa38-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="9aa38-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="9aa38-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9aa38-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="9aa38-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9aa38-155">Request</span></span>

<span data-ttu-id="9aa38-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9aa38-156">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsDeviceUsageUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="9aa38-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9aa38-157">Response</span></span>

<span data-ttu-id="9aa38-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9aa38-158">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="9aa38-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="9aa38-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Used Web,Used Windows Phone,Used iOS,Used Mac,Used Android Phone,Used Windows,Report Period
```
