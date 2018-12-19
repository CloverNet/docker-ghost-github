# docker-ghost-github

### From

- docker
- [ghost-custome-storage](https://docs.ghost.org/concepts/storage-adapters/)
- [ghost-github-storage](https://github.com/wangkezun/ghost-github-storage)

### Config.`env`.json

- Add Storage

```
  "storage": {
      "active": "ghost-github-storage",
      "ghost-github-storage": {
          "token": "{YOUR GITHUB TOKEN}",
          "owner": "{YOUR GITHUB NAME}",
          "repo": "{YOUR IMG REPO}",
          "format": "{yyyy}/{mm}/{dd}/{name}-{uuid}-{timestamp}-{random}{ext}"
      }
  }
```

### Docker

```
  docker run -d -p 2368:2368 --name YOUR-GHOST clovernet/docker-ghost-github:latest
```


