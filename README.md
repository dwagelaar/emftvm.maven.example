# ATL/EMFTVM maven example

[![Build Status](https://travis-ci.org/dwagelaar/emftvm.maven.example.svg?branch=master)](https://travis-ci.org/dwagelaar/emftvm.maven.example)

## Description

This repo contains an example of how to use [ATL/EMFTVM](https://wiki.eclipse.org/ATL/EMFTVM) in a maven build scenario. The repo contains an ATL model transformation module and a UML model:

* `transformations/Example.atl`
* `model/Example.uml`

## Prerequisites

* JDK 8
* Maven 3.0+

## Usage

The maven project first compiles the ATL transformation module, and then runs it against the UML model. Invoke maven as follows from the project root:

```
mvn verify
```

The compiled ATL transformation module and the transformed UML model can both be found in the `target` folder:

  - `target/Example.emftvm`
  - `target/Example.uml`

The `target/Example.emftvm` is the EMFTVM bytecode of the ATL transformation module, which can be read with an Eclipse IDE with ATL/EMFTVM 4.0 installed, and `target/Example.uml` is the same as the input UML model, with a single comment added.
