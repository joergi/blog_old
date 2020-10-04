---
title: "Pushing container to Docker hub"
description: "a short intro how to push containers to docker hub"
categories: [docker, registry, howto]
tags: [docker, registry, howto]
date: 2020-04-29

---

```bash
docker login
docker commit bbcf6acf816d simple-test-project
docker tag simple-test-project:latest joergi/docker_test_project:v1
docker push joergi/docker_test_project:v1
```

this should be enought to push it to docker
