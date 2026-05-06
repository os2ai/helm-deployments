# Changelog

![keep a changelog](https://img.shields.io/badge/Keep%20a%20Changelog-v1.1.0-brightgreen.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGZpbGw9IiNmMTVkMzAiIHZpZXdCb3g9IjAgMCAxODcgMTg1Ij48cGF0aCBkPSJNNjIgN2MtMTUgMy0yOCAxMC0zNyAyMmExMjIgMTIyIDAgMDAtMTggOTEgNzQgNzQgMCAwMDE2IDM4YzYgOSAxNCAxNSAyNCAxOGE4OSA4OSAwIDAwMjQgNCA0NSA0NSAwIDAwNiAwbDMtMSAxMy0xYTE1OCAxNTggMCAwMDU1LTE3IDYzIDYzIDAgMDAzNS01MiAzNCAzNCAwIDAwLTEtNWMtMy0xOC05LTMzLTE5LTQ3LTEyLTE3LTI0LTI4LTM4LTM3QTg1IDg1IDAgMDA2MiA3em0zMCA4YzIwIDQgMzggMTQgNTMgMzEgMTcgMTggMjYgMzcgMjkgNTh2MTJjLTMgMTctMTMgMzAtMjggMzhhMTU1IDE1NSAwIDAxLTUzIDE2bC0xMyAyaC0xYTUxIDUxIDAgMDEtMTItMWwtMTctMmMtMTMtNC0yMy0xMi0yOS0yNy01LTEyLTgtMjQtOC0zOWExMzMgMTMzIDAgMDE4LTUwYzUtMTMgMTEtMjYgMjYtMzMgMTQtNyAyOS05IDQ1LTV6TTQwIDQ1YTk0IDk0IDAgMDAtMTcgNTQgNzUgNzUgMCAwMDYgMzJjOCAxOSAyMiAzMSA0MiAzMiAyMSAyIDQxLTIgNjAtMTRhNjAgNjAgMCAwMDIxLTE5IDUzIDUzIDAgMDA5LTI5YzAtMTYtOC0zMy0yMy01MWE0NyA0NyAwIDAwLTUtNWMtMjMtMjAtNDUtMjYtNjctMTgtMTIgNC0yMCA5LTI2IDE4em0xMDggNzZhNTAgNTAgMCAwMS0yMSAyMmMtMTcgOS0zMiAxMy00OCAxMy0xMSAwLTIxLTMtMzAtOS01LTMtOS05LTEzLTE2YTgxIDgxIDAgMDEtNi0zMiA5NCA5NCAwIDAxOC0zNSA5MCA5MCAwIDAxNi0xMmwxLTJjNS05IDEzLTEzIDIzLTE2IDE2LTUgMzItMyA1MCA5IDEzIDggMjMgMjAgMzAgMzYgNyAxNSA3IDI5IDAgNDJ6bS00My03M2MtMTctOC0zMy02LTQ2IDUtMTAgOC0xNiAyMC0xOSAzN2E1NCA1NCAwIDAwNSAzNGM3IDE1IDIwIDIzIDM3IDIyIDIyLTEgMzgtOSA0OC0yNGE0MSA0MSAwIDAwOC0yNCA0MyA0MyAwIDAwLTEtMTJjLTYtMTgtMTYtMzEtMzItMzh6bS0yMyA5MWgtMWMtNyAwLTE0LTItMjEtN2EyNyAyNyAwIDAxLTEwLTEzIDU3IDU3IDAgMDEtNC0yMCA2MyA2MyAwIDAxNi0yNWM1LTEyIDEyLTE5IDI0LTIxIDktMyAxOC0yIDI3IDIgMTQgNiAyMyAxOCAyNyAzM3MtMiAzMS0xNiA0MGMtMTEgOC0yMSAxMS0zMiAxMXptMS0zNHYxNGgtOFY2OGg4djI4bDEwLTEwaDExbC0xNCAxNSAxNyAxOEg5NnoiLz48L3N2Zz4K)

All notable changes to this project will be documented in this file.

See [keep a changelog] for information about writing changes to this log.

## [Unreleased]

* &mdash;

## [0.4.0-rc.0] - 2026-05-06

### Changed

* Set admin access to other users chats to disabled (false) as default.
* Licensed repo under MPL 2.0.

### Fixed

* Rename webui dashboard ConfigMap data key from `dcgm-dashboard.json` to `openwebui-dashboard.json` to 
  avoid Grafana dashboard filename collisions. Fixes issue #11.
* Upgrade to open-webui 0.8.10
* Support for proper tool call with Mistral model
* Pinned vllm version
* New RAG template (so the same template is not used for web-search and RAG)
* Updated litellm to v1.83.10

## [0.3.0] - 2026-03-10

* Upgraded open-webui to v0.8.5 (last release was v0.6.43)
  See [release](https://github.com/open-webui/open-webui/releases) for information about changes. This is a big jump in
  versions, so we recommend you to check the release notes. _Note_ that you should set repalica count to 1 before
  upgrading and back up once upgraded, which is due to the database migrations.
* Groups share settings have changes, so it now has the values: "members" (string), True (boolean — anyone), False
  (boolean — no one). Where "members" matches the default behavior from the last release. It is this change that has
  held release here back.
* The
  tool [Open WebUI Permissions Manager](https://github.com/AarhusAI/open-webui-permissions-manager?tab=readme-ov-file#share-command)
  has been updated to help update all groups to the same share setting.

## [0.2.0] - 2026-02-25

* Changed nodeSelectorTerm on vllm deployments, for better upgradeability
* Added internal backups for PostgreSQL databases below LiteLLM and OpenWeb UI

## [0.1.1] - 2026-01-14

* Added ArgoCD sync waves to LiteLLM to fix database migration timing (first installation)
* Extracted repoUrl in argo-cd-resources to values.yaml for easier configuration
* Added configuration for the OIDC patch (disabled by default)
* Update docker image with the AAK OIDC patch
* Upgrade open-webui to v0.6.43-1 (**Note**: this release has database updates, and you have to set  `replicaCount` to
  one before updating and back to your count after upgrade. This issue has been fixed in 0.7.x release in core).

## [0.1.0] - 2025-12-16

* Removed embedding model from LiteLLM config.
* Update Open-WebUI to use vllm directly for the embedding model.
* Enabled the login form in Open-WebUI as default.
* Disabled oAuth group management in Open-WebUI.
* Comment out TTS/STT in Open-WebUI as this is not part of the default stack.
* Disabled SSO in Open-WebUI.

[Unreleased]: https://github.com/os2ai/documentation/compare/0.1.1...HEAD
[0.3.0]: https://github.com/os2ai/documentation/compare/0.2.0...0.3.0
[0.2.0]: https://github.com/os2ai/documentation/compare/0.1.1...0.2.0
[0.1.1]: https://github.com/os2ai/documentation/compare/0.1.0...0.1.1
[0.1.0]: https://github.com/os2ai/documentation/releases/tag/0.1.0
