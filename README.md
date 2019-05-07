# ![LOGO](logo.png) Engagement.ManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the Engagement.ManagementClient API (version 2014-12-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/mobileengagement-mobile-engagement/2014-12-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:24+03:00

## API Description

Microsoft Azure Mobile Engagement REST APIs.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists app collections in a subscription.

*Tags:* `AppCollections` `List`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `api-version` - _required_ - Client Api Version.

### Checks availability of an app collection name in the Engagement domain.

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `api-version` - _required_ - Client Api Version.

### Lists supported platforms for Engagement applications.

*Tags:* `List`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `api-version` - _required_ - Client Api Version.

### Lists apps in an appCollection.

*Tags:* `Apps` `List`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `api-version` - _required_ - Client Api Version.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.

### Get the list of campaigns.

*Tags:* `Campaign` `List`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `$skip` - _optional_ - Control paging of campaigns, start results at the given offset, defaults to 0 (1st page of data).
* `$top` - _optional_ - Control paging of campaigns, number of campaigns to return with each call. It returns all campaigns by default. When specifying $top parameter, the response contains a `nextLink` property describing the path to get the next page if there are more results.
* `$filter` - _optional_ - Filter can be used to restrict the results to campaigns matching a specific state. The syntax is `$filter=state eq 'draft'`. Valid state values are: draft, scheduled, in-progress, and finished. Only the eq operator and the state property are supported.
* `$orderby` - _optional_ - Sort results by an expression which looks like `$orderby=id asc` (this example is actually the default behavior). The syntax is orderby={property} {direction} or just orderby={property}. The available sorting properties are id, name, state, activatedDate, and finishedDate. The available directions are asc (for ascending order) and desc (for descending order). When not specified the asc direction is used. Only one property at a time can be used for sorting.
* `$search` - _optional_ - Restrict results to campaigns matching the optional `search` expression. This currently performs the search based on the name on the campaign only, case insensitive. If the campaign contains the value of the `search` parameter anywhere in the name, it matches.

### Create a push campaign (announcement, poll, data push or native push).

*Tags:* `Campaign` `CRUD`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `api-version` - _required_ - Client Api Version.

### Test a new campaign on a set of devices.

*Tags:* `Campaign` `Test`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.

### Delete a campaign previously created by a call to Create campaign.

*Tags:* `Campaign` `CRUD`

#### Input Parameters
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### The Get campaign operation retrieves information about a previously created campaign.

*Tags:* `Campaign` `CRUD`

#### Input Parameters
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Update an existing push campaign (announcement, poll, data push or native push).

*Tags:* `Campaign` `CRUD`

#### Input Parameters
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Activate a campaign previously created by a call to Create campaign.

*Tags:* `Campaign` `Action`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `api-version` - _required_ - Client Api Version.

### Finish a push campaign previously activated by a call to Activate campaign.

*Tags:* `Campaign` `Action`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `api-version` - _required_ - Client Api Version.

### Push a previously saved campaign (created with Create campaign) to a set of devices.

*Tags:* `Campaign` `Action`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.

### Get all the campaign statistics.

*Tags:* `Campaign`

#### Input Parameters
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Suspend a push campaign previously activated by a call to Activate campaign.

*Tags:* `Campaign` `Action`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `api-version` - _required_ - Client Api Version.

### Test an existing campaign (created with Create campaign) on a set of devices.

*Tags:* `Campaign` `Test`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `id` - _required_ - Campaign identifier.
* `api-version` - _required_ - Client Api Version.

### The Get campaign operation retrieves information about a previously created campaign.

*Tags:* `Campaign` `CRUD`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `kind` - _required_ - Campaign kind.
    Possible values: announcements, polls, dataPushes, nativePushes.
* `name` - _required_ - Campaign name.
* `api-version` - _required_ - Client Api Version.

### Query the information associated to the devices running an application.

