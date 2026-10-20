# Security policy

## Reporting a vulnerability

Please **don't** open a public issue for a security problem.

Report it privately through GitHub instead: go to the repository's **Security** tab and choose **Report a vulnerability**. Include what you found, how to reproduce it, and which version and OS you used.

You'll get a reply within a week. Once a fix is released, the advisory will be published, with credit to you unless you'd rather not.

## What counts

Anything that could let someone harm an EVEMA user, for example:

- a crafted settings, export or import file that makes EVEMA run code, write outside the folder it was meant to, or damage other settings;
- a way to make the Tools tab download or launch something other than what the user confirmed, or to skip its checksum check;
- EVEMA sending anything beyond what [what EVEMA does](docs/what-evema-does.md#what-it-connects-to) lists.

Bugs in the third-party tools EVEMA can launch belong with those projects.

## Supported versions

Only the latest release gets security fixes. Builds are not yet code-signed; check downloads against the `SHA256SUMS` file published with each release.
