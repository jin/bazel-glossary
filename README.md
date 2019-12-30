# Bazel Glossary

**Action.** A function that takes *artifacts* as inputs, and produces
*artifacts* as outputs. Includes the command line arguments, action key,
environment variables, and declared input/output artifacts.

**Action key**. The cache key of an *action*. Computed based on the command line
that will be executed, usually containing information like compiler flags,
library locations and system headers. Enables Bazel to cache or invalidate
individual actions deterministically.

**Action cache.**

**Action graph.**

**Analysis (Build phase).**

**Artifact.**

**Aspect.**

**Command.**

**Command flags.**

**Configurable attributes.**

**Configuration.**

**Configuration fragment.**

**Configuration-safe output.**

**Configured query.**

**Configured target.**

**Constraints.**

**Dependency.** A directed edge between two nodes in a graph. This can be a
**target dependency* in the *target graph*, or *action dependency* in the
*action graph*.

**Depset.** A data structure for collecting data on transitive dependencies.
Optimized to be time and space efficient around merging, because it’s common to
have very large depsets, scaling to hundreds of thousands of files. Implemented
to recursively refer to other depsets for space efficiency reasons. Rule
implementations should not flatten depsets to lists unless they are at the top
level. Flattening large depsets incur huge memory consumption. Also known as
*Nested Sets* in Bazel's internal implementation.

**Disk cache.**

**Distdir.** A read-only directory containing files that Bazel would otherwise
fetch from the internet using repository rules. Enables fully offline builds
in an air-gapped environment.

**Dynamic configurations.**

**Dynamic execution.** An execution strategy that wraps both the local and
*remote execution strategy, and through various heuristics, uses the execution
*result of the faster successful strategy. Certain actions are better executed
*locally (e.g. linking), and others remotely (highly parallelizable
*compilation), so the dynamic execution strategy provides the best possible
*incremental and full build times.

**Execution (Build phase).**

**Execution root.**

**Hermeticity.**

**Host configuration.**

**Incompatible change.**

**Label.**

**Loading (Build phase).**

**Mnemonic**. A short human readable string to quickly understand what an
*action* is doing. Can be used as identifiers for *spawn strategy* selections.
For example: `Javac`, `CppCompile`, `AndroidManifestMerger**.

**Nested Set.** See *depset*.

**Output base.**

**Output groups.**

**Output user root.**

**Package.** A directory containing a `BUILD` file. A package can contain
subpackages, which are subdirectories containing `BUILD` files.

**Platform.**

**Provider.**

**Remote caching.**

**Remote execution.**

**Repository.** A directory containing a `WORKSPACE` file.

**Repository cache.**

**Repository rule.**

**Reproducibility.**

**Rule.**

**Runfiles.**

**Sandboxing.**

**Skyframe.**

**Spawn strategy**. 

**Stamping.** A feature to embed additional information into Bazel-built
artifacts. Commonly used for source control, build time and other
workspace-related information for release builds. Enable through the
`--workspace_status_command` flag and rules that support the `stamp`
attribute.

**Starlark.**

**Starlark Build API.**

**Starlark configuration.**

**Startup flags.**

**Symlink forest.**

**Target.** A buildable unit. Can be a *rule target* or *file target*. Rule
targets are instantiated from rule declarations in `BUILD` files. Depending on
the rule implementation, rule targets can also be *testable* or *runnable*.
Every file used in `BUILD` files is a file target. Targets can depend on other
targets via attributes (most commonly but not necessarily `deps`).

**Target configuration.**

**Target graph.**

**Target pattern.**

**Toolchain.**

**Transition.**

**Trimming.**

**Visibility.**

**`.bazelrc`.**

**`BUILD`.**

**`WORKSPACE`.**