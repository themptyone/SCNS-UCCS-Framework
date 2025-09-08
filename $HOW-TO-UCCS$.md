# How to Use the UCCS Framework

Engaging with a UCCS-compliant AI is a structured dialogue. 

This guide explains how to drive the process.

-----

## Step 1: Initialize the Protocol

Start your request by attaching src/UCCS-CORE/UCCS-CORE0000.md & COOKIE GENIE PROMPT stating your **goal** and your **knowledge level (UPL)** for the task.

*In the example below we are generating a new cookie recipes for our communal kitchen use the `$COOKIEGENIE:PROMPT$` within the `$UCCS-CORE0000:FRAMEWORK$`*

**Example User Prompt:**

```
I need to generate a cookie recipe using the COOKIE GENIE protocol. My UPL is 2, as I'm new to this.
```

-----

## Step 2: Engage with the UIP Loop


*The AI will follow the strict UIP sequence.*

Your responsibility is to review and validate at each confirmation gate.

1. **Background Generation**  

The AI generates the content internally.

2. **Summary** 

Example:

   ```
   I have generated a complete, SCNS-compliant recipe for 'Beginner's Classic Chocolate Chip Cookies.' 
   The recipe includes an overview, structured ingredient lists, 6 clear instructions with dependencies, and chef's notes.
   ```

3. **Preview**  

Example:

   ```markdown
   ### Recipe Overview
   `$BLOG-RECIPES:COOKIE:CLASSIC:OVERVIEW:N0010$`
   A timeless recipe for chewy, delicious chocolate chip cookies...

   Ingredients  
   Dry Ingredients `$COOKIEGENIE:PROMPT:DRY-INGREDIENTS:N0020$`

   - 2 ¼ cups All-Purpose Flour
   - ...
   ```

4. **Confirmation Gate**  

Example:

   ```
   Proceed with COOKIE GENIE recipe generation? (Y/N/Modify)
   ```

-----

## Step 3: Provide Your Command

At the confirmation gate, you control the outcome:

- **Y** → Accept the generated content and proceed.

- **N** → Halt the process. The AI will stop and summarize progress. 

- **Modify** → Request specific changes. 

Example:

  ```
  Modify: Change the serving size to 24 cookies and make it nut-free.
  ```

The AI will re-enter the UIP loop and regenerate content until you approve.

-----

## Integrating with AI Agents

UCCS is a universal framework that adapts to multiple AI agents, each governed by a specialized sub-protocol.

### UCCS-INF-CLAUDE (Structured Process)

- **Purpose:** Repeatable process patterns and structured AI-human collaboration. 

- **Best For:** Systematic workflows like project planning, documentation generation, or complex problem-solving.

### UCCS-INF-PERPLEXITY (Real-Time Research)

- **Purpose:** Real-time research with mandatory source verification and credibility assessment.

- **Best For:** Fact-checking, report writing, market analysis, and up-to-date research.

### UCCS-INF-GROK (Dynamic Tool Orchestration)

- **Purpose:** Real-time data analysis, multimedia content processing, and multi-tool orchestration. 

- **Best For:** Fast-moving event insights, uploaded file analysis (PDFs, images), or multi-tool workflows.

-----

## Conclusion

Congratulations! You have successfully used the UCCS framework to collaborate with an AI, maintaining **full control** and **traceability** throughout the process.  

Welcome to the future of structured AI interaction.  

**MAX POWER, MAX STEAM!**
