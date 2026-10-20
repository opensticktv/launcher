# OpenStick launcher

The 10-foot home screen and settings UI. Reads app manifests, shows each service's honest resolution ceiling, and talks to `openstickd` for everything else.

Status: design only. UI stack is open: web or Flutter ([decision 0005](https://github.com/opensticktv/openstick/blob/main/decisions/0005-launcher-ui-stack.md)).

## Requirements from the PRD

- D-pad first: every screen works with up/down/left/right/select/back.
- Service tiles show their ceiling ("Netflix, up to 720p") and status from the playback lab.
- Profiles with PIN; hide apps per profile.
- Screen reader, high contrast, adjustable text size; strings externalised from day one.
- Renders at 1080p; video scales to 4K underneath.
- First-run flow: see [os/docs/first-run.md](https://github.com/opensticktv/os/blob/main/docs/first-run.md).

## App manifest

Apps are Flatpak bundles described by a manifest. Schema: [schema/app-manifest.schema.json](schema/app-manifest.schema.json).
