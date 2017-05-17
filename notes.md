# Drones-query
### Build modified docker image
```
docker build -t my-drone-query-image .
```
# Run drones-query
```
docker run -d --name my-drone-query-app \
              --link my-rabbit:rabbit \
              --link my-mongo:mongo \
              -p 3002:3000 \
              my-drone-query-image

curl -i -X GET http://localhost:3002/drones/drone999/lastTelemetry
```

