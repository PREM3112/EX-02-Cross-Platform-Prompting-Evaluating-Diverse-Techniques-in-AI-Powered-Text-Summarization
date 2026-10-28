# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

## AIM
To design prompts using different prompt structures.

## Scenario
Students should practice with one application, such as Text Summarization or a topic related to their project. Start with a Basic Prompt and progressively improve it through a Role Prompt, Context Prompt, Constraint Prompt, and Output Format Prompt.

1. Basic Prompt
2. Role Prompt
3. Context Prompt
4. Constraint Prompt
5. Output Format Prompt

## AI Tools Required
ChatGPT, Gemini

## Article: A Hybrid Blockchain–IPFS and Generative-AI Framework for Emergency Blood Resource Discovery

**Full research title:** A Hybrid Blockchain–IPFS and Generative-AI Framework for Emergency Blood Resource Discovery: Design and Prototype Evaluation  
**Authors:** Prem R and Tamil Pavalan M

### Article Text (Adapted from the Research Manuscript)

Emergency blood-resource discovery can be difficult because hospitals and blood banks maintain separate inventory records. Users may need to contact institutions individually to find the required blood group and quantity. Moreover, an electronic inventory record cannot, on its own, confirm that the blood is physically available at the hospital.

This research presents a hybrid framework combining Ethereum blockchain, the InterPlanetary File System (IPFS), Generative AI, and location-based mobile discovery. Ethereum stores auditable hospital registration states and compact inventory references. Detailed inventory metadata is maintained off-chain through IPFS, with a content identifier (CID) recorded on-chain. Administrator-controlled verification restricts inventory updates to registered, verified, and active hospital wallets in the evaluated contracts.

A Generative AI dispatch assistant using Gemini 2.5 Flash extracts structured information, including blood group, quantity, and urgency, from natural-language requests. The React Native mobile prototype displays hospitals on a map and provides navigation handoff. The AI assistant supports request extraction rather than clinical diagnosis or transfusion compatibility decisions.

The study evaluated matched-build smart contracts on Ethereum Sepolia, 50 synthetic English text queries, ten local authorization tests, and five preliminary mobile timing observations. For recurring changed-value updates, the fully on-chain baseline consumed 53,447 gas for small inventories and 68,731 gas for large inventories, whereas the hybrid consumed 47,817 gas in both cases. This corresponds to gas reductions of 10.53% and 30.43%, respectively. All 50 completed synthetic queries matched the three reference extraction fields, while 52 total attempts included two quota interruptions. Ten local authorization checks passed, and the five successful phone observations averaged 1,550.37 milliseconds to state-update scheduling.

The results apply to the evaluated components and workloads. The inspected mobile screen still uses a legacy contract interface and does not integrate the strict filtering helper or backend proxy. Multilingual and audio extraction, end-to-end correctness, real-world hospital deployment, and clinical effectiveness have not been established. In particular, blockchain integrity does not prove physical shelf stock; hospital confirmation remains necessary.

---

## Prompts

### Basic Prompt
Summarize the following research article.

---

### Role Prompt
You are an expert technical content summarizer. Summarize the following research article in a clear and concise manner.

---

### Context Prompt
You are an expert technical content summarizer.

The following article is intended for undergraduate engineering students working on a final-year project involving Blockchain, IPFS, and Generative AI.

Summarize the article while highlighting its main problem, proposed solution, technologies, and findings.

---

### Constraint Prompt
You are an expert technical content summarizer.

The following article is for undergraduate engineering students preparing for a final-year project review.

Summarize the article using these constraints:
- Keep the summary between 120 and 150 words.
- Include only the most important technical points and tested results.
- Preserve the actual numerical findings.
- Do not include personal opinions or unsupported claims.
- Use simple and easy-to-understand language.
- Explain at least one important limitation.

---

### Output Format Prompt (Final Prompt)
You are an expert technical content summarizer.

The following article is for undergraduate engineering students preparing for a final-year project review.

Instructions:
- Summarize the article in 120–150 words.
- Use clear and simple technical language.
- Include the problem, solution, technologies, experimental results, and limitations.
- Maintain a neutral, academic tone.
- Do not add information not present in the article.

Present the output in the following format:

**Title:**  
`<Short research title>`

**Summary:**  
`<120–150-word summary>`

**Key Takeaways:**
- Point 1
- Point 2
- Point 3
- Point 4
- Point 5

---

## Output

> **Note:** The outputs below are illustrative examples written from the supplied research article to show the five prompt structures. The Gemini section is a simulated example, not an independently captured Gemini response. The comparison ratings are the supplied example values rather than verified benchmark scores.

### ChatGPT

#### Basic Prompt
**Summary:**

