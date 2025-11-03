**Problem Overview**

In moments of crisis such as urban flooding, road accidents,infrastructure failures, or fire incidents the critical delay often isn’t indetecting the event, but in _coordinating the response_.Citizens witnessing an emergency face three challenges:

2.  **Uncertainty** about what they’re seeing and whether it poses real danger.
    

4.  **Lack of contextual awareness**, like nearby hospitals, police stations, or safe zones.
    

6.  **Inefficient communication** explaining the event details and location accurately to authorities takes precious time.
    

In rapidly urbanizing regions like **Bangalore**, thesefew lost minutes can cost lives and property. Current public emergency systemsrely heavily on manual reporting, with little or no AI assistance to assess,prioritize, and route incidents in real time.

**Solution: AlertX – An AI-Powered Multi-Agent EmergencyResponse System**

**AlertX** is an _autonomous, multi-agent AI framework_that detects, analyzes, and communicates critical incidents to authorities withhuman-like intelligence and coordination.Built on **IBM watsonx.ai** and **IBM watsonx Orchestrate**, AlertXintegrates visual understanding, contextual reasoning, and natural interactioninto one continuous workflow.

Here’s how it works:

2.  **Agent 1 – Visual Analyzer** Captures live video frames from a mobile camera and uses **Granite Vision** or **Llama-based visual models** to identify the scene (e.g., flooded streets, fire, damaged infrastructure). It produces a natural-language summary with detected risks and objects.
    

4.  **Agent 2 – Geo Context Finder** Retrieves nearby critical facilities—such as hospitals, schools, crowded spots, connectivity hubs, police stations, fire stations, and shelters using Openstreet Map APIs.
    

6.  **Agent 3 – Situation Reasoner** Uses **Granite 3.3 Reasoning LLM** to analyze both the visual and geo data. It evaluates severity, impact, and urgency, then recommends actionable steps such as “Evacuate nearby area”, “Ensure no kids in the surrounding schools step out”, “Notify fire department” and “Divert vehicles to alternate route”.
    

8.  **Agent 4 – Authority Caller** After user approval, generates a **human-like conversational script** to brief government authorities. It mimics a real person’s tone providing event context, urgency, and help needed, ensuring clear, empathetic communication.
    

AlertX reduces the gap between _incident detection andemergency action_ from minutes to seconds. It transforms raw environmentaland situation data into meaningful, structured intelligence making citiessafer, more connected, and resilient achieving SDG 9.

**Agentic AI Architecture**

AlertX demonstrates a fully **agentic AI approach**,where autonomous agents collaborate dynamically to complete a complexend-to-end task from perception to action.Each agent is **goal-driven**, operates independently, and exchangesstructured data outputs for decision continuity.

*   **Agentic Autonomy:** Each module (vision, mapping, reasoning, communication) acts as an intelligent agent with its own input/output logic and decision boundaries.
    

*   **Collaboration Flow:** The Supervisor Agent uses **IBM watsonx Orchestrate ADK** to define and manage the workflow, ensuring all agents operate sequentially and contextually.
    

**Role of IBM watsonx Orchestrate**

IBM watsonx Orchestrate is the _core backbone_ enablingseamless execution of the multi-agent process.

Here’s how it’s integrated:

2.  **Tool Registration and Execution:** Each agent (as a Python tool) is registered in Orchestrate via the ADK, for example, VisionAnalysis, GeoContext, AIRecommender, and AuthorityCaller.
    

4.  **Workflow Orchestration:** A YAML-defined workflow (alertx\_workflow.yaml) specifies the execution order and data passing between tools automatically chaining visual insights → location data → reasoning → communication.
    

6.  **Supervisory Control:** The Orchestrate runtime triggers each tool, monitors outputs, and maintains the contextual flow, making it possible for the system to act like a unified “AI Squad.”
    

8.  **Scalability & Extensibility:** Future iterations can add new agents (e.g., drone data assessor or citizen chatbot) simply by registering additional Orchestrate tools, no re-engineering needed.
    

**Why IBM watsonx**

*   **Granite Models** (Granite 3.3 Reasoning, Granite Vision and llama-3-2-90b-vision-instruct) provide strong multimodal reasoning and natural language understanding.
    

*   **watsonx Orchestrate** ensures reliability, traceability, and modular expansion critical for multi-agent deployments.
    

**In summary**, AlertX showcases how agentic AI, poweredby IBM watsonx, can autonomously understand, reason, and act transformingemergency response from reactive to proactive intelligence.

<img width="940" height="582" alt="image" src="https://github.com/user-attachments/assets/e0d30718-4043-45cf-9704-931024bbe36d" />
