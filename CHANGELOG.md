## [1.0.7](https://github.com/Torwent/SRL-T/compare/v1.0.6...v1.0.7) (2023-01-21)


### Bug Fixes

* TRSLogin tweaks and documentation ([a87e92d](https://github.com/Torwent/SRL-T/commit/a87e92dfbc6114ecc0d9d744f144a5c194c1500a))



## [1.0.6](https://github.com/Torwent/SRL-T/compare/v1.0.5...v1.0.6) (2023-01-21)


### Bug Fixes

* typo in Antiban.OnSleeping ([7ad51e8](https://github.com/Torwent/SRL-T/commit/7ad51e8a5642624cc606c548e59efe21e7262bd4))



## [1.0.5](https://github.com/Torwent/SRL-T/compare/v1.0.4...v1.0.5) (2023-01-20)


### Bug Fixes

* remove left over debugging ([06e1230](https://github.com/Torwent/SRL-T/commit/06e1230cbbe00b2761e317df2d0cfed43c5aa6e1))



## [1.0.4](https://github.com/Torwent/SRL-T/compare/v1.0.3...v1.0.4) (2023-01-20)


### Bug Fixes

* added missing login message ([1e33c88](https://github.com/Torwent/SRL-T/commit/1e33c88f83b070a4471f88df0a1ca7786b9dded2))



## [1.0.3](https://github.com/Torwent/SRL-T/compare/f65bc17a9d9cfb93a5b76ffa3ff072c44e92c3cf...v1.0.3) (2023-01-18)


### Bug Fixes

* attempt to fix version not detected ([12184c7](https://github.com/Torwent/SRL-T/commit/12184c7f3d29f71860122f2b113c93cb862658c2))
* fixed issues with GameTabs.GetCurrentTab ([cd9d6f6](https://github.com/Torwent/SRL-T/commit/cd9d6f63ffa02a6a7d3914e62073ed461eb89e8a))
* Inventory.FindItems was not returning the actual slots the items were in. ([1cb1396](https://github.com/Torwent/SRL-T/commit/1cb1396ca366c4243e56fd9c7561114dc7506d0b))
* itemfinder ([36c75ef](https://github.com/Torwent/SRL-T/commit/36c75effb2c3125f19c260c19669f8b299c4a0c0))
* **itemfinder:** fixed noted items ([094b89f](https://github.com/Torwent/SRL-T/commit/094b89f3cf0356a652ffe0158f338dbb08adbdb0))
* magic tab detection ([ea19aae](https://github.com/Torwent/SRL-T/commit/ea19aae596e75c4cbf8274ed44a1612538243437))
* my SRL was renamed to SRL-T ([a3b0a4a](https://github.com/Torwent/SRL-T/commit/a3b0a4a777fb10493c4a6c230b55bf43c9de7924))
* refactored TRSMake ([b2cd1dc](https://github.com/Torwent/SRL-T/commit/b2cd1dc791bb8c65f58b857902994d8259ba0684))
* stop crashes from checking tabs when they are not available ([4724a18](https://github.com/Torwent/SRL-T/commit/4724a188446c9f66123af7b15b6c928fceef28ce))
* typos in the documentation ([467787f](https://github.com/Torwent/SRL-T/commit/467787f484436132c56eccebd14c20afbf8d1a91))
* update docs link ([e85e2fd](https://github.com/Torwent/SRL-T/commit/e85e2fdf90b960272621715c83a176b846fb9a35))
* update item-finder ([4130cf5](https://github.com/Torwent/SRL-T/commit/4130cf587705549e10fa0cb8bc604f46375a30dc))
* update remoteinput plugin ([ec1f4e9](https://github.com/Torwent/SRL-T/commit/ec1f4e93b32a664cb38b47e5cac266c22dd74a36))
* update version gh action ([f2fece7](https://github.com/Torwent/SRL-T/commit/f2fece7b3bbc8c25bfefd5b5b0cba9aea09e9712))


* Bug fixes and minor additions (#65) ([0e9d699](https://github.com/Torwent/SRL-T/commit/0e9d69914cafa0e7089ca9eb2bd95febbb069505)), closes [#65](https://github.com/Torwent/SRL-T/issues/65)


### Features

* added version bumper to my SRL ([4ae462d](https://github.com/Torwent/SRL-T/commit/4ae462d4b9a2a2753c39ce6ac2a5b9ee1264a1c8))
* **bank:** methods to find bank tabs a item is in ([19a335b](https://github.com/Torwent/SRL-T/commit/19a335b85a7d4327f542167fff5724fd4ce56b2c))
* fixed zoom slider and added brightness slider ([f65bc17](https://github.com/Torwent/SRL-T/commit/f65bc17a9d9cfb93a5b76ffa3ff072c44e92c3cf))
* new keybindings.simba file to handle FKeys. ([8fd288d](https://github.com/Torwent/SRL-T/commit/8fd288d85da40aa2b9725ca92b033806305c653f))
* simba1500 walker backport ([31d5378](https://github.com/Torwent/SRL-T/commit/31d53781e9f5ced844e2f721c30a0b6c4a8e9f34))


### BREAKING CHANGES

* This update breaks compatibility with everything! If you update to this version, you will need to update WaspLib as well and the scripts that use them.
* This breaks compatibility with old SRL scripts that used the updated methods because what used to be passed as **roll** is not something else.
* `TRSMainScreen.ConvertDistance()` was renamed to `TRSMainScreen.NormalizeDistance()`.
				 This was renamed by Olly in Simba1500, I guess it's an optional change but I think the rename
				 makes sense and since we are breaking compatibility, might as well bring things closer to 1500
				 already so people have less headaches later.
				 We could also optionally keep both methods and mark this one as deprecated. I'll wait for your feedback.
				 P.S. The method was actually rewrotten in 1500 but was not worth backporting, so I just renamed it!

* fix: update `MainScreen.ConvertDistance()` references to `MainScreen.NormalizeDistance()`

* refactor: added `Contains` methods to equipment and inventory.

I've also left a comment on the PR after the last commit because I forgot to mention TRSBank.ContainsItem().

Anyway, this has the same reasoning. This is optional but I would like to bring the SRL1400 API closer to SRL1500 API.

Old methods are kept and marked with a comment as deprecated so there's no downside to adding this.

This also brings documentation to TRSInventory which is nice :)

* fix: added deprecated warnings

also added more docs to inventory

* fix: added delay after mouse drag release



