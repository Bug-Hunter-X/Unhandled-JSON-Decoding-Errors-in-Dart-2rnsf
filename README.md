# Unhandled JSON Decoding Errors in Dart

This repository demonstrates a common issue in Dart applications: insufficient error handling when decoding JSON data. The provided code lacks specificity in error handling, making it challenging to debug JSON parsing problems.  The solution shows how to improve error handling for better debugging.

## Bug

The `fetchData` function attempts to fetch JSON data from an API. However, it uses a generic `catch` block that doesn't provide specific information about JSON decoding errors. This makes it hard to identify whether the problem stems from a malformed JSON response, a network error, or another issue. 

## Solution

The solution enhances error handling by using a `try-catch` block specifically for `FormatException`. This allows you to distinguish between network issues or other exceptions and issues directly related to the JSON structure.