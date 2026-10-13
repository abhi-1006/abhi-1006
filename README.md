<h1 align="center">Hi, I'm Abhiram Aedunoothala 👋</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1200&color=F7B731&center=true&vCenter=true&width=620&lines=CS+student+%40+University+of+Michigan;Building+agentic+AI+with+LangGraph+%2B+RAG;Shipping+cross-platform+apps+in+React+Native" alt="Typing intro" />
</p>

<p align="center">
  <a href="https://abhiram-aedunoothala.vercel.app"><img src="https://img.shields.io/badge/Website-abhiram--aedunoothala-F7B731?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Personal website" /></a>
  <a href="https://www.linkedin.com/in/abhiram-aedunoothala"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:avsabhiram1006@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://focztrek.vercel.app"><img src="https://img.shields.io/badge/Live_demo-FoczTrek-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="FoczTrek live demo" /></a>
</p>

---

### 🧭 About me

- 🎓 **Computer Science at the University of Michigan** (2026–2029), transferred from Penn State (GPA 3.7, Dean's List, President Walker Award)
- 🤖 Building **agentic AI systems**: LangGraph workflows, hybrid RAG, multi-agent review, LLM evaluation
- 📱 Building **cross-platform apps** with React Native, TypeScript and Expo
- 🧑‍🏫 Learning Assistant for MATH 110 at Penn State
- 🏸 Competitive badminton player, state and national level in India

---

### 🚀 Featured projects

<table>
<tr>
<td width="50%" valign="top">

#### 🏦 [WealthPilot](https://github.com/abhi-1006/wealthpilot)
**SME loan underwriting & credit research assistant**
<sub>IIT Hyderabad Applied AI capstone · 2026</sub>

An agentic system that parses loan applications, scores risk with a tool-calling agent, answers policy questions with RAG, and routes decisions through a human approval gate and a multi-agent review committee.

`Python` `LangGraph` `RAG` `Qdrant` `MCP` `FastAPI` `Langfuse`

</td>
<td width="50%" valign="top">

#### 🏔️ [FoczTrek](https://github.com/abhi-1006/FoczTrek) · [Live ↗](https://focztrek.vercel.app)
**Student productivity app**
<sub>Duke University research project · 2024–25, rebuilt 2026</sub>

Plan with the Eisenhower Matrix, learn why you procrastinate, then work through Pomodoro focus sessions while a hiker climbs the mountain. Points, streaks and ranks keep you coming back.

`TypeScript` `React Native` `Expo Router` `React Native Web` `Jest`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 💡 [Distraction-Free Study Lamp](https://github.com/abhi-1006/Distraction-Free-Study-Lamp)
**Hardware focus timer**
<sub>2025</sub>

Two Micro:bits talk over radio: one runs a Pomodoro timer, the other uses its light sensor to notice when you pick up your phone, and the timer pauses until you put it back.

`MicroPython` `Micro:bit` `Radio` `3D printing`

</td>
<td width="50%" valign="top">

#### ✨ What ties them together
I like building tools that help people **focus and decide better**, from a study lamp to a focus app to an AI assistant that helps lenders make careful, explainable credit decisions.

</td>
</tr>
</table>

<details>
<summary><b>🔍 WealthPilot: how it works and results</b> (click to expand)</summary>
<br>

| Piece | What it does |
|---|---|
| Intake | LLM parses raw applications into validated Pydantic models, with a repair loop for malformed output |
| Risk agent | Tool-calling agent that scores applicant risk |
| Policy RAG | Gemini embeddings in Qdrant + BM25 hybrid search + RRF fusion + cross-encoder reranking; answers must cite their sources |
| Workflow | LangGraph with a real `interrupt()` human approval gate and a durable SQLite checkpointer (resumes a paused run from disk) |
| Committee | An LLM analyst writes the memo; deterministic risk and compliance critics check it, with enforced per-agent write scopes. Credit-bureau data comes from an MCP server |
| Reliability | Langfuse tracing, retries with fallback, and a circuit breaker, tested under seeded fault injection |

**Results**
- Retrieval MRR **0.74 → 1.00** (dense → hybrid → hybrid + rerank) on a 10-question test set
- **19/20** on the policy golden evaluation set (started at 6/20; two real bugs found and fixed)
- **1.0** on faithfulness and groundedness across three LLM-judge frameworks (Ragas, DeepEval, TruLens)
- Under seeded fault injection, valid credit-bureau lookups rose **45% → 85%** with retries; the rest fell back to a flagged record instead of crashing

</details>

<details>
<summary><b>🔍 FoczTrek: architecture and v2 rebuild</b> (click to expand)</summary>
<br>

Started during a research internship with **Duke University (Dr. Eric Fouh)**, then rebuilt in 2026:

| | v1 (2024–25) | v2 (2026) |
|---|---|---|
| Screens | 20 duplicated screens | 9 Expo Router routes built from 20 reusable components |
| Screen code | 2,867 lines | 549 lines (**−81%**) |
| State | Passed screen to screen | React Context + `useReducer`, saved with AsyncStorage |
| Gamification | Visual progress only | Points, daily streaks, ranks |
| Web bundle | 1,579 KB JS | 983 KB JS (**−38%**) |
| Tests | 1 | 38 (Jest + React Native Testing Library) |

<p>
  <img src="https://raw.githubusercontent.com/abhi-1006/FoczTrek/main/docs/screenshots/matrix.jpg" width="190" alt="Eisenhower matrix screen" />
  <img src="https://raw.githubusercontent.com/abhi-1006/FoczTrek/main/docs/screenshots/focus.jpg" width="190" alt="Focus timer screen" />
  <img src="https://raw.githubusercontent.com/abhi-1006/FoczTrek/main/docs/screenshots/complete.jpg" width="190" alt="Session complete screen" />
</p>

</details>

---

### 🛠️ Tech stack

**Languages**
<p>
  <img src="https://skillicons.dev/icons?i=py,cpp,ts,js,html,css,r&perline=7" alt="Python, C++, TypeScript, JavaScript, HTML, CSS, R" />
</p>

**Frameworks & tools**
<p>
  <img src="https://skillicons.dev/icons?i=react,nodejs,fastapi,git,github,vscode,figma&perline=7" alt="React, Node.js, FastAPI, Git, GitHub, VS Code, Figma" />
</p>

**AI & LLM engineering**
<p>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/RAG-6E40C9?style=flat-square" alt="RAG" />
  <img src="https://img.shields.io/badge/Multi--Agent_Systems-0E7490?style=flat-square" alt="Multi-Agent Systems" />
  <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square" alt="Qdrant" />
  <img src="https://img.shields.io/badge/MCP-111111?style=flat-square" alt="Model Context Protocol" />
  <img src="https://img.shields.io/badge/Langfuse-0F172A?style=flat-square" alt="Langfuse" />
  <img src="https://img.shields.io/badge/Ragas_·_DeepEval_·_TruLens-4B5563?style=flat-square" alt="Ragas, DeepEval, TruLens" />
</p>

**Mobile & web**
<p>
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React Native" />
  <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white" alt="Expo" />
  <img src="https://img.shields.io/badge/Expo_Router-4630EB?style=flat-square&logo=expo&logoColor=white" alt="Expo Router" />
  <img src="https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white" alt="Jest" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel" />
</p>

---

<p align="center">
  <i>Open to software engineering and AI internships. Let's talk!</i><br><br>
  <a href="https://abhiram-aedunoothala.vercel.app">Website</a> ·
  <a href="https://www.linkedin.com/in/abhiram-aedunoothala">LinkedIn</a> ·
  <a href="mailto:avsabhiram1006@gmail.com">Email</a> ·
  <a href="https://focztrek.vercel.app">FoczTrek demo</a>
</p>
