---
title: Bannerbite API Reference

toc_footers:
  - <a href='https://app.bannerbite.com/'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Bannerbite API
---

# Bannerbite API Reference
> Base URL

```
https://api.bannerbite.com
```

Welcome to the Bannerbite API! [Bannerbite](https://bannerbite.com/) is a service that auto generates images and videos.

Bite-size videos are the perfect way to capture your audience's attention. They're short and sweet, but they still get the point across. With Bannerbite create bite-sized video in seconds!

# Authentication

Bannerbite uses API keys to allow access to the API. You can get an API key from your account settings.

Bannerbite expects the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer API_KEY`

You can find the API key in My Account → API Settings.

<aside class="notice">
You must replace <code>API_KEY</code> with your personal API key.
</aside>

# Projects

## Get All Projects

> The above command returns JSON structured like this:

```json
{
  "data": [
    {
      "id": 1,
      "user_id": 1,
      "name": "Social Media Post 31.09.22",
      "slug": "social-media-post-310922-300925",
      "description": null,
      "settings": null,
      "created_at": "2022-09-31T01:27:00Z",
      "updated_at": "2022-09-31T01:27:00Z",
      "background_color": null,
      "image": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/project/img-project-9_1.jpg",
      "meta": {}
    },
    {
      "id": 2,
      "user_id": 1,
      "name": "Social Media Post 30.09.22",
      "slug": "social-media-post-300922-300924",
      "description": null,
      "settings": null,
      "created_at": "2022-09-30T01:25:28Z",
      "updated_at": "2022-09-30T01:25:28Z",
      "background_color": null,
      "image": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/project/img-project-3_1.jpg",
      "meta": {}
    }
  ]
}
```

This endpoint retrieves all projects.

### HTTP Request

`GET http://example.com/api/projects`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 10 | The API returns 10 items per page by default but you can request up to 100 using this parameter.

## Get a Specific Projects

> The above command returns JSON structured like this:

```json
{
  "data": {
      "id": 1,
      "user_id": 1,
      "name": "Social Media Post 31.09.22",
      "slug": "social-media-post-310922-300925",
      "description": null,
      "settings": null,
      "created_at": "2022-09-31T01:27:00Z",
      "updated_at": "2022-09-31T01:27:00Z",
      "background_color": null,
      "image": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/project/img-project-9_1.jpg",
      "meta": {}
  }
}
```

This endpoint retrieves a specific project.

### HTTP Request

`GET http://example.com/projects/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the project to retrieve

# Bites

## Get All Bites

> The above command returns JSON structured like this:

```json
{
  "data": [
    {
      "id": 1,
      "user_id": 1,
      "project_id": 1,
      "template_id": 1,
      "bite_size_id": 1,
      "name": "Test shareable",
      "slug": "untitled-video-499",
      "output": null,
      "content": "{\"scenes\":[{\"template\":{\"id\":957,\"file_path\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/monaka_uno/1679382245485-Monaka_P_-_1.json\",\"audioUrl\":\"\",\"thumbnail\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/template/images/1679382254309-Monaka_P_-_1.jpg\",\"size\":\"post\",\"name\":\"Monaka Uno\",\"duration\":15,\"currentDuration\":\"4\"},\"sceneData\":[{\"name\":\"sc01_img_01\",\"refId\":\"image_0\",\"url\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/monaka_uno/img_0.png\",\"width\":369,\"height\":139},{\"name\":\"sc01_img_02\",\"refId\":\"image_1\",\"url\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/monaka_uno/img_1.jpg\",\"width\":970,\"height\":970},{\"name\":\"sc01_shp_01\",\"color\":\"#ffffffff\"},{\"name\":\"sc01_shp_02\",\"color\":\"#007369ff\"},{\"name\":\"sc01_shp_03\",\"color\":\"#02a676ff\"},{\"name\":\"sc01_shp_04\",\"color\":\"#02a676ff\"},{\"name\":\"sc01_txt_01\",\"value\":\"JOIN OUR WEBINAR SESSION ON\",\"color\":\"#02a676\"},{\"name\":\"sc01_txt_02\",\"value\":\"The Global Stage: Understanding International Affairs and Political Dynamics\",\"color\":\"#262626\"},{\"name\":\"sc01_txt_03\",\"value\":\"AUGUST 17\",\"color\":\"#02a676\"},{\"name\":\"sc01_txt_04\",\"value\":\"09:30 AM - GMT\",\"color\":\"#0f0f0f\"},{\"name\":\"sc01_txt_05\",\"value\":\"Natalya Miroslava\",\"color\":\"#ffffff\"},{\"name\":\"sc01_txt_06\",\"value\":\"United Nations Foreign\\u000bAffair Officer\",\"color\":\"#ffffff\"}]},{\"template\":{\"id\":960,\"file_path\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/kornigou_uno/1679382942522-Kornigou_P_-_1.json\",\"audioUrl\":\"\",\"thumbnail\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/template/images/1679382962919-Kornigou_P_-_1.jpg\",\"size\":\"post\",\"name\":\"Kornigou Uno\",\"duration\":15,\"currentDuration\":\"4\"},\"sceneData\":[{\"name\":\"sc01_img_01\",\"refId\":\"image_0\",\"url\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/kornigou_uno/img_0.jpg\",\"width\":627,\"height\":515},{\"name\":\"sc01_shp_01\",\"color\":\"#ffd631ff\"},{\"name\":\"sc01_shp_02\",\"color\":\"#e82435ff\"},{\"name\":\"sc01_shp_03\",\"color\":\"#be202eff\"},{\"name\":\"sc01_shp_04\",\"color\":\"#a00110ff\"},{\"name\":\"sc01_shp_05\",\"color\":\"#a91d2aff\"},{\"name\":\"sc01_txt_01\",\"value\":\"Today's Session\",\"color\":\"#ffffff\"},{\"name\":\"sc01_txt_02\",\"value\":\"Influence & Persuasion\",\"color\":\"#1a1a1a\"},{\"name\":\"sc01_txt_03\",\"value\":\"Unlocking the secrets of effective communication and influence.\",\"color\":\"#1a1a1a\"},{\"name\":\"sc01_txt_04\",\"value\":\"Brian Henderson\",\"color\":\"#ffffff\"},{\"name\":\"sc01_txt_05\",\"value\":\"MAX Inc Community Officer\",\"color\":\"#ffffff\"}]}],\"audioUrl\":\"\",\"audioInPoint\":\"00:00\",\"totalDuration\":\"8s\",\"is_fade\":false,\"is_render_all_format\":false,\"is_trigger_shared_form\":false,\"webhook_single_video\":false,\"webhook\":\"\"}",
      "settings": "",
      "created_at": "2023-03-29T20:51:59Z",
      "updated_at": "2023-04-05T05:24:18Z",
      "generated_lottie": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/generated_lottie/UntitledVideo-1680148959432.mp4",
      "access_token": "Mk0DVMXVYFEKZRAzxdVf"
    }
  ]
}
```

This endpoint retrieves all bites.

### HTTP Request

`GET http://example.com/api/bites`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 10 | The API returns 10 items per page by default but you can request up to 100 using this parameter.
project_id | required | The ID of the project to retrieve

<aside class="notice">
To retrieve bite data, you need to include the <code>project_id</code> parameter in your request.
</aside>

## Get a Specific Bites

> The above command returns JSON structured like this:

```json
{
  "data": {
    "id": 1,
    "user_id": 1,
    "project_id": 1,
    "template_id": 1,
    "bite_size_id": 1,
    "name": "Test shareable",
    "slug": "untitled-video-499",
    "output": null,
    "content": "{\"scenes\":[{\"template\":{\"id\":957,\"file_path\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/monaka_uno/1679382245485-Monaka_P_-_1.json\",\"audioUrl\":\"\",\"thumbnail\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/template/images/1679382254309-Monaka_P_-_1.jpg\",\"size\":\"post\",\"name\":\"Monaka Uno\",\"duration\":15,\"currentDuration\":\"4\"},\"sceneData\":[{\"name\":\"sc01_img_01\",\"refId\":\"image_0\",\"url\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/monaka_uno/img_0.png\",\"width\":369,\"height\":139},{\"name\":\"sc01_img_02\",\"refId\":\"image_1\",\"url\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/monaka_uno/img_1.jpg\",\"width\":970,\"height\":970},{\"name\":\"sc01_shp_01\",\"color\":\"#ffffffff\"},{\"name\":\"sc01_shp_02\",\"color\":\"#007369ff\"},{\"name\":\"sc01_shp_03\",\"color\":\"#02a676ff\"},{\"name\":\"sc01_shp_04\",\"color\":\"#02a676ff\"},{\"name\":\"sc01_txt_01\",\"value\":\"JOIN OUR WEBINAR SESSION ON\",\"color\":\"#02a676\"},{\"name\":\"sc01_txt_02\",\"value\":\"The Global Stage: Understanding International Affairs and Political Dynamics\",\"color\":\"#262626\"},{\"name\":\"sc01_txt_03\",\"value\":\"AUGUST 17\",\"color\":\"#02a676\"},{\"name\":\"sc01_txt_04\",\"value\":\"09:30 AM - GMT\",\"color\":\"#0f0f0f\"},{\"name\":\"sc01_txt_05\",\"value\":\"Natalya Miroslava\",\"color\":\"#ffffff\"},{\"name\":\"sc01_txt_06\",\"value\":\"United Nations Foreign\\u000bAffair Officer\",\"color\":\"#ffffff\"}]},{\"template\":{\"id\":960,\"file_path\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/kornigou_uno/1679382942522-Kornigou_P_-_1.json\",\"audioUrl\":\"\",\"thumbnail\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/template/images/1679382962919-Kornigou_P_-_1.jpg\",\"size\":\"post\",\"name\":\"Kornigou Uno\",\"duration\":15,\"currentDuration\":\"4\"},\"sceneData\":[{\"name\":\"sc01_img_01\",\"refId\":\"image_0\",\"url\":\"https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/kornigou_uno/img_0.jpg\",\"width\":627,\"height\":515},{\"name\":\"sc01_shp_01\",\"color\":\"#ffd631ff\"},{\"name\":\"sc01_shp_02\",\"color\":\"#e82435ff\"},{\"name\":\"sc01_shp_03\",\"color\":\"#be202eff\"},{\"name\":\"sc01_shp_04\",\"color\":\"#a00110ff\"},{\"name\":\"sc01_shp_05\",\"color\":\"#a91d2aff\"},{\"name\":\"sc01_txt_01\",\"value\":\"Today's Session\",\"color\":\"#ffffff\"},{\"name\":\"sc01_txt_02\",\"value\":\"Influence & Persuasion\",\"color\":\"#1a1a1a\"},{\"name\":\"sc01_txt_03\",\"value\":\"Unlocking the secrets of effective communication and influence.\",\"color\":\"#1a1a1a\"},{\"name\":\"sc01_txt_04\",\"value\":\"Brian Henderson\",\"color\":\"#ffffff\"},{\"name\":\"sc01_txt_05\",\"value\":\"MAX Inc Community Officer\",\"color\":\"#ffffff\"}]}],\"audioUrl\":\"\",\"audioInPoint\":\"00:00\",\"totalDuration\":\"8s\",\"is_fade\":false,\"is_render_all_format\":false,\"is_trigger_shared_form\":false,\"webhook_single_video\":false,\"webhook\":\"\"}",
    "settings": "",
    "created_at": "2023-03-29T20:51:59Z",
    "updated_at": "2023-04-05T05:24:18Z",
    "generated_lottie": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/generated_lottie/UntitledVideo-1680148959432.mp4",
    "access_token": "Mk0DVMXVYFEKZRAzxdVf",
    "template": {
      "id": 1,
      "user_id": 1,
      "category_id": null,
      "name": "Kornigou Uno",
      "slug": "kornigou-uno",
      "description": null,
      "type": null,
      "content": "{\"duration\":15.066666666666666,\"scene\":1}",
      "file_path": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/template/kornigou_uno/1679382942522-Kornigou_P_-_1.json",
      "thumbnail_path": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/thumbnail/template/images/1680578980340-Kornigou_P_-_1_[f0075](1).jpg",
      "is_published": 1,
      "is_default": 1,
      "created_at": "2023-03-21T00:15:47.000Z",
      "updated_at": "2023-04-03T20:29:46.000Z",
      "thumbnail_large_path": null,
      "video_preview_small": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/video/preview/template/videos/1680578983595-Kornigou_P_-_1-74.mp4",
      "video_preview_large": null,
      "size": "post",
      "audio_path": null,
      "categories": "[\"Podcast\",\"Profile\",\"Social Media\",\"Webinar\"]",
      "external_id": null,
      "upload_from": "bannerbite",
      "is_allow_video": 0
    },
    "size": {
      "id": 1,
      "user_id": null,
      "name": "Post",
      "slug": "post",
      "width": 1080,
      "height": 1350,
      "description": "For Instagram or Facebook post",
      "icon": null,
      "background_color": "#ffffff",
      "created_at": "2022-01-19T19:09:33.000Z",
      "updated_at": "2022-01-19T19:09:33.000Z"
    }
  }
}
```

This endpoint retrieves a specific project.

### HTTP Request

`GET http://example.com/bites/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the bite to retrieve

## Get Scenes Data

> The above command returns JSON structured like this:

```json
[
  {
      "name": "scene01_image_01",
      "value": "https://bannerbite-dev-storage.s3.eu-central-1.amazonaws.com/gallery/images/1683178194469-tranpsarent-dummy-scene.png"
  },
  {
      "name": "scene01_text_01",
      "value": "Rune  Kristine Fiske ",
      "color": "#ffffff"
  },
  {
      "name": "scene01_text_02",
      "value": "2. kandidat i Lillestrøm",
      "color": "#ffffff"
  },
  {
      "name": "scene01_text_03",
      "value": "Arbeiderpartiet står for frihet, likhet og solidaritet. Les om Arbeiderpartiets politikk og politikere.",
      "color": "#1f1f1f"
  },
  {
      "name": "scene01_video",
      "value": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/bite/videos/1686534630750-25s_5scene1686050915369overlay.mp4",
      "height": 1350,
      "width": 1082,
      "inPoint": "00:00",
      "outPoint": "00:25",
      "visibility": true,
      "position": {
          "x": 0,
          "y": 2,
          "finalWidth": 1080,
          "finalHeight": 1347
      }
  }
]
```

This endpoint retrieves scenes data from bite.

### HTTP Request

`GET http://example.com/api/sceneData/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the bite to retrieve

### Scene Data Parameters

<img src="/images/scenedata.png" alt="Scene Data" width="70%" height="70%">

### Parameters Text
Parameter | Type | Description
--------- | ------- | -----------
name | string | The variables used to identify the scene and the parameters to be used
value | string | Value to be filled in the scene
color | string | The variable used to change the color of the text

### Parameters Image
Parameter | Type  | Description
--------- | ------- | -----------
name | string | The variables used to identify the scene and the parameters to be used
value | string | Value to be filled in the scene

### Parameters Video
Parameter | Type | Description
--------- | ------- | -----------
name | string | The variables used to identify the scene and the parameters to be used
value | string | Value to be filled in the scene
Height | number | Height of video
Width | number | Width of video
inPoint | string | The start of video to be inserted with format <code>mm:ss</code>
outPoint | string | The end of video to be inserted with format <code>mm:ss</code>
visibility | boolean | Variables used to show and hide videos
position | object | Video position


# Renders

## Generate Image/Video
> Example JSON:

```json
{
  "uid": "ASDbdsabkasdj126",
  "audio": {
      "url": "",
      "inPoint": "00:00"
  },
  "type": "image",
  "email": "",
  "scene": 1,
  "webhook": "",
  "sceneData": [
    {
        "name": "scene01_image_01",
        "value": "https://bannerbite-dev-storage.s3.eu-central-1.amazonaws.com/gallery/images/1683178194469-tranpsarent-dummy-scene.png"
    },
    {
        "name": "scene01_text_01",
        "value": "Rune  Kristine Fiske ",
        "color": "#ffffff"
    },
    {
        "name": "scene01_text_02",
        "value": "2. kandidat i Lillestrøm",
        "color": "#ffffff"
    },
    {
        "name": "scene01_text_03",
        "value": "Arbeiderpartiet står for frihet, likhet og solidaritet. Les om Arbeiderpartiets politikk og politikere.",
        "color": "#1f1f1f"
    },
    {
        "name": "scene01_video",
        "value": "https://bannerbite-storage.s3.eu-central-1.amazonaws.com/bite/videos/1686534630750-25s_5scene1686050915369overlay.mp4",
        "height": 1350,
        "width": 1082,
        "inPoint": "00:00",
        "outPoint": "00:25",
        "visibility": true,
        "position": {
            "x": 0,
            "y": 2,
            "finalWidth": 1080,
            "finalHeight": 1347
        }
    }
  ]
}
```

> The above command returns JSON structured like this:

```json
{
  "message": "Render request has been aceppted and now in progress"
}
```

This endpoint generate a image or video.

### HTTP Request

`POST http://example.com/render`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the bite to retrieve

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
uid | string | ID or Access Token from Bite (Required)
audio | object | Object of audio include <code>url</code> and <code>inPoint</code> (Optional)
email | string | The resulting video rendering will be sent via email (Optional)
type | string | Type of render <code>image</code>, <code>video</code> or <code>overlay</code> (Default: image)
scene | number | If the type is <code>image</code>, the <code>scene</code> parameter is required. This parameter determines which scene will be rendered (Default: 1)
webhook | string | Please provide the webhook URL where you would like to receive notifications or updates by filling in the designated field (Default: null)
sceneData | object | Array of object include email and scenes data (Required)