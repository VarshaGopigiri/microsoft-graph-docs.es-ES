<span data-ttu-id="8be9c-p103">El objeto al que se puede asignar el plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="8be9c-p103">The object the service plan can be assigned to. Possible values:</span></span>|El objeto al que se puede asignar el plan de servicio. Valores posibles:<br/><span data-ttu-id="8be9c-127">“User”: el plan de servicio se puede asignar a usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="8be9c-127">"User" - service plan can be assigned to individual users.</span></span><br/><span data-ttu-id="8be9c-128">“Company”: el plan de servicio se puede asignar a todo el inquilino.</span><span class="sxs-lookup"><span data-stu-id="8be9c-128">"Company" - service plan can be assigned to the entire tenant.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="8be9c-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8be9c-129">JSON representation</span></span>

<span data-ttu-id="8be9c-130">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8be9c-130">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.servicePlanInfo"
}-->

```json
{
  "appliesTo": "string",
  "provisioningStatus": "string",
  "servicePlanId": "guid",
  "servicePlanName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePlanInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
