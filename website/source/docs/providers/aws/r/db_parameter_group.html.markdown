---
layout: "aws"
page_title: "AWS: aws_db_parameter_group"
sidebar_current: "docs-aws-resource-db-parameter-group"
---

# aws\_db\_parameter\_group

Provides an RDS DB parameter group resource.

## Example Usage

```
resource "aws_db_parameter_group" "default" {
    name = "rds_pg"
    family = "mysql5.6"
    description = "RDS default parameter group"

  	parameter {
   	  name = "character_set_server"
   	  value = "utf8"
   	}
   	
   	parameter {
      name = "character_set_client"
      value = "utf8"
    }
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) The name of the DB parameter group.
* `family` - (Required) The family of the DB parameter group.
* `description` - (Required) The description of the DB parameter group.
* `parameter` - (Optional) A list of DB parameters to apply.

Parameter blocks support the following:

* `name` - (Required) The name of the DB parameter.
* `value` - (Required) The value of the DB parameter.

## Attributes Reference

The following attributes are exported:

* `id` - The db parameter group name.
