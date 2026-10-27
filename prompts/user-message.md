# User message (per invoice)

This is the exact `Text` (user prompt) on the **Draft Reminder** AI Agent node, with the n8n expression prefix removed. The `{{ ... }}` blocks are n8n expressions evaluated once per invoice row.

```text
Client Name: {{ $json["Client Name"] }}
Company: {{ $json["Company"] }}
Invoice Number: {{ $json["Invoice #"] }}
Amount Overdue: {{ $json["Amount Display"] }}
Days Overdue: {{ $json["Days Past Due"] }} (integer)
Required Tone: {{ $json["Tone"] }}
Due Date: {{ $json["Due Date"] }}
Payment Link: {{ $json["Payment Link"] }}
Today: {{ $now.toFormat("yyyy-MM-dd") }}
```
