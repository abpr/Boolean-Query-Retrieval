# Boolean-Query-Retrieval

TAAT = “Term At A Time”
->Scores for all docs computed concurrently, one query term at a time

DAAT = “Document At A Time”
->Total score for each doc (incl all query terms) computed,
before proceeding to the next

Implementation:

Term-at-a-Time Processing (TAAT): scan postings list one
at a time, maintain a set of potential matching documents
along with their partial scores

Document-at-a-Time Processing (DAAT): scan postings
lists in parallel, identifying at each point the
