## Website JSON API

---

API Route: https://mohistmc.com/api/ 

* Note on behavior: The API will return `404` if a route doesn't exist.

### Getting available versions

```
GET https://mohistmc.com/api/versions

-> Returns a JSON array of strings.
```

Get the list of available Mohist versions.

<details>
  <summary style="font-weight: bold">Example request response</summary>

```json
[
  "1.7.10",
  "1.12.2",
  "1.16.5",
  "1.18.2-testing"
]
```
</details>

### Get all builds

```
GET https://mohistmc.com/api/<mcversion>/

-> Returns a JSON array of objects that contains each builds information.
```

* `mcversion`: The version of Mohist to get the builds for. Can be parsed using the _"Getting available versions"_ route.

Get the list of available builds for a specific Mohist version.

> There are additional params that can be used to filter the results.

Getting all `SUCCESS` builds:

```
GET https://mohistmc.com/api/<mcversion>?status=SUCCESS

-> Returns a JSON array of objects that contains each success builds information.
```

Getting all `FAILED` builds:

```
GET https://mohistmc.com/api/<mcversion>?status=FAILED

-> Returns a JSON array of objects that contains each failed builds information.
```

### Get particular build

> Note: Getting a non-existing build will return 404 error with "Build not found" `string` body.
```
GET https://mohistmc.com/api/<mcversion>/<buildnumber>/

-> Returns a JSON object that contains build information.
```

* `mcversion`: The version of Mohist to get the builds for. Can be parsed using the _"Getting available versions"_ route.
* `buildnumber`: The build number of the build to get. 

Get the information of a specific build for a specific Mohist version.

<details>
  <summary style="font-weight: bold">Example SUCCESS BUILD request response</summary>

```json
{
  "status": "SUCCESS",
  "number": 321,
  "version": "1.12.2",
  "name": "mohist-1.12.2-321-server.jar",
  "forge_version": "14.23.5.2860",
  "tinysha": "9b11c26d",
  "fullsha": "9b11c26db06dfeada98c589258abd5e9065177c0",
  "md5": "9b958889abb4d305df4dced5dffb0752",
  "url": "https://mohistmc.com/builds/1.12.2/mohist-1.12.2-321-server.jar",
  "mirror": "https://ci.codemc.io/job/MohistMC/job/Mohist-1.12.2/321/artifact/projects/mohist/build/libs/mohist-1.12.2-321-server.jar",
  "timeinmillis": 1650670613917,
  "date": "4/22/2022 11:36:53 PM",
  "decomposeddate": {
    "day": 22,
    "month": 3,
    "year": 2022,
    "hours": 23,
    "minutes": 36,
    "seconds": 53
  }
}
```
</details>

<details>
  <summary style="font-weight: bold">Example FAILED BUILD request response</summary>

```json
{
  "status": "FAILED",
  "number": 25
}
```
</details>

### Get the latest build

> Note: It will **always** return a SUCCESS build.

```
GET https://mohistmc.com/api/<mcversion>/latest/

-> Returns a JSON object that contains build information.
```

* `mcversion`: The version of Mohist to get the builds for. Can be parsed using the _"Getting available versions"_ route.

Get the information of the latest build of a specific Mohist version.

<details>
  <summary style="font-weight: bold">Example usage</summary>

```
GET https://mohistmc.com/api/1.12.2/latest
```

```json
{
  "status": "SUCCESS",
  "number": 321,
  "version": "1.12.2",
  "name": "mohist-1.12.2-321-server.jar",
  "forge_version": "14.23.5.2860",
  "tinysha": "9b11c26d",
  "fullsha": "9b11c26db06dfeada98c589258abd5e9065177c0",
  "md5": "9b958889abb4d305df4dced5dffb0752",
  "url": "https://mohistmc.com/builds/1.12.2/mohist-1.12.2-321-server.jar",
  "mirror": "https://ci.codemc.io/job/MohistMC/job/Mohist-1.12.2/321/artifact/projects/mohist/build/libs/mohist-1.12.2-321-server.jar",
  "timeinmillis": 1650670613917,
  "date": "4/22/2022 11:36:53 PM",
  "decomposeddate": {
    "day": 22,
    "month": 3,
    "year": 2022,
    "hours": 23,
    "minutes": 36,
    "seconds": 53
  }
}
```
</details>

### Downloading a build from API

```
GET https://mohistmc.com/api/<mcversion>/<buildnumber>/download

-> Returns the build jar file.
```

* `mcversion`: The version of Mohist to get the builds for. Can be parsed using the _"Getting available versions"_ route.
* `buildnumber`: The build number of the build to get.

<details>
  <summary style="font-weight: bold">Example request</summary>

```
GET https://mohistmc.com/api/1.12.2/300/download
```
</details>

### Downloading the latest build from API

```
GET https://mohistmc.com/api/<mcversion>/latest/download

-> Returns the build jar file.
```

* `mcversion`: The version of Mohist to get the builds for. Can be parsed using the _"Getting available versions"_ route.
* `buildnumber`: The build number of the build to get. 

<details>
  <summary style="font-weight: bold">Example request</summary>

```
GET https://mohistmc.com/api/1.12.2/latest/download
```
</details>