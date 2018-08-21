**Term-based queries \( Or Exact Value queries\)**

Queries like the term or fuzzy queries are low-level queries that have no analysisphase. Term queries search for exact values . we are actually searching the inverted index for the term and not the document itself.

Term level queries search for exact matches so the casing of letters matters.

Term level  queries search for exact values and are not analyzed whereas full text queries are analyzed using the same analyzer.





From 1\)

• When you query a full-text field, the query will apply the same analyzer to the query string to produce the correct list of terms to search for.

• When you query an exact-value field, the query will not analyze the query string, but instead search for the exact value that you have specified.

