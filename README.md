# Challenging-problem
"The toughest challenge was making sure every AI-generated test case was strictly grounded in the actual project documents like product_specs.md, ui_ux_guide.txt, and checkout.html.
AI models tend to hallucinate missing requirements, so I had to build a RAG pipeline that:

parsed HTML and extracted stable selectors,

semantically chunked UI/UX and spec documents,

mapped each test case step to an exact source citation,

and validated whether a requirement actually existed or not.

Getting the grounding system stable required tuning embeddings, designing metadata filters, and running consistency checks. Once solved, the agent could generate 100% context-driven, non-hallucinated test cases."



 2. Designing Stable and Non-Brittle Selectors for Selenium

"Another big challenge was ensuring that automated Selenium tests don't break.
The HTML originally didn’t have stable selectors, so I had to redesign it with consistent IDs and name attributes. I avoided brittle XPath, used semantic CSS selectors, and validated each selector within the HTML’s DOM."


 3. Automating Interaction Across Multiple Layers (UI + Business Logic + Validation)

"The checkout flow involved cart updates, discount logic, shipping logic, and form validation — all updating in real time. Ensuring Selenium could reliably detect each change without flaky waits was challenging. I solved it using WebDriverWait with expected conditions and avoided any hard sleeps."



 4. Maintaining JSON Schema Compliance for 30+ Test Cases

"Another challenge was enforcing a strict JSON schema across all generated test cases.
AI-generated content easily deviates, so I added normalization, schema validators, and fallback formatting to guarantee consistency. This ensured the output could seamlessly plug into the Selenium automation pipeline."


 5. Testing Order of Operations in Dynamic Calculations

"One tricky part was validating the calculation order — (Subtotal - Discount) + Shipping.
Discount, shipping, and quantity changes are all reactive. I had to write test cases that validated not just the final numbers but the intermediate states. Ensuring accuracy under multiple interacting conditions was a challenge."
