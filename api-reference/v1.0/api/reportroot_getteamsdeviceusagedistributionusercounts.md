# <a name="reportroot-getteamsdeviceusagedistributionusercounts"></a><span data-ttu-id="bee70-101">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="bee70-101">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span></span>

<span data-ttu-id="bee70-102">Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="bee70-102">Get the number of Microsoft Teams unique users by device type over the selected time period.</span></span>

## <a name="permissions"></a><span data-ttu-id="bee70-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="bee70-103">Permissions</span></span>

<span data-ttu-id="bee70-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bee70-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="bee70-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bee70-106">Permission type</span></span>                        | <span data-ttu-id="bee70-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bee70-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="bee70-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bee70-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="bee70-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bee70-109">Not supported.</span></span>                           |
| <span data-ttu-id="bee70-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bee70-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bee70-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bee70-111">Not supported.</span></span>                           |
| <span data-ttu-id="bee70-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bee70-112">Application</span></span>                            | <span data-ttu-id="bee70-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="bee70-113">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="bee70-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bee70-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="bee70-115">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bee70-115">Request parameters</span></span>

<span data-ttu-id="bee70-116">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="bee70-116">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="bee70-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bee70-117">Parameter</span></span> | <span data-ttu-id="bee70-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="bee70-118">Type</span></span>   | <span data-ttu-id="bee70-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="bee70-119">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="bee70-120">period</span><span class="sxs-lookup"><span data-stu-id="bee70-120">period</span></span>    | <span data-ttu-id="bee70-121">cadena</span><span class="sxs-lookup"><span data-stu-id="bee70-121">string</span></span> | <span data-ttu-id="bee70-122">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bee70-122">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="bee70-123">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="bee70-123">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="bee70-124">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bee70-124">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="bee70-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bee70-125">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="bee70-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bee70-126">Request headers</span></span>

| <span data-ttu-id="bee70-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="bee70-127">Name</span></span>          | <span data-ttu-id="bee70-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bee70-128">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="bee70-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="bee70-129">Authorization</span></span> | <span data-ttu-id="bee70-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bee70-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="bee70-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bee70-132">Response</span></span>

<span data-ttu-id="bee70-133">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="bee70-133">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="bee70-134">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bee70-134">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="bee70-135">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="bee70-135">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="bee70-136">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="bee70-136">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="bee70-137">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="bee70-137">Report Refresh Date</span></span>
- <span data-ttu-id="bee70-138">Web</span><span class="sxs-lookup"><span data-stu-id="bee70-138">Web</span></span>
- <span data-ttu-id="bee70-139">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="bee70-139">Windows Phone</span></span>
- <span data-ttu-id="bee70-140">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="bee70-140">Android Phone</span></span>
- <span data-ttu-id="bee70-141">iOS</span><span class="sxs-lookup"><span data-stu-id="bee70-141">iOS</span></span>
- <span data-ttu-id="bee70-142">Mac</span><span class="sxs-lookup"><span data-stu-id="bee70-142">Mac</span></span>
- <span data-ttu-id="bee70-143">Windows</span><span class="sxs-lookup"><span data-stu-id="bee70-143">Windows</span></span>
- <span data-ttu-id="bee70-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="bee70-144">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="bee70-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bee70-145">Example</span></span>

#### <a name="request"></a><span data-ttu-id="bee70-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bee70-146">Request</span></span>

<span data-ttu-id="bee70-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bee70-147">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="bee70-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bee70-148">Response</span></span>

<span data-ttu-id="bee70-149">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bee70-149">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="bee70-150">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="bee70-150">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Period
```
