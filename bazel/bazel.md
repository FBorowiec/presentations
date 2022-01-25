---
title: Bazel
author: F.Borowiec
date: 2021-10-27
extensions:
    - image_ueberzug
styles:
    style: paraiso-dark
    table:
        column_spacing: 3
        header_divider: "-"
---

# Bazel

Bazel is a free software tool for the automation of building and testing of software.

The company Google uses the build tool Blaze internally and released an open-sourced part of the Blaze tool as Bazel, named as an anagram of Blaze.

---

# Why use Bazel?

* **High-level build language**.
    * Bazel uses an abstract, human-readable language to describe the build properties of your project at a high semantical level.
    * Unlike other tools, Bazel operates on the concepts of libraries, binaries, scripts, and data sets, shielding you from the complexity of writing individual calls to tools such as compilers and linkers.
* **Bazel is fast and reliable**.
    * Bazel caches all previously done work and tracks changes to both file content and build commands.
    * This way, Bazel knows when something needs to be rebuilt, and rebuilds only that. To further speed up your builds, you can set up your project to build in a highly parallel and incremental fashion.
* **Bazel is multi-platform**.
    * Bazel runs on Linux, macOS, and Windows.
    * Bazel can build binaries and deployable packages for multiple platforms, including desktop, server, and mobile, from the same project.
* **Bazel scales**.
    * Bazel maintains agility while handling builds with 100k+ source files.
    * It works with multiple repositories and user bases in the tens of thousands.
* **Bazel is extensible**.
    * Many languages are supported, and you can extend Bazel to support any other language or framework.

---

# How does Bazel work

When running a build or a test, Bazel does the following:

* Loads the BUILD files relevant to the target.
* Analyzes the inputs and their dependencies, applies the specified build rules, and produces an action graph.
* Executes the build actions on the inputs until the final build outputs are produced.

Since all previous build work is cached, Bazel can identify and reuse cached artifacts and only rebuild or retest what’s changed.

To further enforce correctness, you can set up Bazel to run builds and tests hermetically through sandboxing, minimizing skew and maximizing reproducibility.

---

# Bazel rules

|Language     |Tiobe Index Rank (2019)|Bazel Support|
|------------:|:---------------------:|-------------|
|Java         |1                      | Yes         |
|C            |2                      | Yes         |
|Python       |3                      | Yes         |
|C++          |4                      | Yes         |
|C#           |5                      | Yes         |
|Javascript   |7                      | Yes         |
|Swift        |10                     | Yes         |
|Ruby         |11                     | Yes         |
|Objective-C  |12                     | Yes         |
|Groovy       |14                     | Yes         |
|R            |16                     | Yes         |
|D            |18                     | Yes         |
|Golang       |20                     | Yes         |
|Perl         |21                     | Yes         |
|Rust         |25                     | Yes         |
|Scala        |30                     | Yes         |
|Kotlin       |35                     | Yes         |
|Typescript   |43                     | Yes         |
|Haskell      |44                     | Yes         |
|Bash         |48                     | Yes         |

