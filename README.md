# Dall-E Mini Backend
Image Generation Rest API working with Dall-E Mini. 
## API
```
GET /      - Health-Ping
Response: ------------
{"success": true}
```

```
POST /dalle      - Generate images
Request: ------------- 
{
    "num_images": 1,
    "test": "test"
}
Response: ------------
[<base64 encoded image>]
```

## Build
```
docker build -t dalle .
```
## Run
Dalle Mini
```
docker run --gpus all -p 8080:8080 --name dalle-backend dalle
```
Dalle Mega
```
docker run --gpus all -p 8080:8080 --name dalle-backend dalle python3 app.py 8080 MEGA
```

## Reference
https://github.com/borisdayma/dalle-mini