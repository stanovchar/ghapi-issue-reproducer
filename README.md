# ghapi-issue-reproducer

```
export GITHUB_API_TOKEN=...
```

# Verify repos/.../contents works with simpe branhes

```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md
```

```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md?ref=main
```

