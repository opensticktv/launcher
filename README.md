# OpenStick launcher

The 10-foot home screen and settings UI. Reads app manifests, shows each service's honest resolution ceiling, and talks to `openstickd` for everything else.

Status: design only. Native Android TV app in Kotlin with Compose for TV ([decision 0005](https://github.com/opensticktv/openstick/blob/main/decisions/0005-launcher-ui-stack.md)). It is the home screen if the platform runs Android TV Operator Tier, and a normal app on retail Google TV.

## Requirements from the PRD

- No ads and no sponsored rows; apps in the order the user chooses.
- D-pad first: every screen works with up/down/left/right/select/back.
- Profiles with PIN; hide apps per profile.
- TalkBack, high contrast, adjustable text size; strings externalised from day one.
- First-run privacy disclosure: what Google and the streaming apps collect, with links to each control.

## App manifest

Apps are regular Android apps. The draft manifest schema in [schema/](schema/) is from the earlier Linux design and will be replaced by launcher metadata for Android apps.
