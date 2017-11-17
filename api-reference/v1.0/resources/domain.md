<span data-ttu-id="69816-p114">Las relaciones entre un dominio y otros objetos en el directorio, como sus registros de comprobación y registros de configuración de servicio, se exponen a través de las propiedades de navegación. Para leer estas relaciones, puede abordar las propiedades de navegación en las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="69816-p114">Relationships between a domain and other objects in the directory such as its verification records and service configuration records are exposed through navigation properties. You can read these relationships by targeting these navigation properties in your requests.</span></span>

Las relaciones entre un dominio y otros objetos en el directorio, como sus registros de comprobación y registros de configuración de servicio, se exponen a través de las propiedades de navegación. Para leer estas relaciones, puede abordar las propiedades de navegación en las solicitudes.

| <span data-ttu-id="69816-199">Relación</span><span class="sxs-lookup"><span data-stu-id="69816-199">Relationship</span></span> | <span data-ttu-id="69816-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="69816-200">Type</span></span> |<span data-ttu-id="69816-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="69816-201">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="69816-202">domainNameReferences</span><span class="sxs-lookup"><span data-stu-id="69816-202">domainNameReferences</span></span>|<span data-ttu-id="69816-203">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="69816-203">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="69816-204">Solo lectura, admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="69816-204">Read-only, Nullable</span></span>|
|<span data-ttu-id="69816-205">serviceConfigurationRecords</span><span class="sxs-lookup"><span data-stu-id="69816-205">serviceConfigurationRecords</span></span>|<span data-ttu-id="69816-206">Colección [domainDnsRecord](domaindnsrecord.md)</span><span class="sxs-lookup"><span data-stu-id="69816-206">[domainDnsRecord](domaindnsrecord.md) collection</span></span>| <span data-ttu-id="69816-207">Registros DNS que el cliente agrega al archivo de zona de DNS del dominio antes de que Microsoft Online Services pueda usar el dominio.</span><span class="sxs-lookup"><span data-stu-id="69816-207">DNS records the customer adds to the DNS zone file of the domain before the domain can be used by Microsoft Online services.</span></span><br><span data-ttu-id="69816-208">Solo lectura, admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="69816-208">Read-only, Nullable</span></span> |
|<span data-ttu-id="69816-209">verificationDnsRecords</span><span class="sxs-lookup"><span data-stu-id="69816-209">verificationDnsRecords</span></span>|<span data-ttu-id="69816-210">Colección [domainDnsRecord](domaindnsrecord.md)</span><span class="sxs-lookup"><span data-stu-id="69816-210">[domainDnsRecord](domaindnsrecord.md) collection</span></span>| <span data-ttu-id="69816-211">Registros DNS que el cliente agrega al archivo de zona de DNS del dominio antes de que el cliente pueda completar la comprobación de propiedad de dominio con Azure AD.</span><span class="sxs-lookup"><span data-stu-id="69816-211">DNS records that the customer adds to the DNS zone file of the domain before the customer can complete domain ownership verification with Azure AD.</span></span><br><span data-ttu-id="69816-212">Solo lectura, admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="69816-212">Read-only, Nullable</span></span>|

## <span data-ttu-id="69816-213">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="69816-213">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="69816-214">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="69816-214">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domain"
}-->

```json
{
  "authenticationType": "String",
  "availabilityStatus": "String",
  "id": "String (identifier)",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true,
  "isVerified": true,
  "state": {"@odata.type": "microsoft.graph.domainState"},
  "supportedServices": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->