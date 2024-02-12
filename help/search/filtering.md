# Project Query Handling Overview

## Constants Definition:
- A constant array `BREAKING_CHARS` is defined, containing special characters that, if found in the query, will be removed.

## Extracting Query from URL:
- The code extracts the query parameter from the URL using the `URL` constructor.
- If the query is empty or undefined, it redirects to the home page.

## Cleaning the Query:
- A flag `shouldCleanQuery` is set based on whether the query contains characters other than letters, numbers, spaces, and specific punctuation.
- The `cleanQuery` function removes unwanted characters from the query using regular expressions.
- It also identifies and removes characters specified in the `BREAKING_CHARS` array.
- The function returns the cleaned query, replaced characters, and an array representation of the cleaned query.

## Fetching Data:
- The code fetches data using the `fetchData` function from a specified API endpoint.
- The API endpoint includes the cleaned query as a parameter and sets a cache duration of 1 minute.

## Displaying Alert (if necessary):
- If the `shouldCleanQuery` flag is true, an alert is displayed to notify the user that some characters in their search couldn't be processed.
- The alert includes a list of characters that were removed from the query.
- A link is provided for the user to learn more about the search filtering process.
