## About the connector
CyberBlindspot is CTM360's Digital Risk Protection platform which combines surface, deep, and dark web monitoring, including brand protection, anti-phishing, and takedowns. This connector allows you to ingest the details from the platform and take response actions.
<p>This document provides information about the CTM360 CyberBlindspot Connector, which facilitates automated interactions, with a CTM360 CyberBlindspot server using FortiSOAR&trade; playbooks. Add the CTM360 CyberBlindspot Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with CTM360 CyberBlindspot.</p>

### Version information

Connector Version: 1.0.0

Publisher: Fortinet SE

Certified: No

## Installing the connector
<p>From FortiSOAR&trade; 6.3.4 onwards, use the <strong>Connector Store</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.<br>You can also use the following <code>yum</code> command as a root user to install connectors from an SSH session:</p>
`yum install cyops-connector-ctm360-cyberblindspot`

## Prerequisites to configuring the connector
- You must have the URL of CTM360 CyberBlindspot server to which you will connect and perform automated operations and credentials to access that server.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the CTM360 CyberBlindspot server.

## Minimum Permissions Required
- N/A

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>CTM360 CyberBlindspot</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations&nbsp;</strong> tab enter the required configuration details:&nbsp;</p>
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Server URL<br></td><td>Specify the Server URL to which you want to connect and perform automated information.<br>
<tr><td>API Key<br></td><td>Specify the API Key to connect to the endpoint and perform automated operations.<br>
<tr><td>Verify SSL<br></td><td>Specifies whether the SSL certificate for the server is to be verified or not. <br/>By default, this option is set as True.<br></td></tr>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 6.3.4 and onwards:
<table border=1><thead><tr><th>Function<br></th><th>Description<br></th><th>Annotation and Category<br></th></tr></thead><tbody><tr><td>Get Incidents<br></td><td>Retrieves a list of incidents from CTM360 Blindspot based on the filter criteria that you have specified.<br></td><td>get_incidents <br/><br></td></tr>
<tr><td>Close Incident<br></td><td>Close a specific incident based on the ticket ID that you have specified.<br></td><td>close_incident <br/><br></td></tr>
<tr><td>Request Takedown<br></td><td>Request takedown on a detected incident in CTM360 Blindspot based on the ticket ID that you have specified.<br></td><td>request_takedown <br/>Investigation<br></td></tr>
<tr><td>Add Comment<br></td><td>Add a comment to a specific incident in CTM360 Blindspot based on the ticket ID and comment parameters that you have specified.<br></td><td>add_comment <br/>Investigation<br></td></tr>
<tr><td>Get Malware Logs<br></td><td>Retrieves a list of malware logs from CTM360 Blindspot based on the filter criteria that you have specified.<br></td><td>get_malware_logs <br/>Investigation<br></td></tr>
<tr><td>Get Breached Credentials<br></td><td>Retrieves a list of breached credentials from CTM360 Blindspot based on the filter criteria that you have specified.<br></td><td>get_breached_credentials <br/>Investigation<br></td></tr>
<tr><td>Get Card Leaks<br></td><td>Retrieves a list of card leaks from CTM360 Blindspot based on the filter criteria that you have specified.<br></td><td>get_card_leaks <br/>Investigation<br></td></tr>
<tr><td>Get Domain Protection<br></td><td>Retrieves a list of domain protection from CTM360 Blindspot based on the filter criteria that you have specified.<br></td><td>get_domain_protection <br/>Investigation<br></td></tr>
</tbody></table>

### operation: Get Incidents
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Date Field<br></td><td>(Optional) Select the data field to retrieve incidents from CTM360 Blindspot. You can choose either Created Date or Updated Date. By default, the field is set to "Created Date".<br>
</td></tr><tr><td>Date From<br></td><td>(Optional) Specify the date and time to retrieve results that include only those items that were created/updated after the specified timestamp.<br>
</td></tr><tr><td>Date To<br></td><td>(Optional) Specify the date and time to retrieve results that include only those items that were created/updated before the specified timestamp.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Close Incident
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Ticket ID<br></td><td>Specify the ticket ID of the incident you want to close.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Request Takedown
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Ticket ID<br></td><td>Specify the ticket ID of the incident you want to take down.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Add Comment
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Ticket Id<br></td><td>Specify the ticket ID of the incident to which you want to add a comment.<br>
</td></tr><tr><td>Comment<br></td><td>Specify the comment you want to add to the incident. Note: Special characters are not allowed.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Malware Logs
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Date From<br></td><td>Specify the date and time to retrieve results that include only those items that were created after the specified timestamp.<br>
</td></tr><tr><td>Date To<br></td><td>Specify the date and time to retrieve results that include only those items that were created before the specified timestamp.<br>
</td></tr><tr><td>Page Size<br></td><td>(Optional) Specify the maximum number of results this operation should return, per page, in the response. By default, it will be fetch 5000 records and maximum 10000 records.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Breached Credentials
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Date From<br></td><td>Specify the date and time to retrieve results that include only those items that were created after the specified timestamp.<br>
</td></tr><tr><td>Date To<br></td><td>Specify the date and time to retrieve results that include only those items that were created before the specified timestamp.<br>
</td></tr><tr><td>Page Size<br></td><td>(Optional) Specify the maximum number of results this operation should return, per page, in the response. By default, it will be fetch 5000 records and maximum 10000 records.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Card Leaks
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Date From<br></td><td>Specify the date and time to retrieve results that include only those items that were created after the specified timestamp.<br>
</td></tr><tr><td>Date To<br></td><td>Specify the date and time to retrieve results that include only those items that were created before the specified timestamp.<br>
</td></tr><tr><td>Page Size<br></td><td>(Optional) Specify the maximum number of results this operation should return, per page, in the response. By default, it will be fetch 5000 records and maximum 10000 records.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
### operation: Get Domain Protection
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Date From<br></td><td>Specify the date and time to retrieve results that include only those items that were created after the specified timestamp.<br>
</td></tr><tr><td>Date To<br></td><td>Specify the date and time to retrieve results that include only those items that were created before the specified timestamp.<br>
</td></tr><tr><td>Incident Type<br></td><td>Specify the incident type to filter the records.<br>
</td></tr><tr><td>Risk Score Min<br></td><td>(Optional) Specify the minium risk score to be used for filtering domain protection.<br>
</td></tr><tr><td>Risk Score Max<br></td><td>(Optional) Specify the maximum risk score to be used for filtering domain protection.<br>
</td></tr><tr><td>Finding Status<br></td><td>(Optional) Specify the finding status to filter the records.<br>
</td></tr><tr><td>Page Size<br></td><td>(Optional) Specify the maximum number of results this operation should return, per page, in the response. By default, it will be fetch 5000 records and maximum 10000 records.<br>
</td></tr></tbody></table>

#### Output

 The output contains a non-dictionary value.
## Included playbooks
The `Sample - CTM360 CyberBlindspot - 1.0.0` playbook collection comes bundled with the CTM360 CyberBlindspot connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR<sup>TM</sup> after importing the CTM360 CyberBlindspot connector.

- Get Incidents
- Close Incident
- Request Takedown
- Add Comment
- Get Malware Logs
- Get Breached Credentials
- Get Card Leaks
- Get Domain Protection

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection, since the sample playbook collection gets deleted during connector upgrade and delete.
