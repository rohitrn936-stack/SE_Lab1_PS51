# Use-Case Flow Specification

## Use Case: Submit Manuscript

### 1. Preconditions

1. The Conference Author has access to the Virtual Technical Conference Platform.
2. The author has a technical manuscript ready for submission.
3. The conference submission period is open.

### 2. Postconditions

1. The manuscript is successfully stored in the conference platform.
2. The manuscript is anonymized by removing author-identifying information and metadata.
3. The anonymized manuscript is available for assignment to a reviewer pool.
4. The author receives confirmation that the manuscript has been submitted.

### 3. Main Success Scenario

1. The Conference Author logs into the Virtual Technical Conference Platform.
2. The author selects the "Submit Manuscript" option.
3. The author uploads the technical manuscript.
4. The system validates the submitted manuscript.
5. The system removes author-identifying information and metadata.
6. The system stores the anonymized manuscript.
7. The system makes the anonymized manuscript available for reviewer-pool assignment.
8. The system displays a successful submission confirmation to the author.

### 4. Alternate Flow

**A1. Invalid Manuscript Submission**

1. The author uploads a manuscript that does not satisfy the required submission format.
2. The system detects the invalid format.
3. The system rejects the manuscript submission.
4. The system informs the author that the manuscript format is invalid.
5. The author corrects the manuscript and submits it again.