The research introduces a hybrid Blockchain–IPFS and Generative AI framework for emergency blood-resource discovery. Ethereum maintains auditable hospital records, IPFS stores inventory information, and Generative AI extracts details from requests for blood. A mobile interface helps users locate hospitals on a map. The evaluated hybrid contracts used less gas than the fully on-chain baseline for two tested inventory workloads. However, the current prototype has integration limitations and cannot independently confirm physical blood availability.

---

#### Role Prompt
**Summary:**

The study proposes an Ethereum–IPFS architecture that anchors compact inventory references on-chain while keeping detailed hospital metadata in IPFS. Administrator-governed registration controls which hospital wallets may update reported inventory. A Gemini 2.5 Flash assistant extracts structured blood-group, quantity, and urgency information from natural-language requests, and a mobile map supports discovery and navigation.

For recurring changed-value updates, the hybrid implementation reduced gas use by 10.53% for small inventories and 30.43% for large inventories compared with the tested on-chain baseline. Its component evaluations also included 50 completed synthetic text queries and ten successful local authorization checks. These findings do not establish end-to-end correctness or actual shelf-stock availability.

---

#### Context Prompt
**Summary for Undergraduate Engineering Students**

This project studies how blockchain, decentralized storage, and Generative AI can support a hospital blood-resource discovery application.

The main components are:
- **Ethereum blockchain:** Maintains hospital registration status and auditable inventory references.
- **IPFS:** Stores detailed inventory metadata outside the blockchain.
- **Gemini 2.5 Flash:** Extracts blood group, quantity, and urgency from requests.
- **React Native and maps:** Display hospital locations and offer navigation handoff.

**Findings:** The hybrid approach saved 10.53% gas on small recurring inventory updates and 30.43% on large updates. All 50 completed synthetic English queries matched the expected extraction fields, and ten local authorization tests passed.

**Key Takeaway:** The research demonstrates useful component-level results. The mobile interface is not fully integrated with the evaluated contracts, and hospital-reported blood stock still requires confirmation.

---

#### Constraint Prompt
**Summary (120–150 words):**

The research proposes a hybrid Blockchain–IPFS and Generative AI framework for emergency blood-resource discovery. It addresses fragmented hospital inventory records by storing auditable registration states and inventory references on Ethereum while keeping detailed metadata on IPFS. Gemini 2.5 Flash extracts blood group, quantity, and urgency from natural-language requests. A React Native prototype displays hospital locations and provides navigation handoff. On Ethereum Sepolia, the hybrid contracts reduced recurring update gas by 10.53% for small inventories and 30.43% for large inventories compared with the evaluated on-chain baseline. All 50 completed synthetic English queries matched the three reference extraction fields, and ten local authorization checks passed. Five preliminary phone observations averaged 1,550.37 milliseconds to state-update scheduling. However, the inspected mobile screen uses a legacy contract interface, and the system cannot independently confirm physical blood availability. Further integration and real-world validation are needed.

---

#### Output Format Prompt
**Title:**  
Hybrid Blockchain–IPFS and Generative AI for Blood Discovery

**Summary:**

The research presents a hybrid framework to help users discover hospitals reporting required blood resources. Ethereum maintains auditable hospital registration states and inventory references, while IPFS stores detailed inventory metadata. Gemini 2.5 Flash extracts blood group, quantity, and urgency from natural-language requests. A React Native mobile prototype supports map-based hospital discovery and navigation. In matched-build Sepolia tests, hybrid recurring updates consumed 47,817 gas, saving 10.53% for small inventories and 30.43% for large inventories against the evaluated on-chain baseline. All 50 completed synthetic English queries matched the expected extraction fields, and ten local authorization checks passed. Five phone observations averaged 1,550.37 milliseconds to state-update scheduling. However, the inspected mobile screen uses a legacy contract interface, strict filtering is not fully integrated, and digital records cannot prove physical blood availability. End-to-end and real-world effectiveness remain unvalidated.

**Key Takeaways:**
- Ethereum records registration states and inventory references.
- IPFS stores detailed hospital metadata off-chain.
- Generative AI extracts structured blood-request information.
- Recurring update gas savings were 10.53% and 30.43% for the evaluated workloads.
- Physical stock requires hospital confirmation, and end-to-end validation remains incomplete.

---

### Gemini

> The following are **illustrative Gemini-style responses**, not outputs collected from a live Gemini session.

#### Basic Prompt
**Summary:**

The article describes an emergency blood-discovery prototype combining Ethereum blockchain, IPFS, Generative AI, and mobile mapping. Blockchain supports auditable records, while IPFS stores inventory metadata. The AI assistant extracts blood-request details, and the app helps users find hospitals reporting relevant blood groups. Tests showed lower recurring update gas for the hybrid design. Real-world effectiveness and the physical availability of blood remain unverified.

---

#### Role Prompt
**Executive Summary:**

