---
layout: "mso"
page_title: "MSO: mso_schema_site_anp_epg_subnet"
sidebar_current: "docs-mso-data-source-schema_site_anp_epg_subnet"
description: |-
  Data source for MSO Schema Site ANP EPG Subnet.
---

# mso_schema_site_anp_epg_subnet #

Data source for MSO Schema Site ANP EPG Subnet.

## Example Usage ##

```hcl

data "mso_schema_site_anp_epg_subnet" "subnet1" {
  schema_id     = data.mso_schema.schema1.id
  site_id       = data.mso_site.site1.id
  template_name = "Template1"
  anp_name      = "ANP"
  epg_name      = "DB"
  ip            = "10.7.0.1/8"
}

```

## Argument Reference ##

* `schema_id` - (Required) SchemaID under which you want to deploy Subnet.
* `site_id` - (Required) SiteID under which you want to deploy Subnet.
* `template_name` - (Required) Template name under which you want to deploy Subnet.
* `anp_name` - (Required) ANP name under which you want to deploy Subnet.
* `epg_name` - (Required) EPG name under which you want to deploy Subnet.
* `ip` - (Required) The IP of the Subnet.

## Attribute Reference ##

* `scope` - (Optional) The scope of the subnet.
* `shared` - (Optional) Whether this subnet is shared between VRFs.
* `querier` - (Optional) Whether this subnet is an IGMP querier.
* `no_default_gateway` - (Optional) Whether this subnet has a default gateway.
* `description` - (Optional) The description of this subnet. 

