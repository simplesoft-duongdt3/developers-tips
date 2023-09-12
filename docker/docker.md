#### 1. Check docker cache
##### docker system df

Example:
TYPE            TOTAL     ACTIVE    SIZE      RECLAIMABLE
Images          138       34        36.18GB   34.15GB (94%)
Containers      74        18        834.8kB   834.6kB (99%)
Local Volumes   118       6         15.31GB   15.14GB (98%)
Build Cache     245       0         1.13GB    1.13GB


#### 2. Clear cache
##### docker image prune -f
##### docker container prune
##### docker buildx prune -f
##### docker rmi $(docker images --filter dangling=true -q)