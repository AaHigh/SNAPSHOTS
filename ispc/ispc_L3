
### Architecture Layer 3: Priority Queue and Escalation

Corrections are stored in a learning queue, ranked by:

1. **Frequency:** How many times has this same correction been made?
2. **Consistency:** Does the user always correct it the same way?
3. **Importance:** Is this a proper noun, brand name, or critical terminology?
4. **Recency:** Has the correction been made recently (indicating current priority)?

Rules in the queue are applied in priority order:

- **Tier 1 (Highest):** User has corrected this specific pattern 3+ times
- **Tier 2:** User has explicitly configured this as a preference
- **Tier 3:** Machine learning model detected systematic pattern (confidence > 95%)
- **Tier 4:** Standard dictionary or training data

### Architecture Layer 4: Interactive Configuration Dialog

When user enters "edit mode" or correction workflow:

1. **System Prompts:** "I noticed you keep correcting 'Hightower' to 'High Tower.' Should I learn this as a permanent rule?"
2. **User Confirms:** "Yes, always four words: the High Tower District"
3. **System Records:** Rule added to preference profile with Tier 2 priority
4. **System Applies:** All future transcriptions apply this rule proactively
5. **Changelog Entry:** 
