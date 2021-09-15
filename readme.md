This repository demonstrates the issue of `@wordpress/scripts` being unable to resolve `prettier@npm:wp-prettier@2.2.1-beta-1`, see [github.com/WordPress/gutenberg/issues/21872](https://github.com/WordPress/gutenberg/issues/21872).

During `npm install` it reports the following:

    npm WARN eslint-plugin-prettier@3.4.1 requires a peer of prettier@>=1.13.0 but none is installed. You must install peer dependencies yourself.

while runnig `npm ls prettier` reports:
                
    /path/to/project-directory
    └─┬ @wordpress/scripts@18.0.1
    ├─┬ @wordpress/eslint-plugin@9.1.2
    │ └── UNMET PEER DEPENDENCY prettier@npm:wp-prettier@2.2.1-beta-1 
    └── prettier@npm:wp-prettier@2.2.1-beta-1 

    npm ERR! peer dep missing: prettier@>=1.13.0, required by eslint-plugin-prettier@3.4.1


## Test Report

See the [`reports`](reports) directory for a list of outputs with lock files generated by different versions of Node used by different versions of Node.

- [Without a lock file](https://github.com/xwp/gutenberg-issue-21872-scripts/actions/runs/1238995537)
- [Lock file from Node v12.22.1 (npm v6.14.12)](https://github.com/xwp/gutenberg-issue-21872-scripts/actions/runs/1239000476)
- [Lock file from Node v14.17.6 (npm v6.14.15)](https://github.com/xwp/gutenberg-issue-21872-scripts/actions/runs/1239101141)
- [Lock file from Node v15.14.0 (npm v7.7.6)](https://github.com/xwp/gutenberg-issue-21872-scripts/actions/runs/1239049477)
- [Lock file from Node v16.9.1 (npm v7.21.1)](https://github.com/xwp/gutenberg-issue-21872-scripts/actions/runs/1239016832)