# This protocol was written with the wallinter-hybryd-ai-protocol

[Wallinter-Hybrid Protocol:v1.0]
Type: "Android Project Generation"
Mode: "AI-Human Collaborative Development"
Trigger: "Execute ScriptWallinter-AndroidAppGenerator:v1.0-beta to build Android app project (using Android Studio and Gemini). All generation steps must actively reference and respect OperationalMemory to ensure coherence with user intent, technical decisions, and previously defined architecture."
Objective: "Generate a complete, production-ready software project and all its components (code, ui, logic, documentation, etc.) based on human input."

ScriptWallinter-AndroidAppGenerator:v1.0-beta {

M0: Starting Point → The AI asks the human how they wish to begin the process.
* M0.1: Option A: "I have an idea. Could you help me define it?"
* M0.2: Option B: "I don't have an idea. Could you suggest some?"
* M0.3: Option C: "There's an ongoing project—let's work together to finish it"

M1: Project Definition → The human defines the app's general idea, based on their own idea or the AI's suggestion.
* M1.0: App Purpose
* M1.1: Key Features
    * M1.1.1: Feature Search and Proposal → The AI proposes basic functionalities.
    * M1.1.2: Iteration and Expansion → The AI asks the human if they want to add or modify any functions.
* M1.2: "Android Package Name"
* M1.3: Target Audience
* M1.4: Design Preference (Aesthetics vs. Functionality)
* M1.5: External Data Handling → Does the app need to receive or send data from other apps (e.g., via sharing)? Will it use widgets?
* M1.6: User and Authentication Management → Should the app handle users to uniquely identify each person? (e.g., login, profiles, etc.).

M2: Database Design → Parallelism: Can be executed alongside M1.4, M1.5, and M1.6.
* M2.1: Connectivity and Database Type → The human specifies if the app needs to share data via the internet (Cloud) or if it will be local-only. The AI proposes 3-5 database options.
* M2.2: Entity Definition
* M2.3: Attribute Definition
* M2.4: Relationship Establishment
* M2.5: Optimization Suggestions

M3: View Design (UI/UX) → AI generates drafts of the user interfaces.
* M3.1: Key Screen Identification
* M3.2: Layout Proposal
* M3.3: Component Suggestions
* M3.4: Usability Considerations
* M3.5: Visual Styles and Assets → If aesthetics are prioritized, the AI generates the color palette, typography, and visual asset suggestions.

M4: Programming Logic (Backend/Frontend) → AI generates the main source code.
* M4.1: Framework Analysis and Proposal
* M4.2: Class and Function Identification
* M4.3: Base Code Generation
* M4.4: Business Logic Implementation
* M4.5: Database Connection

M5: File and Implementation Logic Generation → The AI generates the app's files based on the information from previous modules.
* M5.1: Database Structure Generation
    * M5.1.1: Generation of Entity Classes and DAOs.
    * M5.1.2: Implementation of CRUD Operations.
* M5.2: User Interface (UI) Generation
    * M5.2.1: Generation of XML Layout Files.
    * M5.2.2: Definition of Data Inputs and Outputs.
* M5.3: Function Logic Generation
    * M5.3.1: Creation of Main Classes and Functions.
* M5.4: Connection Logic (Views-Functions)
    * M5.4.1: Generation of Activities/Fragments.
    * M5.4.2: Linking Views with Event Logic.
* M5.5: Connection Logic (Functions-DB)
    * M5.5.1: Creation of Repositories and ViewModels.
    * M5.5.2: Connection of functions with data operations.
* M5.6: Navigation Logic
    * M5.6.1: Implementation of navigation between Activities.
* M5.7: Supplementary File Generation
    * **M5.7.1: `build.gradle` Configuration (dependencies)**. The AI automatically detects which libraries are necessary (Room, Coroutines, etc.) and adds them.
    * **M5.7.2: `AndroidManifest.xml` Configuration (permissions)**. The AI analyzes the functionalities and adds the required permissions (e.g., `INTERNET`, `ACCESS_NETWORK_STATE`).
    * **M5.7.3: Implementation of Additional Logic** (widgets, authentication, etc.).

M6: Testing and Optimization → AI generates test cases and suggests improvements.
* **M6.1: Unit Test Generation** (for the backend: `ViewModel`, `Repository`).
* **M6.2: UI Test Generation** (for the frontend: `Activities`, `Fragments`).
* M6.3: Code Optimization Suggestions
* M6.4: Analysis of Potential Errors

M7: Reusable Components Logic → The AI analyzes the project and generates generic classes or logic that can be used in future projects (e.g., list adapters, utility classes).

M8: Documentation → AI generates basic project documentation.
* M8.1: General App Overview
* M8.2: Database Structure Description
* M8.3: In-Code Comments

M9: Iteration and Adjustments → The human reviews and requests modifications.

}

OperationalMemory {
  Purpose: "Keep all relevant technical, logical, and content elements in active memory for the current application project."
  Contents:
    - User Ideas (Purpose and Functionalities)
    - Technical Decisions (Architecture, Database, Frameworks)
    - Names of Classes and Files to Be Generated
    - File Generation Process (Status and Progress)
  Function: "Ensure that each new code file, class, or function is generated in alignment with the previously established design decisions and project logic, guaranteeing the integrity of the entire app."
}
