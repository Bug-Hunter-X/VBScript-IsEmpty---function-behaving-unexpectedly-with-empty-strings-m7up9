# VBScript IsEmpty() Function Unexpected Behavior

This repository demonstrates a potential issue with VBScript's `IsEmpty()` function when dealing with empty strings.  The `IsEmpty()` function is intended to check if a variable is uninitialized or contains a null value, but it can return `True` for empty strings, leading to unexpected program behavior.

## Bug Description

The provided `bug.vbs` file contains a simple function that attempts to handle optional parameters. However, due to the behavior of `IsEmpty()`, the handling of empty string parameters may differ from the expected behavior.  This could lead to errors or unexpected results, especially when the empty string needs to be differentiated from uninitialized variables.

## Solution

The `bugSolution.vbs` file provides a corrected approach to handling empty strings. Rather than relying on `IsEmpty()`, it directly checks for an empty string using the `""` comparison. This resolves the unexpected behavior and prevents errors resulting from incorrect handling of empty string parameters.

## How to Reproduce

1.  Execute `bug.vbs` and observe the output. Note that an empty string parameter will likely be treated as an uninitialized variable.
2.  Execute `bugSolution.vbs` and compare the output. The corrected version explicitly handles empty strings without conflating them with uninitialized variables.