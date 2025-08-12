# Report: Prompting Techniques for Efficient Use of LLMs

## 1. Introduction

Prompting is the process of crafting input queries to guide LLMs (like GPT-4) to produce desired outputs. The effectiveness of LLMs is highly dependent on the quality and structure of prompts. This report explores various prompting methods, provides examples, analyzes their effectiveness for different use cases, and compares their outputs.

---

## 2. Prompting Methods
 
### 2.1. Zero-Shot Prompting


**What is Zero-Shot Prompting?**

Zero-shot prompting is a technique used with large language models (LLMs) where you provide a prompt or question without any prior examples or demonstrations. The model is expected to generate a relevant response based solely on its pre-trained knowledge and understanding of the prompt, without being shown how to answer similar questions beforehand.

This is different from few-shot prompting, where you provide a few examples to guide the model, or fine-tuning, where the model is trained on a specific dataset.

**Key Characteristics**

- No examples: The prompt contains only the task or question.
- Relies on model knowledge: The model uses its pre-trained data to infer the answer.
- Flexible: Useful for tasks where you don't have labeled examples.

---

**Examples of Zero-Shot Prompting**

Below are five examples. Each shows the input prompt and the model output as it might appear from an LLM.

---

**Example 1: Text Summarization**

**Prompt:**
```
Summarize the following paragraph in one sentence:

"Artificial intelligence is a rapidly evolving field that focuses on creating machines capable of performing tasks that typically require human intelligence. These tasks include learning, reasoning, problem-solving, perception, and language understanding."
```

**Model Output:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Artificial intelligence is a field dedicated to developing machines that can perform tasks requiring human-like intelligence, such as learning and problem-solving.
</div>

---

**Example 2: Language Translation**

**Prompt:**
```
Translate the following English sentence to French:

"The weather is beautiful today."
```

**Model Output:**
Le temps est magnifique aujourd'hui.

---

**Example 3: Sentiment Analysis**

**Prompt:**
```
What is the sentiment of this review? "The product arrived late and was damaged. Very disappointed."
```

**Model Output:**
Negative

---

**Example 4: Code Generation**

**Prompt:**
```
Write a Python function that returns the square of a number.
```

**Model Output:**
```python
def square(number):
  return number * number
```

---

**Example 5: Question Answering**

**Prompt:**
```
Who wrote the play "Romeo and Juliet"?
```

**Model Output:**
William Shakespeare

---

**Effectiveness:**  
- **Best for:** Simple, well-defined tasks.
- **Limitations:** May lack accuracy for complex or ambiguous tasks.

---

### 2.2. Few-Shot Prompting

**What is Few-Shot Prompting?**

Few-shot prompting is a technique where you provide a few examples of the task within the prompt. The model uses these demonstrations to infer the pattern and generate an appropriate response for a new, similar input.

**Key Characteristics**
- Includes 2-5 examples in the prompt
- Helps the model learn the desired format, style, or logic
- Useful for tasks with variable outputs or requiring specific structure

---

**Examples of Few-Shot Prompting**

Below are several examples. Each shows the input prompt and the model output, styled for clarity.

---

**Example 1: Language Translation**

**Prompt:**
```
Translate to French:
- 'Good morning.' → 'Bonjour.'
- 'How are you?' → 'Comment ça va ?'
- 'The weather is nice today.' →
```

**Model Output:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Le temps est agréable aujourd'hui.
</div>

---

**Example 2: Sentiment Classification**
**Prompt:**
```
Classify the sentiment:
- "I love this product!" → Positive
- "This is terrible." → Negative
- "It's okay, not great." →
```
**Model Output:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 12px; background:#ffffff; margin: 8px 0;">
Neutral
</div>

---

**Example 3: Text Summarization**
**Prompt:**
```
Summarize:
- "The cat sat on the mat." → "A cat is on a mat."
- "The dog barked at the mailman." → "A dog barked at a mailman."
- "The sun rises in the east and sets in the west." →
```
**Model Output:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 12px; background:#ffffff; margin: 8px 0;">
The sun rises in the east and sets in the west.
</div>

