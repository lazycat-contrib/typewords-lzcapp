# TypeWords

LazyCat LPK v2 packaging for `zyronon/typewords:3.0.2`.

TypeWords is an open-source English word and article typing practice tool.

Notes:

- The runtime image uses the `docker.1ms.run` mirror: `docker.1ms.run/zyronon/typewords:3.0.2`.
- Local Docker is not required for packaging or GitHub image update automation.
- The container is configured with `NUXT_PORT=3000`, and the LazyCat upstream points to `http://typewords:3000/`.
- The original container healthcheck is preserved as `services.typewords.healthcheck`.
- GitHub Actions publishes only to MiaoMiao Store.
- The scheduled workflow uses `update.strategy: publish`: a new upstream version is committed, tagged, released, and submitted without opening a PR.

Required GitHub Secrets:

- `APPSTORE_URL`
- `APPSTORE_TOKEN`
- `APP_ID` (optional when the store can resolve `TypeWords` by name)

`LAZYCAT_TOKEN` and official LazyCat store credentials are not used.
