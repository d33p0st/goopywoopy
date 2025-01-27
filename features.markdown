---
layout: default
title: Features
nav_order: 2
permalink: /features/
---

# Features under GoopyWoopy
{: .no_toc }

GoopyWoopy boasts a few interesting features.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Typing

The `Typing` Section includes helpers and mechanisms related to typing you code base.

### `@override` decorator for python3.8+

The `@override` decorator was introduced in python3.12+ under the `typing` module. However, for python<3.12, it is not available.

The `override` class under `goopywoopy` supports python3.8+ and brings
additional features rather than just helping in maintaining an error
free codebase.

The `override` class contains two static methods that can be used as
decorators: `cls` and `mtd`. The `@override.mtd` acts as a decorator
for the child class methods which are being over-ridden from the
parent class. It sets the `__override__` attribute of the methods,
it has been decorated with, as `True`.

The `@override.cls` decorator on top of a child class, checks for
all methods that have their `__override__` attribute set as `True`
and it generates errors accordingly. It will raise
`MethodOverrideError` if the method set as override is not present in
the parent class. Additionally, it will also check if the current class
is a child class or not (inheritance is implemented or not).

Apart from methods, the properties need not be decorated with `mtd`,
the `@override.cls` over the class will automatically check if the
property is over-ridden or not. If a over-ridden property does not include a `setter` or `deleter` or both, the parent property's
`setter` and `deleter` will be copied to the child class.

## Class Tools

### `Property` class for automating `property` creation at runtime
{: d-inline-block }

v0.1.0
{: .label .label-blue }

### Several Abstract Classes for different purposes
{: .d-inline-block }

Updated
{: .label .label-red }

#### `Possibility` Abstract class for extending return types of methods
{: .d-inline-block }

v0.1.0
{: .label .label-blue }

#### `Feature` Abstract class for creating individual features
{: .d-inline-block }

New
{: .label .label-green }

v0.2.0
{: .label .label-blue }

## Progress

### A Re-defined Fully Customizable `ProgressBar`
{: .d-inline-block }

New
{: .label .label-green }

v0.2.0
{: .label .label-blue }

## Utilities

### The `Random` class for picking a random value from a pool
### The `terminal` module for terminal related operations

<!-- Page Links -->
[GitHub Issues]: https://github.com/d33p0st/goopywoopy/issues
[GitHub Pull Requests]: https://github.com/d33p0st/goopywoopy/pulls
[GitHub]: https://github.com/d33p0st/goopywoopy