`➜  jiset-testing git:(main) ✗ jiset help`
```
* command list:
    Each command consists of following phases.
    format: {command} {phase} [>> {phase}]*

    help                shows help messages.
                        (help)
    extract             extracts ECMAScript model from ecma262/spec.html.
                        (extract)
    gen-model           generates ECMAScript models.
                        (extract >> gen-model)
    compile-repl        performs REPL for printing compile result of particular step.
                        (compile-repl)
    gen-test            generates tests with the current implementation as the oracle.
                        (gen-test)
    parse               parses a JavaScript file using the generated parser.
                        (parse)
    load                loads a JavaScript AST to the initial IR states.
                        (parse >> load)
    eval                evaluates a JavaScript file using generated interpreter.
                        (parse >> load >> eval-ir)
    repl                performs REPL for a JavaScript file
                        (parse >> load >> repl-ir)
    analyze             performs static analysis for a given JavaScript program.
                        (parse >> analyze)
    collect             collects a JS state from concrete evaluation
                        (collect)
    filter-meta         extracts and filters out metadata of test262 tests.
                        (filter-meta)
    parse-ir            parses an IR file.
                        (parse-ir)
    load-ir             loads an IR AST to the initial IR states.
                        (parse-ir >> load-ir)
    eval-ir             evaluates an IR file.
                        (parse-ir >> load-ir >> eval-ir)
    repl-ir             performs REPL for IR instructions.
                        (parse-ir >> load-ir >> repl-ir)
    build-cfg           builds control flow graph (CFG).
                        (extract >> build-cfg)
    type-check          performs type checking for specifications.
                        (extract >> build-cfg >> type-check)

* phase list:
    Each phase has following options.
    format: {phase} [-{phase}:{option}[={input}]]*

    help                shows help messages.


    extract             extracts ECMAScript model from ecma262/spec.html.

                        If -extract:version={string} is given, set the git version of ecma262.
                        If -extract:query={string} is given, set target query.
                        If -extract:load={string} is given, load ECMAScript from JSON.
                        If -extract:json={string} is given, dump ECMAScript in a JSON format.
                        If -extract:detail is given, print log.

    gen-model           generates ECMAScript models.

                        If -gen-model:parser is given, generate JavaScript parser.

    compile-repl        performs REPL for printing compile result of particular step.

                        If -compile-repl:version={string} is given, set the git version of ecma262.
                        If -compile-repl:detail is given, print log.

    gen-test            generates tests with the current implementation as the oracle.


    parse               parses a JavaScript file using the generated parser.

                        If -parse:json={string} is given, dump JSON of AST tree into a file.
                        If -parse:pprint is given, pretty print AST tree
                        If -parse:esparse is given, use `esparse` instead of the generated parser.
                        If -parse:test262 is given, prepend test262 harness files based on metadata.

    load                loads a JavaScript AST to the initial IR states.

                        If -load:cursor={string} is given, set the type of evaluation cursors (default: node).

    analyze             performs static analysis for a given JavaScript program.

                        If -analyze:repl is given, use REPL for static analysis.
                        If -analyze:exec-level={number} is given, use concrete execution to check soundness.
                        If -analyze:gc is given, use abstract garbage collection.
                        If -analyze:inf-sens is given, use infinite sensitivity.
                        If -analyze:loop-iter={number} is given, set maximum loop iteration.
                        If -analyze:loop-depth={number} is given, set maximum loop depth.
                        If -analyze:js-k-cfa={number} is given, set k for JavaScrpt callsite sensitivity.
                        If -analyze:ir-k-cfa={number} is given, set k for IRES callsite sensitivity.
                        If -analyze:timeout={number} is given, set timeout of analyzer(second), 0 for unlimited.

    collect             collects a JS state from concrete/abstract evaluation

                        If -collect:concrete is given, collect concrete state.
                        If -collect:compiled is given, collect final states using compiled programs.
                        If -collect:start={number} is given, 
                        If -collect:end={number} is given, 
                        If -collect:inf-sens is given, use infinite sensitivity.
                        If -collect:loop-iter={number} is given, set maximum loop iteration.
                        If -collect:loop-depth={number} is given, set maximum loop depth.
                        If -collect:js-k-cfa={number} is given, set k for JavaScrpt callsite sensitivity.
                        If -collect:ir-k-cfa={number} is given, set k for IRES callsite sensitivity.

    parse-ir            parses an IR file.


    load-ir             loads an IR AST to the initial IR states.


    eval-ir             evaluates a given IR state.

                        If -eval-ir:timeout={number} is given, set timeout of interpreter(second), 0 for unlimited.

    repl-ir             performs REPL for IR instructions.


    build-cfg           builds control flow graph (CFG).

                        If -build-cfg:dot is given, dump the cfg in a dot format.
                        If -build-cfg:pdf is given, dump the cfg in a dot and pdf format.

    type-check          performs type checks for specifications.

                        If -type-check:dot is given, dump CFG in a dot format.
                        If -type-check:pdf is given, dump CFG in a dot and pdf format.
                        If -type-check:no-prune is given, no abstract state pruning.
                        If -type-check:insens is given, not use type sensitivity for parameters.
                        If -type-check:check-bug is given, check alarms.
                        If -type-check:target={string} is given, set the target of type checks.
                        If -type-check:repl is given, use REPL for type checks.
                        If -type-check:partial-model={string} is given, dump partial models using type checking results.
                        If -type-check:load={string} is given, load abstract semantics from a directory.
                        If -type-check:dump={string} is given, dump abstract semantics to a directory.

* global option:

    If -silent is given, do not show final results.
    If -debug is given, turn on the debug mode.
    If -view is given, turn on the view option.
    If -partial is given, evalute with partial model.
    If -interactive is given, turn on the interactive mode.
    If -no-bugfix is given, use semantics including specification bugs.
    If -log is given, turn on the logging mode.
    If -time is given, display the duration time.
```