This is a WIP.

## Deploying

### Local MC Client Deployment
To deploy locally to a real MC client (vs the dev one built in the dev environment), simply run the `deployToQAClient` task like so:

_Windows_ \
`gradlew.bat deployToQAClient`

_*nix_ \
`./gradlew deployToQAClient`

-----

Without any configuration, this task will build the final mod jar and then copy it to the mods directory of the local machine's default Minecraft directory is.  This will take into account which OS the local machine has.  This can be overridden, details which can be found in the TBD_LINK section.

The task can optionally toss in some other mods specified as absolute paths in a text file, one per line.  In order to not cause headaches while working with VCS, check out the TBD_LINK section.

-----