The framework separates trusted inventory references from off-chain metadata and natural-language request processing.

**Core Components:**
- **Blockchain:** Auditable registration status and inventory references.
- **IPFS:** Content-addressed hospital metadata.
- **Generative AI:** Structured extraction of blood requests.
- **Mobile mapping:** Hospital discovery and navigation handoff.

**Experimental Findings:** The hybrid design reduced recurring update gas by 10.53% and 30.43% for small and large tested inventories, respectively.

**Limitations:** Contract benchmarks and local tests do not establish complete mobile integration or the truth of hospital-reported shelf stock.

---

#### Context Prompt
**Engineering Project Summary**

**Problem:** Blood-inventory records may be fragmented across institutions, making emergency discovery difficult.

**Solution:** The project integrates Ethereum, IPFS, Gemini 2.5 Flash, and a React Native hospital map. Ethereum keeps auditable hospital states and inventory references. IPFS stores detailed metadata. AI extracts relevant blood-request fields.

**Results:** Hybrid updates used 47,817 gas in both measured workloads, compared with 53,447 and 68,731 gas for the respective baselines. Fifty completed synthetic text queries matched the reference fields, and ten authorization checks passed.

**Conclusion:** The system demonstrates component-level feasibility, but practical inventory confirmation and end-to-end evaluation are still required.

---

#### Constraint Prompt
**Summary (120–150 words):**

The study develops a hybrid Blockchain–IPFS and Generative AI prototype for emergency blood-resource discovery. It responds to fragmented hospital inventory information by recording hospital registration states and inventory references on Ethereum, while IPFS stores detailed metadata. Gemini 2.5 Flash extracts blood group, quantity, and urgency from natural-language requests. A React Native interface presents hospitals on a map and supports navigation. Matched-build Sepolia testing found recurring gas savings of 10.53% for small inventory updates and 30.43% for large updates. All 50 completed synthetic English queries matched three reference fields, and ten local authorization checks passed. Five preliminary phone observations averaged 1,550.37 milliseconds to state-update scheduling. However, the inspected mobile screen still uses a legacy contract interface and lacks full strict-filtering integration. Neither blockchain nor IPFS can confirm physical inventory, so hospital confirmation and further real-world testing remain essential.

---

#### Output Format Prompt
**Title:**  
Hybrid Blockchain and AI for Emergency Blood Discovery

**Summary:**

The research proposes an emergency blood-resource discovery framework using blockchain, IPFS, Generative AI, and mapping. Ethereum stores auditable hospital registration states and inventory references, while IPFS maintains detailed metadata. Gemini 2.5 Flash extracts requested blood group, quantity, and urgency from natural-language input, and a React Native mobile interface supports hospital discovery. In Sepolia contract tests, recurring hybrid updates consumed 47,817 gas, compared with baseline values of 53,447 for small inventories and 68,731 for large inventories. These measurements correspond to reductions of 10.53% and 30.43%. All 50 completed synthetic English extraction queries matched reference fields, and ten local authorization tests passed. The inspected mobile screen, however, uses a legacy contract interface and does not fully integrate strict filtering. Physical availability is not verified by blockchain records. Additional end-to-end testing and hospital confirmation are therefore necessary.

**Key Takeaways:**
- Ethereum maintains auditable hospital states and inventory references.
- IPFS stores detailed inventory information off-chain.
- Generative AI extracts structured requests rather than making clinical decisions.
- The tested hybrid design reduced recurring gas in both workloads.
- Real-world deployment requires complete integration and confirmation of reported blood stock.

---

## Comparison Table

| Prompt Type | ChatGPT | Gemini |
|-------------|:-------:|:------:|
| Basic Prompt | **8.5/10** | **8.0/10** |
| Role Prompt | **9.2/10** | **9.0/10** |
| Context Prompt | **9.5/10** | **9.3/10** |
| Constraint Prompt | **9.8/10** | **9.7/10** |
| Output Format Prompt | **10/10** | **9.9/10** |
| **Overall Rating** | **9.4/10** | **9.2/10** |

> **Evaluation note:** These ratings were provided as example values and are not independently verified experimental measurements of ChatGPT or Gemini on this article. The overall ratings are reproduced as supplied rather than recalculated.

## Conclusion

This experiment illustrates how prompt structure can influence AI-generated research summaries. The Basic Prompt requests a general summary; the Role Prompt specifies expertise; the Context Prompt identifies the intended reader; the Constraint Prompt controls length, relevance, and accuracy; and the Output Format Prompt specifies the final presentation. The examples demonstrate that progressively detailed instructions can guide responses toward a clearer, more consistent academic format. To establish an empirical performance comparison, the same source article and prompts should be tested independently in ChatGPT and Gemini, and their actual responses scored against a common rubric.
