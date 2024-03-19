---
title: MSTest Design rules (code analysis)
description: Learn about MSTest code analysis design rules.
author: evangelink
ms.author: amauryleve
ms.date: 01/03/2024
---

# MSTest design rules

Design rules will help you create and maintain test suites that adhere to proper design and good practices.

Identifier | Name | Description
-----------|------|------------
[MSTEST0004](mstest0004.md) | PublicTypeShouldBeTestClassAnalyzer | It's considered a good practice to have only test classes marked public in a test project.
[MSTEST0006](mstest0006.md) | AvoidExpectedExceptionAttributeAnalyzer | Prefer `Assert.ThrowsException` or `Assert.ThrowsExceptionAsync` over `[ExpectedException]` as it ensures that only the expected call throws the expected exception. The assert APIs also provide more flexibility and allow you to assert extra properties of the exception.
[MSTEST0015](mstest0015.md) | TestMethodShouldNotBeIgnored | Test methods should not be ignored (marked with `[Ignore]`).
[MSTEST0016](mstest0016.md) | TestClassShouldHaveTestMethod | Test class should have at least one test method or be 'static' with method(s) marked by '[AssemblyInitialization]' and/or '[AssemblyCleanup]'.