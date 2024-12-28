# PHP Type Juggling Gotcha

This repository demonstrates a common, yet subtle, error in PHP related to type juggling and loose comparisons.  The code showcases the difference between loose comparison (`==`) and strict comparison (`===`) when comparing strings and integers.  Loose comparisons can lead to unexpected behavior if not carefully considered.

## The Problem

PHP's loose comparison (`==`) performs type coercion before comparing values.  This means that if you compare a string '0' with an integer 0, they will be considered equal because PHP converts the string to an integer.  This behavior might be unexpected if you're relying on strict type checking.

## The Solution

Always use the strict comparison operator (`===`) when comparing values in PHP if you need to ensure both the value and the type are identical.  This will prevent unexpected results caused by type juggling.