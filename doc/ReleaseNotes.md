# v00.04.03

* 2022-09-21 Thomas Madlener ([PR#27](https://github.com/key4hep/k4lcioreader/pull/27))
  - Make the `k4LCIOReader` interface conform to `podio::IReader` again, after [AIDASoft/podio#323](https://github.com/AIDASoft/podio/pull/323)
    - The newly added functions are just stubs for the moment.

# v00.04.02

* 2022-06-16 Thomas Madlener ([PR#25](https://github.com/key4hep/k4lcioreader/pull/25))
  - Fix the TrackState conversion after `time` field has been added in key4hep/EDM4hep#138.
    - For now filling a dummy value of `-1` and zeroing out the covariance matrix.

* 2022-05-25 Valentin Volkl ([PR#24](https://github.com/key4hep/k4lcioreader/pull/24))
  - remove HitContributions from Clusters as in  https://github.com/key4hep/EDM4hep/pull/140

* 2022-05-25 Valentin Volkl ([PR#23](https://github.com/key4hep/k4lcioreader/pull/23))
  - remove edx from TrackerHits as in https://github.com/key4hep/EDM4hep/pull/139

* 2022-05-19 Placido Fernandez Declara ([PR#22](https://github.com/key4hep/k4lcioreader/pull/22))
  - Handle possible nullptr on conversion that could lead to segfault

* 2022-03-21 Valentin Volkl ([PR#21](https://github.com/key4hep/k4lcioreader/pull/21))
  - tests: fix wget command

# v00.04.01

* 2022-02-10 Placido Fernandez Declara ([PR#20](https://github.com/key4hep/k4LCIOReader/pull/20))
  - Add missing method from update podio::IReader interface, fixes #19

* 2022-01-28 Andre Sailer ([PR#18](https://github.com/key4hep/k4LCIOReader/pull/18))
  - CI: use github provided docker image

* 2022-01-28 Placido Fernandez Declara ([PR#17](https://github.com/key4hep/k4LCIOReader/pull/17))
  - Change association collection to mutable to be able to `.set()`

* 2022-01-28 Valentin Volkl ([PR#16](https://github.com/key4hep/k4LCIOReader/pull/16))
  - BUILD_TESTING is a CTest builtin, no need to declare it as an option
  - use test file from key4hep www space
  - rename read_lcio exe to k4lcioreader_read-lcio - better in case it will be installed in the future
  - simple cli for the read-lcio test (filename)

* 2021-12-14 Placido Fernandez Declara ([PR#15](https://github.com/key4hep/k4LCIOReader/pull/15))
  - Add association conversion for ReconstructedParticle to Vertex
  
  Needs:
  - https://github.com/key4hep/EDM4hep/pull/133

* 2021-12-14 Thomas Madlener ([PR#14](https://github.com/key4hep/k4LCIOReader/pull/14))
  - Adapt to the new podio immutable class defaults introduced in AIDASoft/podio#205 and key4hep/EDM4hep#132.

# v00.04.00

* 2021-11-12 Placido Fernandez Declara ([PR#13](https://github.com/key4hep/k4LCIOReader/pull/13))
  - Remove `nullptr` return on `cnvAssociationCollection()` when there are no elements.
  - If no collections are found, it will return an empty `edm4hep::<something>AssociationCollection`.

* 2021-09-09 Placido Fernandez Declara ([PR#12](https://github.com/key4hep/k4LCIOReader/pull/12))
  - Adds support for TrackerHitPlane and extra associations
  - Needs EDM4hep: https://github.com/key4hep/EDM4hep/pull/122

# v00.03.02

* 2021-04-09 Placido Fernandez Declara ([PR#11](https://github.com/key4hep/k4LCIOReader/pull/11))
  - Update file handlling test

# v00.03.02

* 2021-04-09 Jiaheng Zou
  - Fixed ([issue#10](https://github.com/key4hep/k4LCIOReader/issues/10)), enable to link to objects in the same collection

# v00.03.01

* 2021-02-16 Placido Fernandez Declara ([PR#9](https://github.com/key4hep/k4LCIOReader/pull/9))
  - Exposed the LCIOConverter header to be able to use it from a different project
  - Fixed include folder not captured correctly in CMake

