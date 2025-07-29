# 37192

## Current behavior

1. The php tag in the `.gitlab-ci.yml` with the value `php:8.1.0-fpm-alpine3.19` will be upgraded to
   `8.1.31-fpm-alpine3.19`
2. I get one merge request for

   | Package | Type | Update | Change |
      |---|---|---|---|
   | php | image | patch | `8.1.0` -> `8.1.33` |
   | php | final | patch | `8.1.0-fpm-alpine3.19` -> `8.1.31-fpm-alpine3.19` |

## Expected behavior

1. The php tag in the `.gitlab-ci.yml` with the value `php:8.1.0-fpm-alpine3.19` will be upgraded to
   `8.1.33-fpm-alpine3.21` or `8.1.33-fpm-alpine3.22`
2. I will get two merge requests:

| Package | Type  | Update | Change              |
|---------|-------|--------|---------------------|
| php     | image | patch  | `8.1.0` -> `8.1.33` |

| Package | Type  | Update | Change                                            |
|---------|-------|--------|---------------------------------------------------|
| php     | image | patch  | `8.1.0-fpm-alpine3.19` -> `8.1.33-fpm-alpine3.22` |

## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/37192