---

**Example 4: Math Pattern Induction**
**Prompt:**
```
What is the next number in the sequence?
- 2, 4, 6, 8, ? → 10
- 5, 10, 15, 20, ? → 25
- 3, 6, 9, 12, ? →
```
**Model Output:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
15
</div>

---

**Effectiveness:**  
- **Best for:** Tasks where context or style is important.
- **Limitations:** Requires careful selection of examples.

---

### 2.3. Chain-of-Thought (CoT) Prompting

**Description:**  
Encourage the model to reason step-by-step.


**Prompt Example 1:**
```
Q: If there are 3 apples and you take away 2, how many do you have?
A: Let's think step by step. There are 3 apples. If I take away 2, I have 2 apples.
```

**Model Output 1:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
2 apples.
</div>

**Prompt Example 2:**
```
Q: John has 5 books. He buys 3 more and gives 2 to his friend. How many books does he have now?
A: Let's break it down. John starts with 5 books. He buys 3 more, so now he has 8 books. He gives 2 away, so 8 - 2 = 6 books.
```

**Model Output 2:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
6 books.
</div>

**Prompt Example 3:**
```
Q: The train leaves at 3 PM and the journey takes 2 hours and 30 minutes. What time does it arrive?
A: The train leaves at 3 PM. Adding 2 hours makes it 5 PM. Adding 30 minutes makes it 5:30 PM.
```

**Model Output 3:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
5:30 PM.
</div>

**Effectiveness:**  
- **Best for:** Reasoning, math, logic, and multi-step problems.
- **Limitations:** May generate verbose outputs.

---

### 2.4. Instruction-Based Prompting

**Description:**  
Give explicit instructions on how to perform the task.


**Prompt Example 1:**
```
Summarize the following paragraph in one sentence: "Artificial intelligence is transforming industries by automating tasks and providing insights from data."
```

**Model Output 1:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
AI is transforming industries through automation and data insights.
</div>

**Prompt Example 2:**
```
Write a polite email declining a meeting invitation.
```

**Model Output 2:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Dear [Name],
Thank you for the invitation. Unfortunately, I am unable to attend the meeting. I appreciate your understanding.
Best regards,
[Your Name]
</div>

**Prompt Example 3:**
```
List three key features of electric cars.
```

**Model Output 3:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
- Zero emissions
- Quiet operation
- Instant torque
</div>

**Effectiveness:**  
- **Best for:** Tasks requiring specific formats or constraints.
- **Limitations:** May require prompt tuning for optimal results.

---

### 2.5. Role-Based Prompting

**Description:**  
Assign a role or persona to the model.


**Prompt Example 1:**
```
You are a helpful assistant. Explain quantum computing in simple terms.
```

**Model Output 1:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Quantum computing uses the principles of quantum mechanics to process information in a way that can be much faster than traditional computers for certain tasks.
</div>

**Prompt Example 2:**
```
You are a professional chef. Describe how to make a perfect omelette.
```

**Model Output 2:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
To make a perfect omelette, beat eggs with a pinch of salt, pour into a hot nonstick pan, and gently stir until just set. Fold and serve immediately.
</div>

**Prompt Example 3:**
```
You are a history teacher. Briefly explain the significance of the Magna Carta.
```

**Model Output 3:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
The Magna Carta, signed in 1215, limited the power of the English king and laid the foundation for modern democracy and legal rights.
</div>


**Effectiveness:**  
- **Best for:** Adapting tone, style, or expertise.
- **Limitations:** May not always strictly adhere to the role.

---

### 2.6. Contextual Prompting

**Description:**  
Provide background information or context.


**Prompt Example 1:**
```
Given the following data about climate change, write a summary: "Global temperatures have risen by 1.2°C since 1880. Sea levels are rising, and extreme weather events are becoming more frequent."
```

**Model Output 1:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Global warming has led to higher temperatures, rising sea levels, and more frequent extreme weather events.
</div>


**Prompt Example 2:**
```
Context: The company has recently launched a new product line targeting young adults. Task: Write a marketing slogan for this product.
```

