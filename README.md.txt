cfx-server-data
The data repository for Cfx.re servers

Deprecation notice
This repository itself is considered finalized/immutable and is currently archived. Pull requests or issue reports were not merged for a while, using the contents of the repository should still be fine (and this shouldn't change until mentioned otherwise).

In the future, relevant parts of this repository will be moved to citizenfx/fivem to be bundled with actual server builds, and the examples (+ legacy API-like resources) will be moved to a new repository.

If there's any critical issue in the code in this repository, posting on the Cfx.re forums may work.

Usage
Make sure to git clone. Don't "Download ZIP", as that'll make it much harder to update to newer versions.
Put custom resources in resources/[local]/ if you don't want to be affected by any random messups.
Advanced usage
You can also consider using the repository as a submodule + symlink for your own Git repository:

Linux:

$ git submodule add https://github.com/citizenfx/cfx-server-data.git vendor/server-data
$ ln -s ../vendor/server-data/resources/ 'resources/[base]/'
Windows:

> git submodule add https://github.com/citizenfx/cfx-server-data.git vendor/server-data
> mklink /d resources\[base] ..\vendor\server-data\resources
Policy
You can make pull requests to propose changes that benefit everyone. Add new useful resources, change/improve existing ones - anything goes, as long as you make sure to:

Not break existing users/APIs.
Not change default behavior without a toggle.
Use best practices (convars over config files, native commands wherever possible, etc.)
Modifying or rewriting existing resources in this repository for local use only is strongly discouraged.