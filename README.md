# ghapi-issue-reproducer

```
export GITHUB_API_TOKEN=...
```

# Verify repos/.../contents works with simpe branhes

```
curl -IL \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md
```

```
curl -IL \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md?ref=main
```

# Create branches with special symbols 
it doesn't matter via UI or vith any git tool

```
bf/2.1@fix-issue
bf/2.1+fix-issue
bf/2.1+!fix-issue
bf/2.1#fix-issue
bf/2.1!fix-issue
```

```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md?ref=bf%2F2.1%40fix-issue
```

```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md?ref=bf%2F2.1%2Bfix-issue
```

```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md?ref=bf%2F2.1%2B%21fix-issue
```

```
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer ${GITHUB_API_TOKEN}" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/stanovchar/ghapi-issue-reproducer/contents/README.md?ref=bf%2F2.1%21fix-issue
```