**Model Output 2:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
"Unleash Your Potential with Our New Collection!"
</div>


**Prompt Example 3:**
```
Background: The patient has a history of hypertension and diabetes. Question: What are important considerations for their treatment?
```

**Model Output 3:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Monitor blood pressure and blood sugar closely, adjust medications as needed, and encourage lifestyle changes.
</div>


**Effectiveness:**  
- **Best for:** Tasks requiring understanding of context or background.
- **Limitations:** Context must be relevant and concise.

---

### 2.7. Output-Constrained Prompting

**Description:**  
Specify the desired format or constraints for the output.


**Prompt Example 1:**
```
List three benefits of exercise in bullet points.
```

**Model Output 1:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
- Improves cardiovascular health
- Boosts mental well-being
- Increases energy levels
</div>


**Prompt Example 2:**
```
Provide a JSON object with the following information: name, age, and occupation for a fictional character.
```

**Model Output 2:**
<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
{
  "name": "Alex Smith",
  "age": 30,
  "occupation": "Engineer"
}
</div>

**Prompt Example 3:**
```
Write a Python function that returns the square of a number. Only output the code.
```

**Model Output 3:**
``` 
def square(n):
    return n * n
```
**Effectiveness:**  
- **Best for:** Structured outputs (lists, tables, code).
- **Limitations:** May require re-prompting for strict adherence.

---

## 3. Effectiveness by Use Case

| Use Case                | Zero-Shot | Few-Shot | CoT      | Instruction | Role-Based | Contextual | Output-Constrained |
|-------------------------|-----------|----------|----------|-------------|------------|------------|--------------------|
| Simple Q&A              | High      | High     | Medium   | High        | Medium     | Medium     | Medium             |
| Translation             | Medium    | High     | Low      | High        | Low        | Medium     | Medium             |
| Reasoning/Math          | Low       | Medium   | High     | Medium      | Low        | Medium     | Medium             |
| Summarization           | Medium    | Medium   | Medium   | High        | Medium     | High       | Medium             |
| Code Generation         | Medium    | High     | Medium   | High        | Medium     | High       | High               |
| Style/Tone Adaptation   | Low       | Medium   | Low      | Medium      | High       | Medium     | Medium             |
| Data Extraction         | Low       | Medium   | Low      | High        | Low        | High       | High               |

---

## 4. Comparative Analysis

### 4.1. Output Quality

- **Zero-Shot:** Fast and simple, but may lack nuance or accuracy for complex tasks.
- **Few-Shot:** Improves accuracy and style matching, especially for tasks with variability.
- **CoT:** Significantly enhances reasoning and multi-step problem solving.
- **Instruction-Based:** Ensures outputs meet specific requirements.
- **Role-Based:** Useful for tone and persona adaptation.
- **Contextual:** Essential for tasks needing background knowledge.
- **Output-Constrained:** Ensures structured and predictable outputs.

### 4.2. Example Comparison

**Task:** Summarize a paragraph.

- **Zero-Shot:**  
  "Summarize: [Paragraph]"  
  Output: May be generic or miss key points.

- **Few-Shot:**  
  "Summarize:  
  - [Example Paragraph 1] → [Summary 1]  
  - [Paragraph]"  
  Output: More aligned with desired style.

- **Instruction-Based:**  
  "Summarize the following in one sentence: [Paragraph]"  
  Output: Concise and focused.

- **Contextual:**  
  "Given the following background, summarize: [Background] [Paragraph]"  
  Output: Incorporates relevant context.

---

## 5. Conclusion

Prompting techniques greatly influence LLM performance.  
- **Zero-shot** is best for simple, direct tasks.  
- **Few-shot** and **CoT** excel in complex, nuanced, or reasoning-heavy tasks.  
- **Instruction-based** and **output-constrained** prompting are ideal for tasks requiring specific formats or outputs.  
- **Role-based** and **contextual** prompting are valuable for tone, style, and context-sensitive tasks.

Experimentation and prompt engineering are key to maximizing LLM effectiveness for any use case.

---


