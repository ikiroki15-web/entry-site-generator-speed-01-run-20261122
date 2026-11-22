# Fast makefun-site

A faster drop-in for makefun-site 1.0.0 (site-generator-speed-01): `solve.js` is a dependency-free ES
module whose `run(input)` returns the same output tree as makefun-site's build for every input, and
`main.ts` is the driver the harness runs (reads `/input/cases.json`, writes `/output/answers.json`).

The build mirrors makefun-site's pipeline (sources, front matter, permalinks, Markdown, collections,
tags, layouts, report) with single-pass scanners, bulk HTML escaping and templates compiled to
functions. Nothing is cached between cases.

https://make.fun
