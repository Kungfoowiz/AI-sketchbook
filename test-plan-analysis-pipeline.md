| Step | Input | Process | Output |
| --- | --- | --- | --- |
| 1. Answer test architect questions | Extracted system information | Build system understanding for testing by answering test architect questions | System understanding for testing |
| 2. Verify evidence | System understanding for testing | Check the underlying evidence is real by counting of evidence items and no missed scenarios | Verified system understanding |
| 3. Create gap analysis report | Verified system understanding | Identify missing logic, contradictions, and unclear rules. Assign each a Gap ID (GAP-n) | Gap analysis report with Gap IDs |
| 4. Create the feature test plan | Verified system understanding and gap analysis report | For each feature, rule and gap, assign a functional requirement (FR-n) or gap ID, and create a test plan. Test types and automated test IDs (AT-n) are created for each test, which link to the functional requirements and gaps (FR-n, GAP-n) | Feature test plan with automated test IDs |
| 5. Modify feature test plan and gap analysis report based on available BA insights | BA feature and rules insights | Update the feature test plan and gap analysis report with BA additions, removals, and rule changes. Redo the functional requirement, gap, and automated test IDs as required | Finalised feature test plan and updated gap analysis report with IDs (AT-n, FR-n, GAP-n) |
