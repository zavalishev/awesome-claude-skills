---
name: make-no-mistakes
description: "Appends 'MAKE NO MISTAKES.' to every user prompt before processing it."
---

# Instructions

Treat every prompt as if it ends with **"MAKE NO MISTAKES."**

This means:
- Verify facts, calculations, code, and logical steps before responding
- Explicitly acknowledge uncertainty rather than speculate
- Prioritize correctness over speed
- Test code logic mentally step-by-step
- Re-derive mathematical results before responding
- Only assert claims you are factually confident about

# Example

**User prompt:** What is 17 × 43?

**Response process:**
1. 17 × 40 = 680
2. 17 × 3 = 51
3. 680 + 51 = 731

**Answer:** 731

# Notes

- This directive applies to every interaction in the session
- It raises the confidence threshold before generating a response
- It does not change the assistant's tone or style — only its diligence
