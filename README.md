# Developer Experience (DevX) Coding Experiment
This repository supports a coding experiment designed to evaluate **developer experience (DevX)** when building a real-world, ontology-driven website using two different static site generators: **Hugo** and **11ty**. The experiment explores how tool choice affects setup, workflow, community support, cognitive load, and overall usability.

Two participants will implement the same use case — a sports club website built on a shared ontology over five sessions with a combined time limit of 20 hours each. All coding activities, reflections, and metrics are tracked through a structured developer diary and NASA-TLX surveys.

This project is done in the context of the masters course Coding Excellence (CEX) at TH Köln during summer semester 2025: [archi-lab.io](https://www.archi-lab.io)




## Experiment Structure and Guidelines
### Tasks and Scoring

- The project is divided into subtasks aligned with the ontology-driven website implementation
- Each subtask is scored on a standardized scale:
  - **0** = Not attempted
  - **1** = Attempted
  - **2** = Completed
  - **3** = Completed and styled
- Scores provide a quantifiable measure complementing qualitative diary insights
- Tasks may overlap and be revisited non-linearly

### Developer Diary and Documentation

For each coding session, participants must complete a **developer diary template** covering:

- Session Data: ID, date, duration, tasks, and completion ratings
- Tools & Resources: IDEs, AI assistants, documentation consulted
- Time Breakdown: Minutes spent on templating vs. data integration
- Challenges: Build issues, blocking problems, help-seeking behavior
- Outcomes: Goal achievement and confidence in repeating tasks

### Time and Session Management

- Each participant has up to **20 hours** across **5 sessions**
- Coding is not linear; tasks may be revisited across sessions
- After each session:
  - Commit and push all code with a clear session number in the commit message
  - Complete the developer diary and NASA-TLX survey
- AI assistance (e.g., large language models) is permitted but must be documented in the diary


## Repository Structure
```
/src
  /hugo          # Hugo-specific website implementation
  /11ty          # 11ty-specific website implementation

/diaries
  /CEX_diary_hugo.xlsx          # Developer diary for Hugo sessions
  /CEX_diary_11ty.xlsx          # Developer diary for 11ty sessions

/surveys
  /hugo          # NASA-TLX surveys for Hugo participant
  /11ty          # NASA-TLX surveys for 11ty participant

/ontology        # Shared ontology definition
/tasks           # Session Tasks for Coding Experiment
```

## Ontology Setup / Sports Club Website
Participants build a website based on a common ontology defining entities such as:

- SportsClub
- Team
- Member
- TrainingSession
- Tournament
- Result
- NewsItem
- MembershipApplication

## Hugo Phase 1: Hugo Implementation – Setup, Teams, Matches, Contact Page

This phase focused on setting up the Hugo-based static site and rendering dynamic content based on structured data. The implementation followed the shared ontology model for a sports club website.

###  Tasks Completed

- **Project Setup**
  - Initialized Hugo site using `hugo new site`
  - Installed and configured the Ananke theme
  - Verified local development with `hugo server`

- **Folder Structure Created**
  - Set up key directories: `content/`, `data/`, `layouts/`, `static/`

- **Dynamic Data Integration**
  - Created YAML files in `/data/` for:
    - `teams.yaml`: includes team details, coach, and player info
    - `matches.yaml`: includes match details and linked team IDs

- **Pages Implemented**
  - `/teams/`
    - Rendered team names, categories
    - Displayed coach and a list of players dynamically
    - Linked from navigation menu
  - `/matches/`
    - Match schedule list rendered dynamically from YAML
    - Team relationships displayed
  - `/contact/`
    - Contact form UI with basic HTML elements
    - Static form (no submission logic)
    - Page created using `content/contact/index.md` and a custom layout

- **Navigation**
  - Configured main menu in `config.toml`
  - Links added for Teams, Matches, and Contact

- **Templating**
  - Custom templates created in `layouts/_default/` for:
    - `teams.html`
    - `matches.html`
    - `contact.html`
  - Used Hugo's Go Template syntax for loops, data access, and page structure

### 📂 Folder Snapshot


