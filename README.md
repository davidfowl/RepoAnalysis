# RepoAnalysis

This repository stores datasets in CSV format containing issue lists for popular repositories. Each issue is annotated with engagement and frustration scores. The raw dataset and prompts are not available yet.

### **Final Engagement Score Formula**

Use the following formula to calculate the **Engagement Score** for each issue:

$$
S = \frac{w_c \cdot C^{1.5} \cdot C_{penalty} \cdot w_d \cdot (D + 0.1) \cdot (1 + w_l \cdot A) \cdot (1 + w_u \cdot U)}{1 + w_a \cdot \sqrt{A + \epsilon}}
$$

Where:
- **\(C\)**: Total number of comments.
- **\(C_{penalty}\)**: 
  - \(C_{penalty} = 0.25\) if \(C < 10\),
  - \(C_{penalty} = 1.0\) otherwise.
- **\(D\)**: Distribution factor, representing how evenly comments are spread over the issue's lifespan.
- **\(A\)**: Age of the issue in years (\(A = \text{(LastUpdated - CreatedAt)}\)).
- **\(\epsilon = 0.1\)**: Small constant added to prevent division by zero or undervaluing very recent issues.
- **\(U\)**: Total number of upvotes (if available, otherwise treated as 0).
- **Weights**:
  - **\(w_c = 2\)**: Emphasizes the number of comments.
  - **\(w_d = 1\)**: Balances the importance of distribution.
  - **\(w_l = 0.5\)**: Boosts older issues for longevity.
  - **\(w_u = 0.5\)**: Boosts issues with upvotes to reflect their priority/interest.
  - **\(w_a = 1\)**: Penalizes older issues for staleness.

### **Handling Missing Upvotes**:
- **If the Upvotes Field is Missing**: Treat **Upvotes** as 0, meaning the **Engagement Score** will be calculated without any boost from upvotes.
- **If Upvotes Exist**: The **Upvotes** field will **boost the engagement score** by contributing to the overall calculation of the score.

---

### **Frustration Score Formula**

To quantify the **frustration** users are experiencing with various issues, we can create a **Frustration Score** based on several factors such as:

$$
F = \left( w_c \cdot C \right) + \left( w_s \cdot S \right) + \left( w_r \cdot R \right) + \left( w_t \cdot T \right)
$$

Where:
- **\(C\)** = Number of comments on the issue.
- **\(S\)** = Sentiment score, based on the proportion of negative sentiments (e.g., using keywords like "bug", "error", "frustrating").
- **\(R\)** = Recurrence factor, a score indicating how often users bring up the issue.
- **\(T\)** = Time factor, where older issues get higher scores.

---
