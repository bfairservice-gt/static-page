---
layout: oss
tags: oss
title: GTIRB
link: https://github.com/grammatech/gtirb
brief: |
    A fast and accurate disassembler.  DDisasm is able to disassemble
    real-world stripped binaries with accuracy sufficient to enable modification
    and reassembly.  The core disassembly logic is implemented in datalog
    resulting in *fast* parallel disassembly, and the easy declarative specification
    of disassembly heuristics.
---

GTIRB is GrammaTech's Intermediate Representation for Binary analysis
and rewriting.  It seeks to be for binaries what LLVM is for source
allowing researchers and developers to compose tools and leverage each
other's work. GTIRB is described in a [blog][], [whitepaper][],
[tutorial][], and in its [manual][].  GTIRB is a relatively simple
data structure (shown below).

<center>
  <!-- <img class="w3-round" src="{{ "/img/gtirb.svg"|url }}" width="80%"> -->
  {% include ../img/gtirb.svg %}
</center>

The GTIRB data structure tries to structurally require the minimal
analysis results that are required for binary analysis and rewriting.
All other analysis results and properties can be stored in AuxData
tables (there are a large number of [standard AuxData tables][]).

A growing number of tools are emerging that emit and consume GTIRB:

<center>

| Tool                    | Description                                            |
|-------------------------|--------------------------------------------------------|
| [DDisasm][]             | Fast and accurate disassembler which produces GTIRB    |
| [GTIRB-PPrinter][]      | Pretty print GTIRB to assembler or a binary executable |
| [gtirb-rewriting][]     | Python API for rewriting GTIRB files                   |
| [gtirb-functions][]     | APIs for working with functions in GTIRB files         |
| [gtirb-ghidra-plugin][] | Import/Export GTIRB files to/from Ghidra               |
| [gtirb-capstone][]      | Integration with the [Capstone][] decoder              |
| [gtirb-stack-stamp][]   | Example hardening transform over GTIRB                 |

</center>

[blog]: https://blogs.grammatech.com/open-source-tools-for-binary-analysis-and-rewriting
[whitepaper]: https://arxiv.org/abs/1907.02859
[manual]: https://grammatech.github.io/gtirb
[tutorial]: https://grammatech.github.io/gtirb/md_stack-stamp.html
[standard AuxData tables]: https://grammatech.github.io/gtirb/md__aux_data.html#sanctioned-auxdata-tables
[DDisasm]: {{ "/oss/ddisasm"|url }}
[GTIRB-PPrinter]: https://github.com/grammatech/gtirb-pprinter
[gtirb-rewriting]: https://github.com/grammatech/gtirb-rewriting
[gtirb-functions]: https://github.com/grammatech/gtirb-functions
[gtirb-ghidra-plugin]: https://github.com/grammatech/gtirb-ghidra-plugin
[gtirb-stack-stamp]: https://github.com/grammatech/gtirb-stack-stamp
[gtirb-capstone]: https://github.com/GrammaTech/gtirb-capstone
[Capstone]: https://www.capstone-engine.org