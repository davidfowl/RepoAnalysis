Here's the revised set of prompts tailored explicitly for the uploaded dataset, ensuring alignment with its structure (e.g., issues with comments, metadata like CreatedAt, LastUpdated, and their engagement/frustration scores):

---

### **Critical Issue Identification**
**Prompt**:  
*"From the uploaded dataset, identify the top 5 most critical issues. Use these criteria:*  
   - **Engagement Score**: Use the formula provided to rank issues by user interest and activity.  
   - **Frustration Score**: Calculate scores to capture unresolved user dissatisfaction.  
   - **Sentiment in Comments**: Perform sentiment analysis to identify issues with predominantly negative comments.  
   - **Keyword Recurrence**: Look for urgency indicators ('urgent,' 'critical,' 'important') in issue descriptions and comments.  

For each issue, provide the following details:  
   - Title and URL.  
   - Engagement and Frustration Scores with a brief explanation.  
   - Sentiment summary (e.g., 'Predominantly Negative').  
   - A snippet of text showing urgency keywords (if applicable).  
   - A short explanation of why this issue is critical."  

**Expected Chat Output**:  
*"The most critical issue is 'Dependency Injection of Open Generics via Factory' (URL). It has an engagement score of 806.41, indicating strong community activity, and a frustration score of 55.67 due to its prolonged 4+ year unresolved status. Comments predominantly reflect negative sentiment, with keywords like 'critical' highlighting user urgency."*

---

### **Sentiment Insights**
**Prompt**:  
*"Perform sentiment analysis on the comments of each issue in the dataset and categorize them into three groups: Positive, Neutral, and Negative. For each group, provide:*  
   - A representative issue's Title and URL.  
   - Average sentiment score and a brief explanation of what it suggests about user attitudes.  
   - A comment snippet illustrating the sentiment.  

Focus on explaining the overall tone of the group based on representative examples."  

**Expected Chat Output**:  
*"For the Negative sentiment group, the issue 'Optimize ServiceCollectionDescriptorExtensions' (URL) stands out with an average sentiment score of -0.25. A user commented, 'This inefficiency is a dealbreaker for scaling our applications,' highlighting deep frustration with current limitations."*

---

### **Thematic Analysis**
**Prompt**:  
*"Cluster issues from the dataset into themes using their titles and descriptions. For each theme, provide:*  
   - The theme's name and top keywords (e.g., 'Dependency Scope: Scope, Lifetime, Disposable').  
   - The most representative issue's Title, URL, and Engagement Score.  
   - A short summary of what user concerns the theme represents.  

Base the grouping on recurring patterns across titles and descriptions."  

**Expected Chat Output**:  
*"One theme is 'Dependency Scope Management,' with keywords like 'scope,' 'lifetime,' and 'disposable.' The issue 'Fast Repeated Resolution of Dependency Injection Services' (URL, Engagement Score: 312.4) exemplifies this concern, focusing on inefficiencies when handling transient services. This theme highlights user challenges with performance optimization."*

---

### **Roadmap Development**
**Prompt**:  
*"Using the Engagement and Frustration Scores from the dataset, develop a roadmap for addressing high-priority issues. Group the roadmap into Immediate, Medium-Term, and Long-Term phases, providing for each phase:*  
   - Issue Title and URL.  
   - Engagement and Frustration Scores.  
   - The main user pain point (based on comments or descriptions).  
   - Recommended next steps for resolution."  

**Expected Chat Output**:  
*"Immediate Phase: Address 'Dependency Injection of Open Generics via Factory' (URL). Its engagement score of 806.41 and frustration score of 55.67 make it a top priority. User pain points focus on missing functionality and its long-open status. Next steps: Engage the community with a proposed design and schedule a resolution within 2 weeks."*

---

### **Oldest Unresolved Issues**
**Prompt**:  
*"From the dataset, identify the 5 oldest unresolved issues. For each issue, provide:*  
   - Title and URL.  
   - Age in years (based on CreatedAt and LastUpdated).  
   - Engagement and Frustration Scores.  
   - A short explanation of why the issue may have been left unresolved."  

**Expected Chat Output**:  
*"One of the oldest unresolved issues is 'DependencyInjection Add Factory for Generated Classes' (URL), open for over 5 years. Despite moderate engagement (50.8) and low frustration (20.3), its lack of resolution suggests limited user impact or prioritization by maintainers."*

---

### **Comment Activity Trends**
**Prompt**:  
*"Analyze comment activity trends for each issue in the dataset. Identify issues with significant spikes in activity and provide:*  
   - Issue Title and URL.  
   - The month(s) with the highest comment activity and the number of comments.  
   - Possible reasons for the spike (e.g., related to a release or community discussion)."  

**Expected Chat Output**:  
*"The issue 'Dependency Injection: Add Factory for Generated Classes' (URL) had a comment spike in March 2020 with 15 comments. This spike aligns with a major framework release, driving community discussions on new dependency injection features."*

---

### **Keyword-Based Prioritization**
**Prompt**:  
*"Search the dataset for issues containing urgency keywords ('critical,' 'urgent,' 'important'). For each matching issue, provide:*  
   - Title and URL.  
   - Engagement and Frustration Scores.  
   - A snippet containing the urgency keyword."  

**Expected Chat Output**:  
*"The issue 'Optimize ServiceCollectionDescriptorExtensions' (URL) includes the keyword 'critical': 'This optimization is critical for improving dependency injection performance.' Engagement: 311.48, Frustration: 32.55."*

---

### **Deep Dive on High-Frustration Clusters**
**Prompt**:  
*"For the cluster with the highest average frustration score, provide:*  
   - Cluster name and top keywords.  
   - Issues in the cluster (Title and URL).  
   - The primary concern driving frustration, based on comments and scores."  

**Expected Chat Output**:  
*"Cluster: 'Service Lifetime Management' (keywords: scope, lifetime, disposable). Issues include 'Fast Repeated Resolution of Dependency Injection Services' (URL). The main frustration stems from inefficiencies in transient service resolution, as reflected in comments like 'This slows down large-scale applications significantly.'"*

---

These prompts are tailored to leverage the structure of your dataset while ensuring outputs are chat-based, narrative-driven, and provide clear, actionable insights. Let me know if you’d like further adjustments!