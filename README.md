# api documentation for  [lab (v13.0.1)](https://github.com/hapijs/lab#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-lab.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-lab) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-lab.svg)](https://travis-ci.org/npmdoc/node-npmdoc-lab)
#### Test utility

[![NPM](https://nodei.co/npm/lab.png?downloads=true)](https://www.npmjs.com/package/lab)

[![apidoc](https://npmdoc.github.io/node-npmdoc-lab/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-lab_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-lab/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-lab/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-lab/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "lab": "./bin/lab"
    },
    "bugs": {
        "url": "https://github.com/hapijs/lab/issues"
    },
    "contributors": [
        {
            "name": "Eran Hammer",
            "email": "eran@hammer.io",
            "url": "http://hueniverse.com"
        },
        {
            "name": "Wyatt Preul",
            "email": "wpreul@gmail.com",
            "url": "http://jsgeek.com"
        }
    ],
    "dependencies": {
        "bossy": "3.x.x",
        "diff": "3.x.x",
        "eslint": "3.17.x",
        "eslint-config-hapi": "10.x.x",
        "eslint-plugin-hapi": "4.x.x",
        "espree": "3.x.x",
        "find-rc": "3.0.x",
        "handlebars": "4.x.x",
        "hoek": "4.x.x",
        "items": "2.x.x",
        "json-stable-stringify": "1.x.x",
        "json-stringify-safe": "5.x.x",
        "mkdirp": "0.5.x",
        "seedrandom": "2.4.x",
        "source-map": "0.5.x",
        "source-map-support": "0.4.x"
    },
    "description": "Test utility",
    "devDependencies": {
        "code": "4.x.x",
        "cpr": "2.0.x",
        "eslint-plugin-markdown": "1.0.0-beta.4",
        "lab-event-reporter": "1.x.x",
        "rimraf": "2.6.x"
    },
    "directories": {},
    "dist": {
        "shasum": "982e3aa382ba00911de36e928b3cedb610473f9c",
        "tarball": "https://registry.npmjs.org/lab/-/lab-13.0.1.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "gitHead": "ea0fec8861b48650840d44991e25a65047052545",
    "homepage": "https://github.com/hapijs/lab#readme",
    "keywords": [
        "test"
    ],
    "license": "BSD-3-Clause",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "hueniverse",
            "email": "eran@hueniverse.com"
        },
        {
            "name": "wyatt",
            "email": "wpreul@gmail.com"
        }
    ],
    "name": "lab",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/hapijs/lab.git"
    },
    "scripts": {
        "lint": "node ./bin/_lab -d -f -L",
        "lint-md": "eslint --config hapi --rule 'strict: 0, eol-last: 0' --plugin markdown --ext md  .",
        "posttest": "npm run lint-md",
        "test": "node ./bin/_lab -fL -t 100 -m 3000",
        "test-cov-html": "node ./bin/_lab -fL -r html -m 3000 -o coverage.html"
    },
    "version": "13.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module lab](#apidoc.module.lab)
1.  [function <span class="apidocSignatureSpan">lab.</span>execute (scripts, options, reporter, callback)](#apidoc.element.lab.execute)
1.  [function <span class="apidocSignatureSpan">lab.</span>report (scripts, options, callback)](#apidoc.element.lab.report)
1.  [function <span class="apidocSignatureSpan">lab.</span>script (options)](#apidoc.element.lab.script)
1.  object <span class="apidocSignatureSpan">lab.</span>assertions
1.  object <span class="apidocSignatureSpan">lab.</span>coverage
1.  object <span class="apidocSignatureSpan">lab.</span>leaks
1.  object <span class="apidocSignatureSpan">lab.</span>lint
1.  object <span class="apidocSignatureSpan">lab.</span>runner
1.  object <span class="apidocSignatureSpan">lab.</span>transform
1.  object <span class="apidocSignatureSpan">lab.</span>utils

#### [module lab.coverage](#apidoc.module.lab.coverage)
1.  [function <span class="apidocSignatureSpan">lab.coverage.</span>analyze (options)](#apidoc.element.lab.coverage.analyze)
1.  [function <span class="apidocSignatureSpan">lab.coverage.</span>instrument (options)](#apidoc.element.lab.coverage.instrument)

#### [module lab.leaks](#apidoc.module.lab.leaks)
1.  [function <span class="apidocSignatureSpan">lab.leaks.</span>detect (customGlobals)](#apidoc.element.lab.leaks.detect)

#### [module lab.lint](#apidoc.module.lab.lint)
1.  [function <span class="apidocSignatureSpan">lab.</span>lint (settings, callback)](#apidoc.element.lab.lint.lint)

#### [module lab.runner](#apidoc.module.lab.runner)
1.  [function <span class="apidocSignatureSpan">lab.runner.</span>execute (scripts, options, reporter, callback)](#apidoc.element.lab.runner.execute)
1.  [function <span class="apidocSignatureSpan">lab.runner.</span>report (scripts, options, callback)](#apidoc.element.lab.runner.report)

#### [module lab.transform](#apidoc.module.lab.transform)
1.  [function <span class="apidocSignatureSpan">lab.</span>transform (filename, content)](#apidoc.element.lab.transform.transform)
1.  [function <span class="apidocSignatureSpan">lab.transform.</span>install (settings, primeFn)](#apidoc.element.lab.transform.install)
1.  [function <span class="apidocSignatureSpan">lab.transform.</span>retrieveFile (path)](#apidoc.element.lab.transform.retrieveFile)

#### [module lab.utils](#apidoc.module.lab.utils)
1.  [function <span class="apidocSignatureSpan">lab.utils.</span>applyOptions (parent, child)](#apidoc.element.lab.utils.applyOptions)
1.  [function <span class="apidocSignatureSpan">lab.utils.</span>mergeOptions (parent, child, ignore)](#apidoc.element.lab.utils.mergeOptions)



# <a name="apidoc.module.lab"></a>[module lab](#apidoc.module.lab)

#### <a name="apidoc.element.lab.execute"></a>[function <span class="apidocSignatureSpan">lab.</span>execute (scripts, options, reporter, callback)](#apidoc.element.lab.execute)
- description and source-code
```javascript
execute = function (scripts, options, reporter, callback) {

    const settings = Utils.mergeOptions(internals.defaults, options);

    scripts = [].concat(scripts);

    if (settings.shuffle) {
        internals.shuffle(scripts, settings.seed);
    }

    const experiments = scripts.map((script) => {

        script._executed = true;
        return script._root;
    });

    const onlyNodes = Hoek.flatten(scripts.map((script) => script._onlyNodes));
    if (onlyNodes.length > 1) {
        const paths = onlyNodes.map((onlyNode) => {

            if (onlyNode.test) {
                return 'Test: ${onlyNode.test.title}';
            }
            return 'Experiment: ${onlyNode.path}';
        });
        return callback(new Error('Multiple tests are marked as "only":\n\t' + paths.join('\n\t')));
    }

    const onlyNode = onlyNodes[0];
    if (onlyNode) {
        internals.skipAllButOnly(scripts, onlyNode);
    }

    reporter = reporter || { test: function () { }, start: function () { } };

    if (settings.environment) {
        process.env.NODE_ENV = settings.environment;
    }

    const filters = {
        ids: settings.ids,
        grep: settings.grep ? new RegExp(settings.grep) : null
    };

    const count = internals.count(experiments, { filters });        // Sets test.id
    reporter.start({ count });

    const startTime = Date.now();
    const state = {
        report: {
            tests: [],
            failures: 0,
            errors: []
        },
        reporter,
        filters,
        options: settings,
        only: onlyNode
    };

    // Instantiate common lazily loaded items that can leak domains.
    internals.loadLazyObjects();

    internals.executeExperiments(experiments, state, settings.dry, () => {

        const notebook = {
            ms: Date.now() - startTime,
            tests: state.report.tests,
            failures: state.report.failures,
            errors: state.report.errors
        };

        return callback(null, notebook);
    });
}
```
- example usage
```shell
...

    const settings = Utils.mergeOptions(internals.defaults, options);
    settings.environment = settings.environment.trim();
    const reporter = Reporters.generate(settings);

    const executeScripts = function (next) {

exports.execute(scripts, settings, reporter, (err, result) => {
    // Can only be (and is) covererd via CLI tests
    /* $lab:coverage:off$ */
    if (err) {
        const outputStream = [].concat(options.output).find((output) => !!output.write);
        if (outputStream) {
            outputStream.write(err.toString() + '\n');
        }
...
```

#### <a name="apidoc.element.lab.report"></a>[function <span class="apidocSignatureSpan">lab.</span>report (scripts, options, callback)](#apidoc.element.lab.report)
- description and source-code
```javascript
report = function (scripts, options, callback) {

    const settings = Utils.mergeOptions(internals.defaults, options);
    settings.environment = settings.environment.trim();
    const reporter = Reporters.generate(settings);

    const executeScripts = function (next) {

        exports.execute(scripts, settings, reporter, (err, result) => {
            // Can only be (and is) covererd via CLI tests
<span class="apidocCodeCommentSpan">            /* $lab:coverage:off$ */
</span>            if (err) {
                const outputStream = [].concat(options.output).find((output) => !!output.write);
                if (outputStream) {
                    outputStream.write(err.toString() + '\n');
                }
                else {
                    console.error(err.toString());
                }
                return process.exit(1);
            }
            /* $lab:coverage:on$ */

            if (settings.leaks) {
                result.leaks = Leaks.detect(settings.globals);
            }

            if (settings.coverage) {
                result.coverage = Coverage.analyze(settings);
            }

            if (settings.shuffle) {
                result.seed = settings.seed;
                result.shuffle = true;
            }

            return next(null, result);
        });
    };

    const executeLint = function (next) {

        if (!settings.lint) {
            return next();
        }

        Linters.lint(settings, next);
    };

    Items.parallel.execute({ notebook: executeScripts, lint: executeLint }, (ignoreErr, results) => {

        const notebook = results.notebook;
        notebook.lint = results.lint;

        if (settings.assert) {
            notebook.assertions = settings.assert.count && settings.assert.count();
            const incompletes = settings.assert.incomplete && settings.assert.incomplete();
            if (incompletes) {
                for (let i = 0; i < incompletes.length; ++i) {
                    const error = new Error('Incomplete assertion at ' + incompletes[i]);
                    error.stack = undefined;
                    notebook.errors.push(error);
                }
            }
        }

        return reporter.finalize(notebook, callback);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lab.script"></a>[function <span class="apidocSignatureSpan">lab.</span>script (options)](#apidoc.element.lab.script)
- description and source-code
```javascript
script = function (options) {

    options = options || {};

    global._labScriptRun = true;                                        // Compared by CLI to detect missing exports.lab

    const script = {
        _current: {
            experiments: [],
            tests: [],
            options: {},
            title: 'script'
        },
        _titles: [],
        _path: [],
        _count: 0,
        _executed: false,
        _onlyNodes: [],
        _cli: options.cli,
        setOnly: function (experiment, test, path) {

            this._onlyNodes.push({ experiment, test, path });
        }
    };

    script._root = script._current;

    script.experiment = internals.experiment.bind(script);
    script.experiment.skip = internals.skip(script, 'experiment');
    script.experiment.only = internals.only(script, 'experiment');
    script.describe = script.experiment;
    script.suite = script.experiment;

    script.test = internals.test.bind(script);
    script.test.skip = internals.skip(script, 'test');
    script.test.only = internals.only(script, 'test');
    script.it = script.test;

    script.before = internals.before.bind(script);
    script.beforeEach = internals.beforeEach.bind(script);
    script.after = internals.after.bind(script);
    script.afterEach = internals.afterEach.bind(script);

    if (options.schedule !== false) {                   // Defaults to true
        setImmediate(() => {

            if (!script._executed) {
                Runner.report(script, options);         // Schedule automatic execution when used without the CLI
            }
        });
    }

    return script;
}
```
- example usage
```shell
...
$ lab unit.js
'''

Test files must require the **lab** module, and export a test script:
'''javascript
const Code = require('code');   // assertion library
const Lab = require('lab');
const lab = exports.lab = Lab.script();

lab.test('returns true when 1 + 1 equals 2', (done) => {

    Code.expect(1 + 1).to.equal(2);
    done();
});
'''
...
```



# <a name="apidoc.module.lab.coverage"></a>[module lab.coverage](#apidoc.module.lab.coverage)

#### <a name="apidoc.element.lab.coverage.analyze"></a>[function <span class="apidocSignatureSpan">lab.coverage.</span>analyze (options)](#apidoc.element.lab.coverage.analyze)
- description and source-code
```javascript
analyze = function (options) {

    // Process coverage  (global.__$$labCov needed when labCov isn't defined)

<span class="apidocCodeCommentSpan">    /* $lab:coverage:off$ */ const report = global.__$$labCov || { files: {} }; /* $lab:coverage:on$ */
</span>    const pattern = internals.pattern(options);

    const cov = {
        sloc: 0,
        hits: 0,
        misses: 0,
        percent: 0,
        files: []
    };

    // Filter files

    const files = Object.keys(report.files);
    for (let i = 0; i < files.length; ++i) {
        const filename = files[i];
        if (pattern.test(filename)) {
            report.files[filename].source = internals.sources[filename] || [];
            const data = internals.file(filename, report.files[filename], options);

            cov.files.push(data);
            cov.hits += data.hits;
            cov.misses += data.misses;
            cov.sloc += data.sloc;
        }
    }

    // Sort files based on directory structure

    cov.files.sort((a, b) => {

        const segmentsA = a.filename.split('/');
        const segmentsB = b.filename.split('/');

        const al = segmentsA.length;
        const bl = segmentsB.length;

        for (let i = 0; i < al && i < bl; ++i) {

            if (segmentsA[i] === segmentsB[i]) {
                continue;
            }

            const lastA = i + 1 === al;
            const lastB = i + 1 === bl;

            if (lastA !== lastB) {
                return lastA ? -1 : 1;
            }

            return segmentsA[i] < segmentsB[i] ? -1 : 1;
        }

        return segmentsA.length < segmentsB.length ? -1 : 1;
    });

    // Calculate coverage percentage

    if (cov.sloc > 0) {
        cov.percent = (cov.hits / cov.sloc) * 100;
    }

    return cov;
}
```
- example usage
```shell
...
/* $lab:coverage:on$ */

if (settings.leaks) {
    result.leaks = Leaks.detect(settings.globals);
}

if (settings.coverage) {
    result.coverage = Coverage.analyze(settings);
}

if (settings.shuffle) {
    result.seed = settings.seed;
    result.shuffle = true;
}
...
```

#### <a name="apidoc.element.lab.coverage.instrument"></a>[function <span class="apidocSignatureSpan">lab.coverage.</span>instrument (options)](#apidoc.element.lab.coverage.instrument)
- description and source-code
```javascript
instrument = function (options) {

    internals.patterns.unshift(internals.pattern(options));

    Transform.install(options, internals.prime);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lab.leaks"></a>[module lab.leaks](#apidoc.module.lab.leaks)

#### <a name="apidoc.element.lab.leaks.detect"></a>[function <span class="apidocSignatureSpan">lab.leaks.</span>detect (customGlobals)](#apidoc.element.lab.leaks.detect)
- description and source-code
```javascript
detect = function (customGlobals) {

    const whitelist = {
        _labScriptRun: true,                // Lab global to detect script executions

        // Enumerable globals
        setTimeout: true,
        setInterval: true,
        setImmediate: true,
        clearTimeout: true,
        clearInterval: true,
        clearImmediate: true,
        console: true,
        Buffer: true,
        process: true,
        global: true,
        GLOBAL: true,
        root: true,
        constructor: true,
        ArrayBuffer: true,
        Int8Array: true,
        Uint8Array: true,
        Uint8ClampedArray: true,
        Int16Array: true,
        Uint16Array: true,
        Int32Array: true,
        Uint32Array: true,
        Float32Array: true,
        Float64Array: true,
        DataView: true,
        __$$labCov: true,
        gc: true,

        // Non-Enumerable globals
        Array: true,
        isNaN: true,
        ReferenceError: true,
        Number: true,
        RangeError: true,
        EvalError: true,
        Function: true,
        isFinite: true,
        Object: true,
        undefined: true,
        Date: true,
        SyntaxError: true,
        String: true,
        eval: true,
        parseFloat: true,
        unescape: true,
        Error: true,
        encodeURI: true,
        NaN: true,
        RegExp: true,
        encodeURIComponent: true,
        Math: true,
        decodeURI: true,
        parseInt: true,
        Infinity: true,
        escape: true,
        decodeURIComponent: true,
        JSON: true,
        TypeError: true,
        URIError: true,
        Boolean: true,
        Intl: true,
        Map: true,
        Promise: true,
        Set: true,
        Symbol: true,
        WeakMap: true,
        WeakSet: true
    };

    if (customGlobals) {
        for (let i = 0; i < customGlobals.length; ++i) {
            whitelist[customGlobals[i]] = true;
        }
    }

    if (global.Proxy) {
        whitelist.Proxy = true;
    }

    if (global.Reflect) {
        whitelist.Reflect = true;
    }

    if (global.DTRACE_HTTP_SERVER_RESPONSE) {
        whitelist.DTRACE_HTTP_SERVER_RESPONSE = true;
        whitelist.DTRACE_HTTP_SERVER_REQUEST = true;
        whitelist.DTRACE_HTTP_CLIENT_RESPONSE = true;
        whitelist.DTRACE_HTTP_CLIENT_REQUEST = true;
        whitelist.DTRACE_NET_STREAM_END = true;
        whitelist.DTRACE_NET_SERVER_CONNECTION = true;
        whitelist.DTRACE_NET_SOCKET_READ = true;
        whitelist.DTRACE_NET_SOCKET_WRITE = true;
    }

    if (global.COUNTER_NET_SERVER_CONNECTION) {
        whitelist.COUNTER_NET_SERVER_CONNECTION = true;
        whitelist.COUNTER_NET_SERVER_CONNECTION_CLOSE = true;
        whitelist.COUNTER_HTTP_SERVER_REQUEST = true;
        whitelist.COUNTER_HTTP_SERVER_RESPONSE = true;
        whitelist.COUNTER_HTTP_CLIENT_REQUEST = true;
        whitelist.COUNTER_HTTP_CLIENT_RESPONSE = true;
    }

    const leaks = [];
    const globals = Object.getOwnPropertyNames(global);
    for (let i = 0; i < globals.length; ++i) {
        if (!whitelist[globals[i]] &&
            global[globals[i]] !== global) {

            leaks.push(globals[i]);
        }
    }

    return leaks;
}
```
- example usage
```shell
...
        console.error(err.toString());
    }
    return process.exit(1);
}
/* $lab:coverage:on$ */

if (settings.leaks) {
    result.leaks = Leaks.detect(settings.globals);
}

if (settings.coverage) {
    result.coverage = Coverage.analyze(settings);
}

if (settings.shuffle) {
...
```



# <a name="apidoc.module.lab.lint"></a>[module lab.lint](#apidoc.module.lab.lint)

#### <a name="apidoc.element.lab.lint.lint"></a>[function <span class="apidocSignatureSpan">lab.</span>lint (settings, callback)](#apidoc.element.lab.lint.lint)
- description and source-code
```javascript
lint = function (settings, callback) {

    const linterPath = (settings.linter && settings.linter !== 'eslint') ? settings.linter : internals.linter;

    let linterOptions;

    try {
        linterOptions = JSON.parse(settings['lint-options'] || '{}');
    }
    catch (err) {
        throw new Error('lint-options could not be parsed');
    }

    linterOptions.fix = settings['lint-fix'];

    const child = ChildProcess.fork(linterPath, [JSON.stringify(linterOptions)], { cwd: settings.lintingPath });
    child.once('message', (message) => {

        child.kill();

        const result = { lint: message, totalErrors: 0, totalWarnings: 0 };

        result.lint.forEach((lint) => {

            let errors = 0;
            let warnings = 0;

            lint.errors.forEach((err) => {

                if (err.severity === 'ERROR') {
                    errors++;
                }
                else {
                    warnings++;
                }
            });

            lint.totalErrors = errors;
            lint.totalWarnings = warnings;
            result.totalErrors += errors;
            result.totalWarnings += warnings;

            if (lint.fix) {
                Fs.writeFileSync(lint.filename, lint.fix.output);
            }
        });

        result.total = result.totalErrors + result.totalWarnings;

        return callback(null, result);
    });
}
```
- example usage
```shell
...

    const executeLint = function (next) {

if (!settings.lint) {
    return next();
}

Linters.lint(settings, next);
    };

    Items.parallel.execute({ notebook: executeScripts, lint: executeLint }, (ignoreErr, results) => {

const notebook = results.notebook;
notebook.lint = results.lint;
...
```



# <a name="apidoc.module.lab.runner"></a>[module lab.runner](#apidoc.module.lab.runner)

#### <a name="apidoc.element.lab.runner.execute"></a>[function <span class="apidocSignatureSpan">lab.runner.</span>execute (scripts, options, reporter, callback)](#apidoc.element.lab.runner.execute)
- description and source-code
```javascript
execute = function (scripts, options, reporter, callback) {

    const settings = Utils.mergeOptions(internals.defaults, options);

    scripts = [].concat(scripts);

    if (settings.shuffle) {
        internals.shuffle(scripts, settings.seed);
    }

    const experiments = scripts.map((script) => {

        script._executed = true;
        return script._root;
    });

    const onlyNodes = Hoek.flatten(scripts.map((script) => script._onlyNodes));
    if (onlyNodes.length > 1) {
        const paths = onlyNodes.map((onlyNode) => {

            if (onlyNode.test) {
                return 'Test: ${onlyNode.test.title}';
            }
            return 'Experiment: ${onlyNode.path}';
        });
        return callback(new Error('Multiple tests are marked as "only":\n\t' + paths.join('\n\t')));
    }

    const onlyNode = onlyNodes[0];
    if (onlyNode) {
        internals.skipAllButOnly(scripts, onlyNode);
    }

    reporter = reporter || { test: function () { }, start: function () { } };

    if (settings.environment) {
        process.env.NODE_ENV = settings.environment;
    }

    const filters = {
        ids: settings.ids,
        grep: settings.grep ? new RegExp(settings.grep) : null
    };

    const count = internals.count(experiments, { filters });        // Sets test.id
    reporter.start({ count });

    const startTime = Date.now();
    const state = {
        report: {
            tests: [],
            failures: 0,
            errors: []
        },
        reporter,
        filters,
        options: settings,
        only: onlyNode
    };

    // Instantiate common lazily loaded items that can leak domains.
    internals.loadLazyObjects();

    internals.executeExperiments(experiments, state, settings.dry, () => {

        const notebook = {
            ms: Date.now() - startTime,
            tests: state.report.tests,
            failures: state.report.failures,
            errors: state.report.errors
        };

        return callback(null, notebook);
    });
}
```
- example usage
```shell
...

    const settings = Utils.mergeOptions(internals.defaults, options);
    settings.environment = settings.environment.trim();
    const reporter = Reporters.generate(settings);

    const executeScripts = function (next) {

exports.execute(scripts, settings, reporter, (err, result) => {
    // Can only be (and is) covererd via CLI tests
    /* $lab:coverage:off$ */
    if (err) {
        const outputStream = [].concat(options.output).find((output) => !!output.write);
        if (outputStream) {
            outputStream.write(err.toString() + '\n');
        }
...
```

#### <a name="apidoc.element.lab.runner.report"></a>[function <span class="apidocSignatureSpan">lab.runner.</span>report (scripts, options, callback)](#apidoc.element.lab.runner.report)
- description and source-code
```javascript
report = function (scripts, options, callback) {

    const settings = Utils.mergeOptions(internals.defaults, options);
    settings.environment = settings.environment.trim();
    const reporter = Reporters.generate(settings);

    const executeScripts = function (next) {

        exports.execute(scripts, settings, reporter, (err, result) => {
            // Can only be (and is) covererd via CLI tests
<span class="apidocCodeCommentSpan">            /* $lab:coverage:off$ */
</span>            if (err) {
                const outputStream = [].concat(options.output).find((output) => !!output.write);
                if (outputStream) {
                    outputStream.write(err.toString() + '\n');
                }
                else {
                    console.error(err.toString());
                }
                return process.exit(1);
            }
            /* $lab:coverage:on$ */

            if (settings.leaks) {
                result.leaks = Leaks.detect(settings.globals);
            }

            if (settings.coverage) {
                result.coverage = Coverage.analyze(settings);
            }

            if (settings.shuffle) {
                result.seed = settings.seed;
                result.shuffle = true;
            }

            return next(null, result);
        });
    };

    const executeLint = function (next) {

        if (!settings.lint) {
            return next();
        }

        Linters.lint(settings, next);
    };

    Items.parallel.execute({ notebook: executeScripts, lint: executeLint }, (ignoreErr, results) => {

        const notebook = results.notebook;
        notebook.lint = results.lint;

        if (settings.assert) {
            notebook.assertions = settings.assert.count && settings.assert.count();
            const incompletes = settings.assert.incomplete && settings.assert.incomplete();
            if (incompletes) {
                for (let i = 0; i < incompletes.length; ++i) {
                    const error = new Error('Incomplete assertion at ' + incompletes[i]);
                    error.stack = undefined;
                    notebook.errors.push(error);
                }
            }
        }

        return reporter.finalize(notebook, callback);
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lab.transform"></a>[module lab.transform](#apidoc.module.lab.transform)

#### <a name="apidoc.element.lab.transform.transform"></a>[function <span class="apidocSignatureSpan">lab.</span>transform (filename, content)](#apidoc.element.lab.transform.transform)
- description and source-code
```javascript
transform = function (filename, content) {

    let ext = '';
    let transform = null;

    internals.transforms.forEach((element) => {

        ext = element.ext;
        if (filename.indexOf(ext, filename.length - ext.length) !== -1) {
            transform = element.transform;
        }
    });

    const relativeFilename = filename.substr(process.cwd().length + 1);
    internals.fileCache[relativeFilename] = (typeof transform === 'function') ? transform(content, relativeFilename) : content;
    return internals.fileCache[relativeFilename];
}
```
- example usage
```shell
...
const Btoa = require('btoa');

module.exports = [
{ ext: '.js', transform: (content, filename) => {

    // Make sure to only transform your code or the dependencies you want
    if (filename.indexOf('node_modules') === -1) {
        const result = Babel.transform(content, { sourceMap: 'inline', filename, sourceFileName: filename });
        return result.code;
    }

    return content;
} },
{ ext: '.coffee', transform: (content, filename) => {
...
```

#### <a name="apidoc.element.lab.transform.install"></a>[function <span class="apidocSignatureSpan">lab.transform.</span>install (settings, primeFn)](#apidoc.element.lab.transform.install)
- description and source-code
```javascript
install = function (settings, primeFn) {

    if (Array.isArray(settings.transform)) {
        settings.transform.forEach((element) => {

            if (element.ext === '.js') {
                internals.transforms[0].transform = element.transform;
            }
            else {
                internals.transforms.push(element);
            }
        });
    }

    if (typeof primeFn !== 'function') {
        primeFn = internals.prime;
    }

    internals.transforms.forEach((transform) => {

        primeFn(transform.ext);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lab.transform.retrieveFile"></a>[function <span class="apidocSignatureSpan">lab.transform.</span>retrieveFile (path)](#apidoc.element.lab.transform.retrieveFile)
- description and source-code
```javascript
retrieveFile = function (path) {

    const cwd = process.cwd();
    const cacheKey = path.indexOf(cwd) === 0 ? path.substr(cwd.length + 1) : path;
    if (internals.fileCache[cacheKey]) {
        return internals.fileCache[cacheKey];
    }

    let contents = null;
    try {
        contents = Fs.readFileSync(path, 'utf8');
    }
    catch (e) {
        contents = null;
    }

    internals.fileCache[path] = contents;

    return contents;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.lab.utils"></a>[module lab.utils](#apidoc.module.lab.utils)

#### <a name="apidoc.element.lab.utils.applyOptions"></a>[function <span class="apidocSignatureSpan">lab.utils.</span>applyOptions (parent, child)](#apidoc.element.lab.utils.applyOptions)
- description and source-code
```javascript
applyOptions = function (parent, child) {

    Object.keys(child).forEach((key) => {

        parent[key] = child[key];
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.lab.utils.mergeOptions"></a>[function <span class="apidocSignatureSpan">lab.utils.</span>mergeOptions (parent, child, ignore)](#apidoc.element.lab.utils.mergeOptions)
- description and source-code
```javascript
mergeOptions = function (parent, child, ignore) {

    ignore = ignore || [];
    const options = {};

    Object.keys(parent || {}).forEach((key) => {

        if (ignore.indexOf(key) === -1) {
            options[key] = parent[key];
        }
    });

    Object.keys(child || {}).forEach((key) => {

        options[key] = child[key];
    });

    return options;
}
```
- example usage
```shell
...
    'lint-errors-threshold': 0,
    'lint-warnings-threshold': 0
};


exports.report = function (scripts, options, callback) {

    const settings = Utils.mergeOptions(internals.defaults, options);
    settings.environment = settings.environment.trim();
    const reporter = Reporters.generate(settings);

    const executeScripts = function (next) {

exports.execute(scripts, settings, reporter, (err, result) => {
    // Can only be (and is) covererd via CLI tests
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
