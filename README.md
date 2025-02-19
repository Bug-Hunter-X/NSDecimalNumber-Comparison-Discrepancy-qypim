# NSDecimalNumber Comparison Discrepancy in Objective-C

This repository demonstrates a subtle bug in Objective-C related to comparing `NSDecimalNumber` objects created from different string representations.  Even though the numbers represent the same numerical value, the comparison using `isEqualToNumber:` might incorrectly return `NO` due to internal representation differences.  The solution showcases how to handle this comparison reliably.

## Bug Description

The bug occurs when creating `NSDecimalNumber` objects from strings with varying formatting (e.g., extra whitespace, different decimal notations).  A direct comparison using `isEqualToNumber:` may fail despite the numbers being mathematically equivalent.

## Solution

The provided solution shows how to use `compare:` method which provide more robust comparison, handling different representations consistently.