<div align="center">

[![Visit EyeLevel's GroundX APIs](./header.png)](https://www.eyelevel.ai)

# [EyeLevel's GroundX APIs](https://www.eyelevel.ai)<a id="eyelevels-groundx-apis"></a>

RAG Made Simple, Secure and Hallucination Free

[![npm](https://img.shields.io/badge/npm-v1.3.28-blue)](https://www.npmjs.com/package/groundx-typescript-sdk/v/1.3.28)
[![More Info](https://img.shields.io/badge/More%20Info-Click%20Here-orange)](https://www.eyelevel.ai/)

</div>

## Table of Contents<a id="table-of-contents"></a>

<!-- toc -->

- [Installation](#installation)
- [Getting Started](#getting-started)
- [Reference](#reference)
  * [`groundx.buckets.create`](#groundxbucketscreate)
  * [`groundx.buckets.delete`](#groundxbucketsdelete)
  * [`groundx.buckets.get`](#groundxbucketsget)
  * [`groundx.buckets.list`](#groundxbucketslist)
  * [`groundx.buckets.update`](#groundxbucketsupdate)
  * [`groundx.customer.get`](#groundxcustomerget)
  * [`groundx.documents.crawlWebsite`](#groundxdocumentscrawlwebsite)
  * [`groundx.documents.delete`](#groundxdocumentsdelete)
  * [`groundx.documents.delete1`](#groundxdocumentsdelete1)
  * [`groundx.documents.get`](#groundxdocumentsget)
  * [`groundx.documents.getProcessingStatusById`](#groundxdocumentsgetprocessingstatusbyid)
  * [`groundx.documents.ingestLocal`](#groundxdocumentsingestlocal)
  * [`groundx.documents.ingestRemote`](#groundxdocumentsingestremote)
  * [`groundx.documents.list`](#groundxdocumentslist)
  * [`groundx.documents.lookup`](#groundxdocumentslookup)
  * [`groundx.health.get`](#groundxhealthget)
  * [`groundx.health.list`](#groundxhealthlist)
  * [`groundx.projects.addBucket`](#groundxprojectsaddbucket)
  * [`groundx.projects.create`](#groundxprojectscreate)
  * [`groundx.projects.delete`](#groundxprojectsdelete)
  * [`groundx.projects.get`](#groundxprojectsget)
  * [`groundx.projects.list`](#groundxprojectslist)
  * [`groundx.projects.removeBucket`](#groundxprojectsremovebucket)
  * [`groundx.projects.update`](#groundxprojectsupdate)
  * [`groundx.search.content`](#groundxsearchcontent)

<!-- tocstop -->

## Installation<a id="installation"></a>

<table>
<tr>
<th width="292px"><code>npm</code></th>
<th width="293px"><code>pnpm</code></th>
<th width="292px"><code>yarn</code></th>
</tr>
<tr>
<td>

```bash
npm i groundx-typescript-sdk
```

</td>
<td>

```bash
pnpm i groundx-typescript-sdk
```

</td>
<td>

```bash
yarn add groundx-typescript-sdk
```

</td>
</tr>
</table>

## Getting Started<a id="getting-started"></a>

```typescript
import { Groundx } from "groundx-typescript-sdk";

const groundx = new Groundx({
  // Defining the base path is optional and defaults to https://api.groundx.ai/api
  // basePath: "https://api.groundx.ai/api",
  apiKey: "API_KEY",
});

const createResponse = await groundx.buckets.create({
  name: "your_bucket_name",
});

console.log(createResponse);
```

## Reference<a id="reference"></a>


### `groundx.buckets.create`<a id="groundxbucketscreate"></a>

Create a new bucket.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const createResponse = await groundx.buckets.create({
  name: "your_bucket_name",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### name: `string`<a id="name-string"></a>

#### 🔄 Return<a id="🔄-return"></a>

[BucketResponse](./models/bucket-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/bucket` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.buckets.delete`<a id="groundxbucketsdelete"></a>

Delete a bucket.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const deleteResponse = await groundx.buckets.delete({
  bucketId: 1,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### bucketId: `number`<a id="bucketid-number"></a>

The bucketId of the bucket being deleted.

#### 🔄 Return<a id="🔄-return"></a>

[MessageResponse](./models/message-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/bucket/{bucketId}` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.buckets.get`<a id="groundxbucketsget"></a>

Look up a specific bucket by its bucketId.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const getResponse = await groundx.buckets.get({
  bucketId: 1,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### bucketId: `number`<a id="bucketid-number"></a>

The bucketId of the bucket to look up.

#### 🔄 Return<a id="🔄-return"></a>

[BucketResponse](./models/bucket-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/bucket/{bucketId}` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.buckets.list`<a id="groundxbucketslist"></a>

List all buckets within your GroundX account

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listResponse = await groundx.buckets.list({});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### n: `number`<a id="n-number"></a>

The maximum number of returned documents. Accepts 1-100 with a default of 20.

##### nextToken: `string`<a id="nexttoken-string"></a>

A token for pagination. If the number of documents for a given query is larger than n, the response will include a \"nextToken\" value. That token can be included in this field to retrieve the next batch of n documents.

#### 🔄 Return<a id="🔄-return"></a>

[BucketListResponse](./models/bucket-list-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/bucket` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.buckets.update`<a id="groundxbucketsupdate"></a>

Rename a bucket.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const updateResponse = await groundx.buckets.update({
  bucketId: 1,
  newName: "your_bucket_name",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### newName: `string`<a id="newname-string"></a>

The new name of the bucket being renamed.

##### bucketId: `number`<a id="bucketid-number"></a>

The bucketId of the bucket being updated.

#### 🔄 Return<a id="🔄-return"></a>

[BucketUpdateResponse](./models/bucket-update-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/bucket/{bucketId}` `PUT`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.customer.get`<a id="groundxcustomerget"></a>

Get the account information associated with the API key.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const getResponse = await groundx.customer.get();
```

#### 🔄 Return<a id="🔄-return"></a>

[CustomerResponse](./models/customer-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/customer` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.crawlWebsite`<a id="groundxdocumentscrawlwebsite"></a>

Upload the content of a publicly accessible website for ingestion into a GroundX bucket. This is done by following links within a specified URL, recursively, up to a specified depth or number of pages.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const crawlWebsiteResponse = await groundx.documents.crawlWebsite({
  websites: [
    {
      bucketId: 123,
      cap: 100,
      depth: 3,
      sourceUrl: "https://my.website.com",
    },
  ],
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### websites: [`WebsiteCrawlRequestWebsitesInner`](./models/website-crawl-request-websites-inner.ts)[]<a id="websites-websitecrawlrequestwebsitesinnermodelswebsite-crawl-request-websites-innerts"></a>

#### 🔄 Return<a id="🔄-return"></a>

[IngestResponse](./models/ingest-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/documents/website` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.delete`<a id="groundxdocumentsdelete"></a>

Delete multiple documents hosted on GroundX

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const deleteResponse = await groundx.documents.delete({
  documentIds: ["documentIds_example"],
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### documentIds: `string`[]<a id="documentids-string"></a>

A list of documentIds which correspond to documents ingested by GroundX

#### 🔄 Return<a id="🔄-return"></a>

[IngestResponse](./models/ingest-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/documents` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.delete1`<a id="groundxdocumentsdelete1"></a>

Delete a single document hosted on GroundX

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const delete1Response = await groundx.documents.delete1({
  documentId: "documentId_example",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### documentId: `string`<a id="documentid-string"></a>

A documentId which correspond to a document ingested by GroundX

#### 🔄 Return<a id="🔄-return"></a>

[IngestResponse](./models/ingest-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/document/{documentId}` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.get`<a id="groundxdocumentsget"></a>

Look up an existing document by documentId.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const getResponse = await groundx.documents.get({
  documentId: "documentId_example",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### documentId: `string`<a id="documentid-string"></a>

The documentId of the document for which GroundX information will be provided.

#### 🔄 Return<a id="🔄-return"></a>

[DocumentResponse](./models/document-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/document/{documentId}` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.getProcessingStatusById`<a id="groundxdocumentsgetprocessingstatusbyid"></a>

Get the current status of an ingest, initiated with documents.ingest_remote, documents.ingest_local, or documents.crawl_website, by specifying the processId (the processId is included in the response of the documents.ingest functions).

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const getProcessingStatusByIdResponse =
  await groundx.documents.getProcessingStatusById({
    processId: "processId_example",
  });
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### processId: `string`<a id="processid-string"></a>

the processId for the ingest process being checked

#### 🔄 Return<a id="🔄-return"></a>

[ProcessStatusResponse](./models/process-status-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/{processId}` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.ingestLocal`<a id="groundxdocumentsingestlocal"></a>

Upload documents hosted on a local file system for ingestion into a GroundX bucket.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const ingestLocalResponse = await groundx.documents.ingestLocal([
  {
    blob: fs.readFileSync("/path/to/file"),
    metadata: {
      bucketId: 1234,
      fileName: "my_file.txt",
      fileType: "txt",
    },
  },
]);
```

#### ⚙️ Request Body<a id="⚙️-request-body"></a>

[`DocumentLocalIngestRequestInner`](./models/document-local-ingest-request-inner.ts)[]

#### 🔄 Return<a id="🔄-return"></a>

[IngestResponse](./models/ingest-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/documents/local` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.ingestRemote`<a id="groundxdocumentsingestremote"></a>

Ingest documents hosted on public URLs to a GroundX bucket. 

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const ingestRemoteResponse = await groundx.documents.ingestRemote({
  documents: [
    {
      bucketId: 1234,
      fileName: "my_file.txt",
      fileType: "txt",
      sourceUrl: "https://my.source.url.com/file.txt",
    },
  ],
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### documents: [`DocumentRemoteIngestRequestDocumentsInner`](./models/document-remote-ingest-request-documents-inner.ts)[]<a id="documents-documentremoteingestrequestdocumentsinnermodelsdocument-remote-ingest-request-documents-innerts"></a>

#### 🔄 Return<a id="🔄-return"></a>

[IngestResponse](./models/ingest-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/documents/remote` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.list`<a id="groundxdocumentslist"></a>

lookup all documents across all resources which are currently on GroundX

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listResponse = await groundx.documents.list({
  sort: "name",
  sortOrder: "asc",
  status: "queued",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### n: `number`<a id="n-number"></a>

The maximum number of returned documents. Accepts 1-100 with a default of 20.

##### filter: `string`<a id="filter-string"></a>

Only documents with names that contain the filter string will be returned in the results.

##### sort: [`Sort`](./models/sort.ts)<a id="sort-sortmodelssortts"></a>

The document attribute that will be used to sort the results.

##### sortOrder: [`SortOrder`](./models/sort-order.ts)<a id="sortorder-sortordermodelssort-orderts"></a>

The order in which to sort the results. A value for sort must also be set.

##### status: [`ProcessingStatus`](./models/processing-status.ts)<a id="status-processingstatusmodelsprocessing-statusts"></a>

A status filter on the get documents query. If this value is set, then only documents with this status will be returned in the results.

##### nextToken: `string`<a id="nexttoken-string"></a>

A token for pagination. If the number of documents for a given query is larger than n, the response will include a \"nextToken\" value. That token can be included in this field to retrieve the next batch of n documents.

#### 🔄 Return<a id="🔄-return"></a>

[DocumentListResponse](./models/document-list-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/documents` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.documents.lookup`<a id="groundxdocumentslookup"></a>

lookup the document(s) associated with a processId, bucketId, or projectId.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const lookupResponse = await groundx.documents.lookup({
  id: 1,
  sort: "name",
  sortOrder: "asc",
  status: "queued",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### id: `number`<a id="id-number"></a>

a processId, bucketId, or projectId

##### n: `number`<a id="n-number"></a>

The maximum number of returned documents. Accepts 1-100 with a default of 20.

##### filter: `string`<a id="filter-string"></a>

Only documents with names that contain the filter string will be returned in the results.

##### sort: [`Sort`](./models/sort.ts)<a id="sort-sortmodelssortts"></a>

The document attribute that will be used to sort the results.

##### sortOrder: [`SortOrder`](./models/sort-order.ts)<a id="sortorder-sortordermodelssort-orderts"></a>

The order in which to sort the results. A value for sort must also be set.

##### status: [`ProcessingStatus`](./models/processing-status.ts)<a id="status-processingstatusmodelsprocessing-statusts"></a>

A status filter on the get documents query. If this value is set, then only documents with this status will be returned in the results.

##### nextToken: `string`<a id="nexttoken-string"></a>

A token for pagination. If the number of documents for a given query is larger than n, the response will include a \"nextToken\" value. That token can be included in this field to retrieve the next batch of n documents.

#### 🔄 Return<a id="🔄-return"></a>

[DocumentLookupResponse](./models/document-lookup-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/ingest/documents/{id}` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.health.get`<a id="groundxhealthget"></a>

Look up the current health status of a specific service. Statuses update every 5 minutes.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const getResponse = await groundx.health.get({
  service: "service_example",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### service: `string`<a id="service-string"></a>

The name of the service to look up.

#### 🔄 Return<a id="🔄-return"></a>

[HealthResponse](./models/health-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/health/{service}` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.health.list`<a id="groundxhealthlist"></a>

List the current health status of all services. Statuses update every 5 minutes.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listResponse = await groundx.health.list();
```

#### 🔄 Return<a id="🔄-return"></a>

[HealthResponse](./models/health-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/health` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.addBucket`<a id="groundxprojectsaddbucket"></a>

Add an existing bucket to an existing project. Buckets and projects can be associated many to many.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const addBucketResponse = await groundx.projects.addBucket({
  projectId: 1,
  bucketId: 1,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### projectId: `number`<a id="projectid-number"></a>

The projectId of the project which the bucket will be added to.

##### bucketId: `number`<a id="bucketid-number"></a>

The bucketId of the bucket being added to the project.

#### 🔄 Return<a id="🔄-return"></a>

[MessageResponse](./models/message-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project/{projectId}/bucket/{bucketId}` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.create`<a id="groundxprojectscreate"></a>

create a new project, a project being a collection of buckets which can be searched.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const createResponse = await groundx.projects.create({
  name: "your_project_name",
  bucketName: "your_new_bucket_name",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### name: `string`<a id="name-string"></a>

The name of the project being created.

##### bucketName: `string`<a id="bucketname-string"></a>

Specify bucketName to automatically create a bucket, by the name specified, and add it to the created project.

#### 🔄 Return<a id="🔄-return"></a>

[ProjectResponse](./models/project-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.delete`<a id="groundxprojectsdelete"></a>

Delete a project.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const deleteResponse = await groundx.projects.delete({
  projectId: 1,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### projectId: `number`<a id="projectid-number"></a>

The projectId of the project to be deleted.

#### 🔄 Return<a id="🔄-return"></a>

[MessageResponse](./models/message-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project/{projectId}` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.get`<a id="groundxprojectsget"></a>

look up a specific project by its projectId.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const getResponse = await groundx.projects.get({
  projectId: 1,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### projectId: `number`<a id="projectid-number"></a>

The projectId of the project to look up.

#### 🔄 Return<a id="🔄-return"></a>

[ProjectResponse](./models/project-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project/{projectId}` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.list`<a id="groundxprojectslist"></a>

list all projects within your GroundX account.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const listResponse = await groundx.projects.list({});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### n: `number`<a id="n-number"></a>

The maximum number of returned documents. Accepts 1-100 with a default of 20.

##### nextToken: `string`<a id="nexttoken-string"></a>

A token for pagination. If the number of documents for a given query is larger than n, the response will include a \"nextToken\" value. That token can be included in this field to retrieve the next batch of n documents.

#### 🔄 Return<a id="🔄-return"></a>

[ProjectListResponse](./models/project-list-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project` `GET`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.removeBucket`<a id="groundxprojectsremovebucket"></a>

remove a bucket from a project. Buckets and projects can be associated many to many, this removes one bucket to project association without disturbing others.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const removeBucketResponse = await groundx.projects.removeBucket({
  projectId: 1,
  bucketId: 1,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### projectId: `number`<a id="projectid-number"></a>

The projectId of the project which the bucket will be removed from.

##### bucketId: `number`<a id="bucketid-number"></a>

The bucketId of the bucket which will be removed from the project.

#### 🔄 Return<a id="🔄-return"></a>

[MessageResponse](./models/message-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project/{projectId}/bucket/{bucketId}` `DELETE`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.projects.update`<a id="groundxprojectsupdate"></a>

Rename a project

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const updateResponse = await groundx.projects.update({
  projectId: 1,
  newName: "your_project_name",
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### newName: `string`<a id="newname-string"></a>

The new name of the project being renamed.

##### projectId: `number`<a id="projectid-number"></a>

The projectId of the project to update.

#### 🔄 Return<a id="🔄-return"></a>

[ProjectResponse](./models/project-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/project/{projectId}` `PUT`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


### `groundx.search.content`<a id="groundxsearchcontent"></a>

Search documents on GroundX for the most relevant information to a given query.

The result of this query is typically used in one of two ways; result['search']['text'] can be used to provide context to a language model, facilitating RAG, or result['search']['results'] can be used to observe chunks of text which are relevant to the query, facilitating citation.

Interact with the "Request Body" below to explore the arguments of this function. Enter your GroundX API key to send a request directly from this web page. Select your language of choice to structure a code snippet based on your specified arguments.


#### 🛠️ Usage<a id="🛠️-usage"></a>

```typescript
const contentResponse = await groundx.search.content({
  id: null,
  n: 20,
  nextToken: "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9",
  query: "my search query",
  relevance: 10,
});
```

#### ⚙️ Parameters<a id="⚙️-parameters"></a>

##### query: `string`<a id="query-string"></a>

The search query to be used to find relevant documentation.

##### id: [`SearchContentIdParameter`](./models/search-content-id-parameter.ts)<a id="id-searchcontentidparametermodelssearch-content-id-parameterts"></a>

The bucketId, projectId, or documentId to be searched. The document or documents within the specified container will be compared to the query, and relevant information will be extracted.

##### relevance: `number`<a id="relevance-number"></a>

The minimum search relevance score required to include the result. By default, this is 10.0.

##### n: `number`<a id="n-number"></a>

The maximum number of returned documents. Accepts 1-100 with a default of 20.

##### nextToken: `string`<a id="nexttoken-string"></a>

A token for pagination. If the number of search results for a given query is larger than n, the response will include a \"nextToken\" value. That token can be included in this field to retrieve the next batch of n search results.

##### verbosity: `number`<a id="verbosity-number"></a>

The amount of data returned with each search result. 0 == no search results, only the recommended context. 1 == search results but no searchData. 2 == search results and searchData.

#### 🔄 Return<a id="🔄-return"></a>

[SearchResponse](./models/search-response.ts)

#### 🌐 Endpoint<a id="🌐-endpoint"></a>

`/v1/search/{id}` `POST`

[🔙 **Back to Table of Contents**](#table-of-contents)

---


## Author<a id="author"></a>
This TypeScript package is automatically generated by [Konfig](https://konfigthis.com)
