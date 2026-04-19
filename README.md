1.1 Core Research Question
When reusing test cases across semantically similar Python functions, does selecting tests from embedding-based clusters produce better test effectiveness than random selection — and which embedding model best supports this?

1.2 Central Hypothesis
Functions that are semantically similar should share compatible behaviour, meaning their test cases should transfer more effectively. Code embedding models capture semantic similarity in vector space, and clustering groups this similarity. Therefore, reusing tests from cluster-members of a given function should outperform randomly selecting tests from the broader signature pool.

1.3 Research Contribution
This research makes the following contributions:
•	A systematic comparison of seven embedding models for code clustering quality, evaluated across four ground-truth dimensions (bug type, AST structure, LDA topics, function length)
•	A novel cluster-based test reuse pipeline that selects test cases for a Function Under Test (FUT) based on semantic similarity rather than random sampling
•	An empirical evaluation of whether embedding-based test reuse achieves higher pass rates and mutation scores compared to a random baseline
•	Identification of the best-performing embedding model and clustering algorithm combination for test reuse effectiveness

1.4 Dataset
Dataset	PyTrace — a Python bug-fix dataset containing real-world buggy and fixed function pairs
Raw size	23,575 Python functions
After filtering	19,358 functions (duplicates, malformed entries removed)
Fields used	before_merge (buggy code), after_merge (fixed code), function_name, traceback_type, unique function ID
Bug types	TypeError, ValueError, AttributeError, KeyError, IndexError, and others
Tokenisation	Function names and parameters extracted as tokens per function
