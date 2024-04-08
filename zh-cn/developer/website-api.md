## 网站 JSON API

---
# API V2

在此处访问 API V2 文档: https://new.mohistmc.com/mohistmc-api

# API V1

### 重要提醒: API V1 将在 2024 年 12 月 31 日终止。

API 路径: https://mohistmc.com/api/ 

* 行为提示: 若请求路径不存在，API将返回`404`。

### 获取可用该版本

```
GET https://mohistmc.com/api/versions

-> 返回一个包含字符串的JSON数组。
```

获取可用的 Mohist 版本列表。

<details>
  <summary style="font-weight: bold">请求返回值示例</summary>

```json
[
  "1.7.10",
  "1.12.2",
  "1.16.5",
  "1.18.2-testing"
]
```
</details>

### 获取所有构建版本

```
GET https://mohistmc.com/api/<mcversion>/

-> 返回一个包含构建信息对象的JSON数组。
```

* `mcversion`: 要获取构建信息的 Mohist 版本。 可以从 _"获取可用的 Mohist 版本列表"_ 路径提取。

获取特定 Mohist 版本的可用构建列表。

> 可使用附加参数筛选请求结果。

获取所有 `SUCCESS` (成功)构建:

```
GET https://mohistmc.com/api/<mcversion>?status=SUCCESS

-> 返回一个包含成功构建信息对象的JSON数组。
```

获取所有 `FAILED` (失败)构建:

```
GET https://mohistmc.com/api/<mcversion>?status=FAILED

-> 返回一个包含失败构建信息对象的JSON数组。
```

### 获取特定构建版本

> 提示: 获取不存在的构建版本将返回 404 错误和"Build not found"字符串响应体。
```
GET https://mohistmc.com/api/<mcversion>/<buildnumber>/

-> 返回构建信息JSON对象。
```

* `mcversion`: 要获取构建信息的 Mohist 版本。可以从 _"获取可用的 Mohist 版本列表"_ 路径提取。
* `buildnumber`: 要获取的构建版本的构建号。

获取特定 Mohist 版本的特定构建版本信息。

<details>
  <summary style="font-weight: bold">成功构建请求返回值示例</summary>

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
  <summary style="font-weight: bold">失败构建请求返回值示例</summary>

```json
{
  "status": "FAILED",
  "number": 25
}
```
</details>

### 获取最新构建版本

> 提示: 此API**总是**返回成功构建的信息.

```
GET https://mohistmc.com/api/<mcversion>/latest/

-> 返回一个包含构建信息的JSON对象。
```

* `mcversion`: 要获取构建信息的 Mohist 版本。可以从 _"获取可用的 Mohist 版本列表"_ 路径提取。

获取特定 Mohist 版本的最新构建版本信息。

<details>
  <summary style="font-weight: bold">用法示例</summary>

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

### 使用API下载一个构建版本

```
GET https://mohistmc.com/api/<mcversion>/<buildnumber>/download

-> 返回构建 jar 文件。
```

* `mcversion`: 要获取构建信息的 Mohist 版本。可以从 _"获取可用的 Mohist 版本列表"_ 路径提取。
* `buildnumber`: 要获取的构建版本的构建号。

<details>
  <summary style="font-weight: bold">请求示例</summary>

```
GET https://mohistmc.com/api/1.12.2/300/download
```
</details>

### 使用API下载最新构建版本

```
GET https://mohistmc.com/api/<mcversion>/latest/download

-> 返回构建 jar 文件。
```

* `mcversion`: 要获取构建信息的 Mohist 版本。可以从 _"获取可用的 Mohist 版本列表"_ 路径提取。

<details>
  <summary style="font-weight: bold">请求示例</summary>

```
GET https://mohistmc.com/api/1.12.2/latest/download
```
</details>
