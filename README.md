# concourse-bump-git-semver
Sample concourse pipelines that show bumping the semver version via a git file.

The samples use the concourse [semver resource type](https://github.com/concourse/semver-resource#readme) and its [`git`](https://github.com/concourse/semver-resource#git-driver) driver.

The sample files show the possible [bumping semantics supported](https://github.com/concourse/semver-resource#version-bumping-semantics):
* bump: Optional. Bump the version number semantically. The value must be one of:
  * [major](pipeline-bump-major.yml): Bump the major version number, e.g. 1.0.0 -> 2.0.0.
  * [minor](pipeline-bump-minor.yml): Bump the minor version number, e.g. 0.1.0 -> 0.2.0.
  * [patch](pipeline-bump-patch.yml): Bump the patch version number, e.g. 0.0.1 -> 0.0.2.
  * [final](pipeline-bump-final.yml): Promote the version to a final version, e.g. 1.0.0-rc.1 -> 1.0.0.
* [pre](pipeline-bump-pre.yml): Optional. When bumping, bump to a prerelease (e.g. rc or alpha), or bump an existing prerelease.
