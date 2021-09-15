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