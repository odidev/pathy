## [0.6.1](https://github.com/justindujardin/pathy/compare/v0.6.0...v0.6.1) (2021-10-25)


### Bug Fixes

* Update for Python 3.10 compatibility ([#68](https://github.com/justindujardin/pathy/issues/68)) ([450c2f2](https://github.com/justindujardin/pathy/commit/450c2f206efefe3d96e24294f5d02f8e9ceaf4ff))

# [0.6.0](https://github.com/justindujardin/pathy/compare/v0.5.2...v0.6.0) (2021-06-26)


### Features

* support smart_open >=5.0.0,<6.0.0 ([#63](https://github.com/justindujardin/pathy/issues/63)) ([9718752](https://github.com/justindujardin/pathy/commit/97187528b70fdb96e928e1f90a3b06732e126b16))


### BREAKING CHANGES

* This change removes support for smart_open < 5.0.0

The API for specifying s3 credentials changed in smart_open v5, so previous versions are incompatible.

## [0.5.2](https://github.com/justindujardin/pathy/compare/v0.5.1...v0.5.2) (2021-04-24)


### Features

* **cli:** add version number to cli help string ([#55](https://github.com/justindujardin/pathy/issues/55)) ([8001907](https://github.com/justindujardin/pathy/commit/800190760759f35a545948a12417952451e7891f))

## [0.5.1](https://github.com/justindujardin/pathy/compare/v0.5.0...v0.5.1) (2021-04-23)


### Features

* **clients:** add support for S3 bucket storage ([#54](https://github.com/justindujardin/pathy/issues/54)) ([5bb7e1b](https://github.com/justindujardin/pathy/commit/5bb7e1b8faa422c8a80d91d7d8e71f6de4052962))

# [0.5.0](https://github.com/justindujardin/pathy/compare/v0.4.0...v0.5.0) (2021-04-22)


### Bug Fixes

* **auto-import:** move public exports into __init__.py ([fd09021](https://github.com/justindujardin/pathy/commit/fd090215efc392e76d167e9c0203520c251578da))
* **cli:** ls returns code 1 from invalid sources ([b2ff829](https://github.com/justindujardin/pathy/commit/b2ff829f35db6b5af25c9bc553f1e1b76be7e39c))
* **samefile:** compare self.key to other.key not self.key ([688628e](https://github.com/justindujardin/pathy/commit/688628ecbf430284fbcb83142d7751e0b54475d2))


### BREAKING CHANGES

* **auto-import:** Previously you could import symbols directly from their files in the module, e.g. `from pathy.base import Pathy`. Now you must import them from the base package, e.g. `from pathy import Pathy`.

# [0.4.0](https://github.com/justindujardin/pathy/compare/v0.3.6...v0.4.0) (2021-02-15)


### Bug Fixes

* **gcs:** stop handling DefaultCredentialsError ([d4754ff](https://github.com/justindujardin/pathy/commit/d4754ff9be5fc5ecce35ba8658097a1dd29ce5d0)), closes [#43](https://github.com/justindujardin/pathy/issues/43)


### BREAKING CHANGES

Pathy would previously handle google's DefaultCredentialsError and raise its own, which covered some use-cases and confused others. If google's cloud SDK cannot find default credentials, you will need to handle that exception manually.

## [0.3.6](https://github.com/justindujardin/pathy/compare/v0.3.5...v0.3.6) (2021-02-10)


### Features

* **cli:** add "-l" flag to ls command ([e47fb02](https://github.com/justindujardin/pathy/commit/e47fb02db95b62d1060bd48d505706bcbcbbc22b))
* **Pathy:** add "ls" method for quickly querying blobs with stats ([bf452e7](https://github.com/justindujardin/pathy/commit/bf452e7b658cdc4b391155264c91ddeeaed09220))
* **tests:** include tests in pypi package ([#44](https://github.com/justindujardin/pathy/issues/44)) ([d6ad724](https://github.com/justindujardin/pathy/commit/d6ad7244452e874e97246f38d29d0fe8e77c5b76))

## [0.3.5](https://github.com/justindujardin/pathy/compare/v0.3.4...v0.3.5) (2021-02-02)


### Bug Fixes

* **pypi:** add requirements.txt to distribution ([#45](https://github.com/justindujardin/pathy/issues/45)) ([759cd86](https://github.com/justindujardin/pathy/commit/759cd862be15dd1683248cdbdc0873e64f2712da))
* python 3.9 compatibility ([#46](https://github.com/justindujardin/pathy/issues/46)) ([a965f40](https://github.com/justindujardin/pathy/commit/a965f40a086ccb305e58936813a30c35f95d5212))

## [0.3.4](https://github.com/justindujardin/pathy/compare/v0.3.3...v0.3.4) (2020-11-22)


### Features

* **clients:** add set_client_params for specifying client-specific args ([#39](https://github.com/justindujardin/pathy/issues/39)) ([84b9987](https://github.com/justindujardin/pathy/commit/84b9987d4a7819ed6b9c8475523036d5809b1b2a))

## [0.3.3](https://github.com/justindujardin/pathy/compare/v0.3.2...v0.3.3) (2020-11-12)


### Bug Fixes

* path.scheme would error with schemeless paths ([#37](https://github.com/justindujardin/pathy/issues/37)) ([80f0036](https://github.com/justindujardin/pathy/commit/80f003670e9ce2515b23813fec9dfdf7a6696fb3))

## [0.3.2](https://github.com/justindujardin/pathy/compare/v0.3.1...v0.3.2) (2020-11-12)


### Bug Fixes

* upgrade smart-open to >=2.2.0,<4.0.0 ([#36](https://github.com/justindujardin/pathy/issues/36)) ([fdf083e](https://github.com/justindujardin/pathy/commit/fdf083eb711f225e577e9f6199a7a403b49bf2ea))

## [0.3.1](https://github.com/justindujardin/pathy/compare/v0.3.0...v0.3.1) (2020-09-26)


### Features

* update smart-open to 2.2.0 for minimal deps ([4b3e959](https://github.com/justindujardin/pathy/commit/4b3e959ce1c4c491cb291935e8d47ac537b72485))
* **ci:** add pyright check to lint step ([10ce34d](https://github.com/justindujardin/pathy/commit/10ce34d13ddc99232b3ce7681db27f561d51c87b))

# [0.3.0](https://github.com/justindujardin/pathy/compare/v0.2.0...v0.3.0) (2020-09-04)


### Code Refactoring

* add BasePathy class to bind PathType var to ([796dd40](https://github.com/justindujardin/pathy/commit/796dd407fca72c5297914e597f3221fdbcd9e95e))


### Features

* add get_client/register_client for supporting multiple services ([747815b](https://github.com/justindujardin/pathy/commit/747815b46e1e3cd61e6e69d04b52f5f5958ed373))
* **ci:** add lint check before testing ([2633480](https://github.com/justindujardin/pathy/commit/263348028fe5c217163632d9fd002cd7f5b5c77c))
* **GCS:** print install command when using GCS without deps installed ([d8dbcd4](https://github.com/justindujardin/pathy/commit/d8dbcd41d1e813090cad906c81df95880ae7289c))


### BREAKING CHANGES

* This renames the internal GCS/File adapter classes by removing the prefix Client.

- ClientBucketFS -> BucketFS
- ClientBlobFS -> BlobFS
- ClientBucketGCS -> BucketGCS
- ClientBlobGCS -> BlobGCS
- BucketStat -> BlobStat
* use_fs, get_fs_client, use_fs_cache, get_fs_cache, and clear_fs_cache moved from pathy.api to pathy.clients

# [0.2.0](https://github.com/justindujardin/pathy/compare/v0.1.3...v0.2.0) (2020-08-22)


### Code Refactoring

* rename PureGCSPath to PurePathy ([5632f26](https://github.com/justindujardin/pathy/commit/5632f264ed5d22b54b1c284ca1d79d2e248c5fd3))


### Features

* **build:** use husky to auto update docs when code changes ([5a32357](https://github.com/justindujardin/pathy/commit/5a32357db47f003fb3ebc6345d7fa4cee829fd99))
* **README:** generate API and CLI docs ([0213d2f](https://github.com/justindujardin/pathy/commit/0213d2f7028c08d40d863d1cc123e7d55ff1c89f))


### BREAKING CHANGES

* PureGCSPath is now PurePathy

## [0.1.3](https://github.com/justindujardin/pathy/compare/v0.1.2...v0.1.3) (2020-06-28)


### Features

* upgrade typer support ([e481000](https://github.com/justindujardin/pathy/commit/e4810004eff21a605626d30cd717983787a6a8c6))

## [0.1.2](https://github.com/justindujardin/pathy/compare/v0.1.1...v0.1.2) (2020-05-23)


### Bug Fixes

* path.owner() can raise when using filesystem adapter ([2877b06](https://github.com/justindujardin/pathy/commit/2877b06562e4bb1d4767e9c297e2aee2fc1284ad))

## [0.1.1](https://github.com/justindujardin/pathy/compare/v0.1.0...v0.1.1) (2020-04-24)


### Features

* **cli:** add -r and -v flags for safer usage ([a87e36f](https://github.com/justindujardin/pathy/commit/a87e36fbc13a705c1f7f9ed7909ff6c9fe8e494e))

# [0.1.0](https://github.com/justindujardin/pathy/compare/v0.0.17...v0.1.0) (2020-04-24)


### Features

* add FluidPath and GCSPath.fluid method ([3393226](https://github.com/justindujardin/pathy/commit/3393226bc7f390f696d109bfac5f44e59a8b5151))
* **cli:** add ls [path] command ([17cab1d](https://github.com/justindujardin/pathy/commit/17cab1d8b96d92ca79e18512ac7e8a42aa136066))
* **cli:** add pathy executable with cp and mv commands ([98760fc](https://github.com/justindujardin/pathy/commit/98760fcfc0cb62891b7f2aac81a74fef088fdf78))
* **cli:** add rm [path] command ([31cea91](https://github.com/justindujardin/pathy/commit/31cea9156d99d9d465569c20c566943d4238c5dd))
* **pathy:** rename library to be more generic ([c62b14d](https://github.com/justindujardin/pathy/commit/c62b14da2aba25024af647e29df09ee57a13f6bd))

## [0.0.17](https://github.com/justindujardin/pathy/compare/v0.0.16...v0.0.17) (2020-04-17)


### Bug Fixes

* do not de/compress opened files based on extension ([22d14e7](https://github.com/justindujardin/pathy/commit/22d14e7d4919f16ca54bf28e685c221f7c96f8d3))

## [0.0.16](https://github.com/justindujardin/pathy/compare/v0.0.15...v0.0.16) (2020-04-16)


### Features

* **typing:** expose library python types to mypy ([53cf348](https://github.com/justindujardin/pathy/commit/53cf34845399e1d31538dc02e462d7e02bcd32a6))

## [0.0.15](https://github.com/justindujardin/pathy/compare/v0.0.14...v0.0.15) (2020-04-16)


### Bug Fixes

* **requirements:** remove typer dependency ([08e8fa0](https://github.com/justindujardin/pathy/commit/08e8fa0baa186b710a6adf2205b0a51bbd39fe37))

## [0.0.14](https://github.com/justindujardin/pathy/compare/v0.0.13...v0.0.14) (2020-04-16)


### Bug Fixes

* **iterdir:** don't return empty results ([2a8b870](https://github.com/justindujardin/pathy/commit/2a8b870c2ca232431c65808050363e8faff60ba2))

## [0.0.13](https://github.com/justindujardin/pathy/compare/v0.0.12...v0.0.13) (2020-04-16)


### Bug Fixes

* **to_local:** issue where files without extensions would not be cached ([3d543a8](https://github.com/justindujardin/pathy/commit/3d543a88a81604d13f8e401422d59803d9bb3943))

## [0.0.12](https://github.com/justindujardin/pathy/compare/v0.0.11...v0.0.12) (2020-04-15)


### Bug Fixes

* recursion error when copying blob folders ([8b6e01c](https://github.com/justindujardin/pathy/commit/8b6e01c3e8c35a78deee60d45563b27b7a732e9a))

## [0.0.11](https://github.com/justindujardin/pathy/compare/v0.0.10...v0.0.11) (2020-04-15)


### Features

* **to_local:** support caching folders ([cc56f6e](https://github.com/justindujardin/pathy/commit/cc56f6eab21f850f0521013749589ad0736e261d))

## [0.0.10](https://github.com/justindujardin/pathy/compare/v0.0.9...v0.0.10) (2020-04-14)


### Features

* add `use_fs_caching` and `Pathy.to_local` for caching ([2894360](https://github.com/justindujardin/pathy/commit/2894360d48e3ac4b28ecb4627eb562f9e65b3c93))

## [0.0.9](https://github.com/justindujardin/pathy/compare/v0.0.8...v0.0.9) (2020-04-08)


### Features

* add `resolve` method ([7cebc69](https://github.com/justindujardin/pathy/commit/7cebc69bfc88b1a522defdce1637f5159c37def6))

## [0.0.8](https://github.com/justindujardin/pathy/compare/v0.0.7...v0.0.8) (2020-04-08)


### Features

* allow passing Pathy to spacy.Model.to_disk ([1d628cb](https://github.com/justindujardin/pathy/commit/1d628cb8c5056683590d9f2403f1482e2a310971))
* **use_fs:** allow passing root folder as Path ([3635152](https://github.com/justindujardin/pathy/commit/36351525bf84001ed4f9b0b7abf842f8e27ef1f0))

## [0.0.7](https://github.com/justindujardin/pathy/compare/v0.0.6...v0.0.7) (2020-03-30)


### Bug Fixes

* **gcs:** gracefully handle invalid gcs client case ([529f630](https://github.com/justindujardin/pathy/commit/529f63026abe1b11c3336febb152a030e28a85ef))

## [0.0.6](https://github.com/justindujardin/pathy/compare/v0.0.5...v0.0.6) (2020-03-30)


### Features

* add github releases for each pypi version ([66dbed8](https://github.com/justindujardin/pathy/commit/66dbed851346372ab84080f027113aba054452af))

## [0.0.5](https://github.com/justindujardin/pathy/compare/v0.0.4...v0.0.5) (2020-03-30)

### Bug Fixes

- generating changelog ([ef43ed1](https://github.com/justindujardin/pathy/commit/ef43ed11a140ed3cfaba2e7d72b7c01c7275c8d6))

## [0.0.4](https://github.com/justindujardin/pathy/compare/v0.0.3...v0.0.4) (2020-03-30)

### Features

- support unlink path operation

## [0.0.3](https://github.com/justindujardin/pathy/compare/v0.0.2...v0.0.3) (2020-03-30)

### Features

- **gcs:** use smart_open for streaming files ([e557ab9](https://github.com/justindujardin/pathy/pull/3/commits/e557ab9e3bc7c0edcb02333fe8ea6be760c152dc))
- add file-system bucket adapter ([1c72f47](https://github.com/justindujardin/pathy/pull/3/commits/1c72f475fde8de1c6cb3af23d63b793722fe82e2))
- use_fs stores buckets on the file-system ([f717280](https://github.com/justindujardin/pathy/pull/3/commits/f7172806d0ae3e408aafc12fe7526b9852ce8b36))

## [0.0.2](v0.0.1...v0.0.2) (2020-03-18)

### Bug Fixes

- **tests:** enable unit tests on ci ([dd56011](dd56011))
