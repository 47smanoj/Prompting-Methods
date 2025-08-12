# Zero-Shot Prompting: Definition and Examples

## What is Zero-Shot Prompting?

**Zero-shot prompting** is a technique used with large language models (LLMs) where you provide a prompt or question without any prior examples or demonstrations. The model is expected to generate a relevant response based solely on its pre-trained knowledge and understanding of the prompt, without being shown how to answer similar questions beforehand.

This is different from **few-shot prompting**, where you provide a few examples to guide the model, or **fine-tuning**, where the model is trained on a specific dataset.

---

## Key Characteristics

- **No examples**: The prompt contains only the task or question.
- **Relies on model knowledge**: The model uses its pre-trained data to infer the answer.
- **Flexible**: Useful for tasks where you don't have labeled examples.

---

## Examples of Zero-Shot Prompting

Below are five examples. Each shows the **input prompt** (in a highlighted box) and the **model output** (as it might appear from an LLM).

---

### Example 1: Text Summarization

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

### Example 2: Language Translation

**Prompt:**
```
Translate the following English sentence to French:

"The weather is beautiful today."
```

**Model Output:**

<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Le temps est magnifique aujourd'hui.
</div>

---

### Example 3: Sentiment Analysis

**Prompt:**
```
What is the sentiment of this review? "The product arrived late and was damaged. Very disappointed."
```

**Model Output:**

<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
Negative
</div>

---

### Example 4: Code Generation

**Prompt:**
```
Write a Python function that returns the square of a number.
```

**Model Output:**

<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
<pre>
<code>def square(number):
    return number * number
</code>
</pre>
</div>

---

### Example 5: Question Answering

**Prompt:**
```
Who wrote the play "Romeo and Juliet"?
```

**Model Output:**

<div style="border:1px solid #ccc; border-radius:6px; padding: 16px 12px; background:#ffffff; margin: 8px 0;">
William Shakespeare
</div>

---

## Summary

Zero-shot prompting allows you to leverage the power of LLMs for a wide range of tasks without needing to provide examples. This makes it a powerful tool for rapid prototyping and general-
