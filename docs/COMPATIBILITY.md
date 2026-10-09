# Compatibility policy

Support currently targets Ubuntu Touch 24.04 (Noble) only. OS release, Halium baseline, device variant and port version are separate dimensions.

Each independent device adaptation gets `ut-device-<vendor>-<codename>`. Variants can share a repository only when configuration and qualification explicitly cover each variant. Share a `ut-kernel-` repository only for a common upstream kernel lineage with compatible maintenance requirements.

Use branches for incompatible maintained source lines, tags for immutable releases and channels for artifact delivery. Do not silently move release tags. Administrative force push is an emergency facility; document rewritten published history and its effect on source locks.

Increment the source-lock schema version for incompatible contract changes and update validators together. Adding dependencies requires explicit schema and tooling support. Port fixes increment the patch version; new compatible features increment minor; incompatible installation/storage changes increment major. Experimental releases remain explicitly labeled.