*Tags:* `Device`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `$top` - _optional_ - Number of devices to return with each call. Defaults to 100 and cannot return more. Passing a greater value is ignored. The response contains a `nextLink` property describing the URI path to get the next page of results if not all results could be returned at once.
* `$select` - _optional_ - By default all `meta` and `appInfo` properties are returned, this property is used to restrict the output to the desired properties. It also excludes all devices from the output that have none of the selected properties. In other terms, only devices having at least one of the selected property being set is part of the results. Examples: - `$select=appInfo` : select all devices having at least 1 appInfo, return them all and don't return any meta property. - `$select=meta` : return only meta properties in the output. - `$select=appInfo,meta/firstSeen,meta/lastSeen` : return all `appInfo`, plus meta object containing only firstSeen and lastSeen properties. The format is thus a comma separated list of properties to select. Use `appInfo` to select all appInfo properties, `meta` to select all meta properties. Use `appInfo/{key}` and `meta/{key}` to select specific appInfo and meta properties.
* `$filter` - _optional_ - Filter can be used to reduce the number of results. Filter is a boolean expression that can look like the following examples: * `$filter=deviceId gt 'abcdef0123456789abcdef0123456789'` * `$filter=lastModified le 1447284263690L` * `$filter=(deviceId ge 'abcdef0123456789abcdef0123456789') and (deviceId lt 'bacdef0123456789abcdef0123456789') and (lastModified gt 1447284263690L)` The first example is used automatically for paging when returning the `nextLink` property. The filter expression is a combination of checks on some properties that can be compared to their value. The available operators are: * `gt`  : greater than * `ge`  : greater than or equals * `lt`  : less than * `le`  : less than or equals * `and` : to add multiple checks (all checks must pass), optional parentheses can be used. The properties that can be used in the expression are the following: * `deviceId {operator} '{deviceIdValue}'` : a lexicographical comparison is made on the deviceId value, use single quotes for the value. * `lastModified {operator} {number}L` : returns only meta properties or appInfo properties whose last value modification timestamp compared to the specified value is matching (value is milliseconds since January 1st, 1970 UTC). Please note the `L` character after the number of milliseconds, its required when the number of milliseconds exceeds `2^31 - 1` (which is always the case for recent timestamps). Using `lastModified` excludes all devices from the output that have no property matching the timestamp criteria, like `$select`. Please note that the internal value of `lastModified` timestamp for a given property is never part of the results.

### Get the list of export tasks.

*Tags:* `export` `list`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `$skip` - _optional_ - Control paging of export tasks, start results at the given offset, defaults to 0 (1st page of data).
* `$top` - _optional_ - Control paging of export tasks, number of export tasks to return with each call. By default, it returns all export tasks with a default paging of 20.
The response contains a `nextLink` property describing the path to get the next page if there are more results.
The maximum paging limit for $top is 40.
* `$orderby` - _optional_ - Sort results by an expression which looks like `$orderby=taskId asc` (default when not specified).
The syntax is orderby={property} {direction} or just orderby={property}.
Properties that can be specified for sorting: taskId, errorDetails, dateCreated, taskStatus, and dateCreated.
The available directions are asc (for ascending order) and desc (for descending order).
When not specified the asc direction is used.
Only one orderby property can be specified.

### Creates a task to export activities.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export crashes.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export errors.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export events.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export push campaign data for a set of campaigns.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export push campaign data for a date range.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export jobs.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export sessions.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export tags.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Creates a task to export tags.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Retrieves information about a previously created export task.

*Tags:* `export` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `id` - _required_ - Export task identifier.

### Get the list of import jobs.

*Tags:* `import` `list`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `$skip` - _optional_ - Control paging of import jobs, start results at the given offset, defaults to 0 (1st page of data).
* `$top` - _optional_ - Control paging of import jobs, number of import jobs to return with each call. By default, it returns all import jobs with a default paging of 20.
The response contains a `nextLink` property describing the path to get the next page if there are more results.
The maximum paging limit for $top is 40.
* `$orderby` - _optional_ - Sort results by an expression which looks like `$orderby=jobId asc` (default when not specified).
The syntax is orderby={property} {direction} or just orderby={property}.
Properties that can be specified for sorting: jobId, errorDetails, dateCreated, jobStatus, and dateCreated.
The available directions are asc (for ascending order) and desc (for descending order).
When not specified the asc direction is used.
Only one orderby property can be specified.

### Creates a job to import the specified data to a storageUrl.

*Tags:* `import` `crud`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### The Get import job operation retrieves information about a previously created import job.

*Tags:* `import` `crud`

#### Input Parameters
* `id` - _required_ - Import job identifier.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Update the tags registered for a set of devices running an application. Updates are performed asynchronously, meaning that a few seconds are needed before the modifications appear in the results of the Get device command.

*Tags:* `Device`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Get the information associated to a device running an application.

*Tags:* `Device`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `deviceId` - _required_ - Device identifier.

### Update the tags registered for a set of users running an application. Updates are performed asynchronously, meaning that a few seconds are needed before the modifications appear in the results of the Get device command.

*Tags:* `Device`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.

### Get the information associated to a device running an application using the user identifier.

*Tags:* `Device`

#### Input Parameters
* `subscriptionId` - _required_ - Gets subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.
* `resourceGroupName` - _required_ - The name of the resource group.
* `appCollection` - _required_ - Application collection.
* `appName` - _required_ - Application resource name.
* `api-version` - _required_ - Client Api Version.
* `userId` - _required_ - User identifier.

## License

**flow**ground :- Telekom iPaaS / azure-com-mobileengagement-mobile-engagement-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
