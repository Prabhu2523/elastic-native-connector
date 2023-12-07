# elastic-native-connector

Native connectors are connectors available directly within your Elastic Cloud deployment. No additional infrastructure is required.

Native connectors sync data sources directly to Elasticsearch indices. Create these indices using the Connector workflow within Kibana.

The following connectors are available as native connectors. See each connector reference for additional information specific to each connector.

Azure Blob Storage
Confluence
Dropbox
GitHub
Google Drive
Jira
Microsoft SQL
MongoDB
Network Drive
OneDrive
MySQL
PostgreSQL
ServiceNow
SharePoint Online
Availability and prerequisites
Native connectors were introduced in Elastic version 8.5.0.

Your Elastic cloud deployment must include the following Elastic services:

Elasticsearch
Kibana
Enterprise Search
Refer to Native Integrations on the Elastic subscriptions page, in the Elastic Search section for native connector licensing requirements.

Usage
Follow the Connector workflow in Kibana to select the Connector ingestion method. Choose a data source, create an Elasticsearch index, and configure a native connector to manage the index.

use a connector workflow
Select a connector
Choose the data source to sync from the available options and select Continue.

Create index
Create a new index to be managed by the connector:

Name your index and optionally change the language analyzer to match the human language of your data source. (The index name will be automatically prefixed with search-.)
Select Create index.
The index is created and ready to configure.

This operation requires access to Kibana and the write indices privilege for the .elastic-connectors index.

Configure connector
Create a new index to be managed by the connector.

Continue from above, or navigate to the following location within Kibana:

Search > Content > Elasticsearch indices

Choose the index to configure, and then choose the Configuration tab.

Configure the connector:

Edit the name and description for the connector. Your team can use this information to differentiate this index from other connector indices. (These fields describe the connector and are independent of the Elasticsearch index name.)
Save your changes.
Edit the data source configuration. The fields here vary by connector. Refer to the documentation for each connector for details (see list of native connectors, above). See Security for security considerations.
Save your changes.
Optionally choose Edit sync schedule to begin managing the connector.

This operation requires access to Kibana and the write indices privilege for the .elastic-connectors index.

Manage connector
To manage documents, syncs, sync rules, ingest pipelines, and other connector features, see Using connectors.

These processes are identical for native connectors and connector clients.

End-to-end example
The following example demonstrates how to use a native connector: Native connector tutorial (MongoDB).

Convert a native connector
You can convert a native connector to a self-managed connector client to be run on your own infrastructure. You’ll find instructions in the UI on the connector index’s overview page.

Converting a native connector to a self-managed connector client is an irreversible operation!
