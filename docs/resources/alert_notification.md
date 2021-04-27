---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "grafana_alert_notification Resource - terraform-provider-grafana"
subcategory: ""
description: |-
  Official documentation https://grafana.com/docs/grafana/latest/alerting/notifications/HTTP API https://grafana.com/docs/grafana/latest/http_api/alerting_notification_channels/
---

# grafana_alert_notification (Resource)

* [Official documentation](https://grafana.com/docs/grafana/latest/alerting/notifications/)
* [HTTP API](https://grafana.com/docs/grafana/latest/http_api/alerting_notification_channels/)

## Example Usage

```terraform
resource "grafana_alert_notification" "email_someteam" {
  name          = "Email that team"
  type          = "email"
  is_default    = false
  send_reminder = true
  frequency     = "24h"

  settings = {
    addresses   = "foo@example.net;bar@example.net"
    uploadImage = "false"
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) The name of the alert notification channel.
- **type** (String) The type of the alert notification channel.

### Optional

- **disable_resolve_message** (Boolean) Whether to disable sending resolve messages. Defaults to `false`.
- **frequency** (String) Frequency of alert reminders. Frequency must be set if reminders are enabled. Defaults to ``.
- **id** (String) The ID of this resource.
- **is_default** (Boolean) Is this the default channel for all your alerts. Defaults to `false`.
- **send_reminder** (Boolean) Whether to send reminders for triggered alerts. Defaults to `false`.
- **settings** (Map of String, Sensitive) Additional settings, for full reference see [Grafana HTTP API documentation](https://grafana.com/docs/grafana/latest/http_api/alerting_notification_channels/).
- **uid** (String) Unique identifier. If unset, this will be automatically generated.

