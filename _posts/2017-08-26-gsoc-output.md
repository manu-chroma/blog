---
layout: post
title:  "Google Summer of Code 2017: Final Report"
categories: GSoC '17
published: true
---

**This report was initially published as [a GitHub gist](https://gist.github.com/manu-chroma/8e10ea9fd728356a4363b5af1f0d8aaa)**

Hey everyone! I'm Manvendra, a Google Summer of Code '17 student developer. This summer, I worked on [Common Workflow Language Project](github.com/common-workflow-language/) which comes under [OBF Org](https://www.open-bio.org/wiki/Main_Page). This is a summary report on what I managed to do in the past three months. 

My major deliverables were:
- Adding Python 3 compatibility to [CWL Tool](https://github.com/common-workflow-language/cwltool), [Schema Salad](https://github.com/common-workflow-language/schema_salad) and [CWL Test](https://github.com/common-workflow-language/cwltest) projects.
- Improving [mypy](http://mypy-lang.org/) annotations and upgrading mypy dependency for CWL Tool and Schema Salad. 
- Reducing issue backlog and misc enhancements.

It was a great experience and I got to learn a lot about python, mypy, debugging effectively and several libraries (both standard and third-party) and a lot of other things. I was the highest committer in Schema Salad and CWL Tool from the start of my coding period i.e. end of April to mid-August: [commit](https://github.com/common-workflow-language/cwltool/graphs/contributors?from=2017-05-30&to=2017-08-17&type=c) [graph](https://github.com/common-workflow-language/schema_salad/graphs/contributors?from=2017-05-05&to=2017-08-17&type=c), [commits to](https://github.com/common-workflow-language/cwltool/commits/master?author=manu-chroma) [master](https://github.com/common-workflow-language/schema_salad/commits/master?author=manu-chroma) 

## List of PR's

Here's a list of my PR's which got merged during the coding period.

- ### CWL Tool

| Link to PR                                                           |  Description                                                                      | 
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------| 
| [#523](https://github.com/common-workflow-language/cwltool/pull/523) |  Fix linting and minor errors in README                                             | 
| [#519](https://github.com/common-workflow-language/cwltool/pull/519) |  README: Add more verbose instructions to install from source                     | 
| [#512](https://github.com/common-workflow-language/cwltool/pull/512) |  cwlrdf.py: Pass str rather than bytes to write function           | 
| [#509](https://github.com/common-workflow-language/cwltool/pull/509) |  load_tool.py: Pass to regex before checking for acceptable versions              | 
| [#505](https://github.com/common-workflow-language/cwltool/pull/505) |  Add support for Python 3 conformance testing on Jenkins CI                       | 
| [#497](https://github.com/common-workflow-language/cwltool/pull/497) |  pack.py: add `cwlVersion` in pack dict, if only single item exists in $graph     | 
| [#496](https://github.com/common-workflow-language/cwltool/pull/496) |  Pass group id (GID) in `--user` flag when calling docker run                 | 
| [#494](https://github.com/common-workflow-language/cwltool/pull/494) |  sandboxjs.py: Fix check condition for downloading node:slim pull                          | 
| [#491](https://github.com/common-workflow-language/cwltool/pull/491) |  load_tool: If no version or incorrect of `cwlVersion` is found, throw fatal error | 
| [#477](https://github.com/common-workflow-language/cwltool/pull/477) |  setup.py: Remove condition which blocks python 3 install                         | 
| [#476](https://github.com/common-workflow-language/cwltool/pull/476) |  Use io.open instead of builtin open                      | 
| [#470](https://github.com/common-workflow-language/cwltool/pull/470) |  tox.ini: Remove redundant unit tests code blocks command                                      | 
| [#464](https://github.com/common-workflow-language/cwltool/pull/464) |  Turn on Python 3 on travis CI                                                    | 
| [#461](https://github.com/common-workflow-language/cwltool/pull/461) |  Upgrade mypy to v.520                                                            | 
| [#460](https://github.com/common-workflow-language/cwltool/pull/460) |  mypy: Don't silence schema_salad errors                                          | 
| [#450](https://github.com/common-workflow-language/cwltool/pull/450) |  setup.py: Pin ruamel.yaml package version                                        | 
| [#442](https://github.com/common-workflow-language/cwltool/pull/442) |  **Mega PR** for Python3 compatibility                              | 
| [#423](https://github.com/common-workflow-language/cwltool/pull/423) |  Updates to mypy                                                                  | 
| [#407](https://github.com/common-workflow-language/cwltool/pull/407) |  Sorting python imports using isort                                               | 
| [#406](https://github.com/common-workflow-language/cwltool/pull/406) |  requirements.txt: Use same version of rdflib as in setup.py and schema_salad     | 
| [#393](https://github.com/common-workflow-language/cwltool/pull/393) |  Prevent python3-pip installation until py3 is supported                    | 
| [#383](https://github.com/common-workflow-language/cwltool/pull/383) |  Added ISSUE_TEMPLATE.md                                                          | 
| [#337](https://github.com/common-workflow-language/cwltool/pull/337) |  sandboxjs.py: Check for valid version of node/nodejs engine                      | 

- ### Schema Salad

| Link to PR                                                        |  Description                                                             | 
|-------------------------------------------------------------------|--------------------------------------------------------------------------| 
| [#128](https://github.com/common-workflow-language/schema_salad/pull/128) |  Bump version of `avro` for Python 3                             | 
| [#125](https://github.com/common-workflow-language/schema_salad/pull/125) |  Fix windows installation error due to absence of `\tmp` folder  | 
| [#123](https://github.com/common-workflow-language/schema_salad/pull/123) |  Integrate avro fork in Python 3 installation                    |
| [#122](https://github.com/common-workflow-language/schema_salad/pull/122) |  Use io.open instead of builtin open                             | 
| [#121](https://github.com/common-workflow-language/schema_salad/pull/121) |  Update mypy to 0.520                                            |
| [#118](https://github.com/common-workflow-language/schema_salad/pull/118) |  Pin `ruamel.yaml` dependency                                    | 
| [#116](https://github.com/common-workflow-language/schema_salad/pull/116) |  requirements.txt: Add mypy, typed-ast packages, use in tox and Makefile | 
| [#114](https://github.com/common-workflow-language/schema_salad/pull/114) |  Minor refactor: Create utils.py                                 | 
| [#109](https://github.com/common-workflow-language/schema_salad/pull/109) |  **Mega PR** for Python 3 compatibility                              | 


- ### CWL Test

| Link to PR                                                  | Description                                                                     | 
|-------------------------------------------------------------|---------------------------------------------------------------------------------| 
| [#20](https://github.com/common-workflow-language/cwltest/pull/20) | Add Python 3 support                                                     | 
| [#33](https://github.com/common-workflow-language/cwltest/pull/33) | Add `classname` category to specify Python run time version in XML output file| 


- ### Some fun stats

``` bash 
git log --author="Manvendra Singh" --oneline --shortstat
```

| Repo         |     LOC++ |  LOC-- | 
|--------------|------------|---------| 
| cwltool      |     6,731  |  9,469  | 
| schema_salad |     1,965  |  3,158  | 
| cwltest      |     34     |  20     | 

**Total LOC:** ``8370++``, ``12647--`` 


## Work done 


<!-- <center> --><!-- 
![img](http://imgur.com/aZpTrSt.png)
</center> -->

### Phase 1: 7 weeks

- Made Schema Salad code Python 3 compatible and fixed mypy annotations. The majority of the changes were made in [this Mega PR.](https://github.com/common-workflow-language/schema_salad/pull/109)
- Worked on CWL Py3 compatibility: Again majority of the changes came in [a Mega PR](https://github.com/common-workflow-language/cwltool/pull/442) 
- Fixed mypy annotations and upgraded to ``v.511``
- Ran mypy in Python 3 mode without any errors. This required adding compatible stub files.
- Dealt with [Apache Avro issues](https://github.com/common-workflow-language/cwltool/issues/524)
- Fixed failing unit tests
- Fixed failing conformance tests
- Added Py3 compatibility to CWL Test

### Phase 2: 4 weeks 

I tracked my _Phase 2_ progress using [Manvendra's Issue Tracker](https://github.com/orgs/common-workflow-language/projects/3?fullscreen=true). This included addressing very specific issues and enhancements: 

- Better errors for invalid ``cwlVersion``
- Fix ``node:slim`` check and download condition
- Update Jenkins script to add Python 3 conformance testing
- Fix Windows installation error
- Fix packed workflow bug related to ``cwlVersion``
- Add classname field in XML output report when running CWL Test
- README: Improve installation instructions and formatting
- Deprecate CWL ``draft 2,3,4`` support on CWL Tool

### Challenges

Some of the major challenges along the way:

- CWL User guide is rich but the codebase is relatively less documented. A major challenge was to figure a lot of stuff  myself and how a lot of code is interacting. [Michael](https://github.com/mr-c) was quite helpful and very responsive to queries. Going through testing code also helped.
- Strings needed to be handled correctly: differentiating between binary strings and ASCII/Unicode strings. Discussed this issue in two of the weekly posts: [1](https://manu-chroma.github.io/blog/gsoc/'17/2017/06/19/week-3.html), [2](https://manu-chroma.github.io/blog/gsoc/'17/2017/07/03/week-5.html)  
- Dependency upgrade: Getting Apache Avro working under Python 3 runtime turned out to be a big challenge: [issues/524](https://github.com/common-workflow-language/cwltool/issues/524)
- Fixing failing conformance was also a challenge, but an interesting one. Even though conformance tests cover less than half codebase of what unit tests do, they helped uncover a lot of subtle and integration testing bugs while porting.

## Future Work

I've a few Work In Progress PR's currently which I plan to complete. 

- Add contributing guide for CWL Tool
PR: [#508](https://github.com/common-workflow-language/cwltool/pull/508)
- Config coveralls to measure code coverage diff on PR's
PR: [#526](https://github.com/common-workflow-language/cwltool/pull/526)
- Deprecate previous drafts
PR: [#520](https://github.com/common-workflow-language/cwltool/pull/520)
- Fix Makefile target for conformance code coverage
Related issue: [#334](https://github.com/common-workflow-language/cwltool/issues/334)

## Acknowledgement

I would like to thank a bunch of people for helping me throughout my journey. One of the best part of open source dev is to see other people willingly help each other out and collaborate to create amazing software. I'd like to thank my mentors [Michael Crusoe](https://github.com/mr-c), [Anton Khodak](https://github.com/anton_khodak) and [Janneke van der Zwaan](https://github.com/jvdzwaan). My interaction and collaboration with my mentors was great throughout. It was a big reason why I sticked well to the timeline and was able to keep up my progress.
Special thanks to Michael. He was very responsive and helpful all along. He ended up giving useful insights throughout whenever I was stuck or something which I could have done better.  

I would also like to thank [Alexandr](https://github.com/AleksandrSl) who helped me in mypy debugging and wrote a few stub files, [Kapil](https://github.com/kapilkd13) who reviewed some of my code and I reviewed his, [Petr](https://github.com/tetron) for hanging around and giving ocassional advice. A big shout out to the entire CWL and mypy community: both of them were super active on Gitter and offered some very helpful advice on porting and mypy debugging.

I was able to sucessfully deliver my project objectives and thus, would consider it a successful summer work. I hope my work has postive impact on current and potential users of CWL Tool. 