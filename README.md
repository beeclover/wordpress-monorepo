wordpress monorepo

## Feature

- 배포, 릴리즈 자동화 (CI/CD)
- 폴더구조
- eslint, prettier
- tailwindcss

## CI/CD

- **릴리즈 자동화** 테마 릴리즈 자동화 (테마 빌드결과물 zip으로 에셋 담아줌)
- **배포 자동화** 프로덕션 서버에 rsync로 테마파일 업데이트

## 폴더구조

프로젝트 코드베이스 구성

```shell
$ tree
.  # https://github.com/beeclover/wordpress-docker 참고
|-- Makefile
|-- README.md
|-- apps
|   `-- v1  # wordpress-monorepo 구성!
|       |-- README.md
|       `-- theme (require)
|-- volumes
|   `-- v1
|       |-- wp
|       `-- db
|-- docker-compose.override.yaml
`-- docker-compose.yaml
```

`.vscode/settings.json`에서 `intelephense` 설정을 추가해서 `volumes/v1/wp`의 폴더를 레퍼런스로 가져올수있도록하였다.
