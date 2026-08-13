# ProjectFoundry

**Where AI Starts the Project.**

ProjectFoundry is an open-source platform that transforms ideas into fully structured open-source repositories. By analyzing social media posts, concept descriptions, or shared ideas, ProjectFoundry uses AI to assist in generating a repository complete with documentation, project structure, and starter code. A human in the loop initiates every project and makes all final decisions to ensure quality and alignment with project goals.

Each repository includes a **notice.md** file denoting all contributors as well as the original author. This ensures proper attribution for all contributions.

---

# Vision

ProjectFoundry bridges the gap between idea and execution. Instead of ideas being lost in social feeds or discussions, ProjectFoundry turns them into real projects ready for developer collaboration.

---

# Core Features

## Human-in-the-Loop Project Initiation

A human reviews and approves every project idea before any repository is created. All final decisions on structure, naming, documentation, and technology are made by the human to maintain project quality.

---

## AI Idea Extraction

AI assists by analyzing a post or concept description to extract:

- Project name  
- Project purpose  
- Suggested technology stack  
- Architecture outline  
- Core features  
- Development roadmap  

---

## Automatic Repository Generation

ProjectFoundry generates a repository on Codeberg including:

- Repository naming conventions  
- Directory structure  
- README.md  
- License (AGPL 3.0+)  
- CONTRIBUTING.md   
- docs/Workflow.md  
- notice.md  
- Starter code based on detected technologies  

---

## Project Documentation

Each repository includes:

README.md  
License  
CONTRIBUTING.md   
notice.md    

Additional documentation may include:

docs/Workflow.md
docs/concept.md  
docs/architecture.md  
docs/api-spec.md  

---

## Smart Project Structure

ProjectFoundry generates a development-ready structure such as:

project-name/

README.md  
License  
CONTRIBUTING.md  
notice.md  

/docs  
Workflow.md  
concept.md  
architecture.md  
api-spec.md 

/src  
backend/  
frontend/  

/tests  

/data  

.forgejo  
issue_templates  
pull_request_template.md  

---

## Starter Code Generation

Based on detected technologies, ProjectFoundry generates starter code.

Python Projects:  

requirements.txt  
main.py  

Node.js Projects:  

package.json  
server.js  

Rust Projects:  

Cargo.toml  
src/main.rs  

---

## Automatic Issue Generation

ProjectFoundry can create starter issues to guide contributors:

- good first issue  
- help wanted  
- documentation improvements  
- feature requests  
- MVP tasks  

---

# Example Workflow

1. A human selects and approves an idea or pastes a link to a social media post.  
2. ProjectFoundry AI analyzes the idea to suggest project structure and starter code.  
3. The human reviews and finalizes the repository structure and content.  
4. The repository is created with documentation, workflow, license, and starter code.  
5. Developers begin contributing immediately.  

---

# Example Use Case

Idea:  

> "Create an open-source database to track freelance wages worldwide."

ProjectFoundry generates:

Repository: freelance-wage-map  
License: AGPL 3.0+  
Stack: Python + PostgreSQL + React  

Generated files include:

README.md  
License    
CONTRIBUTING.md  
notice.md  
docs/Workflow.md  
Architecture and concept docs  
Starter backend code  

---

# Tech Stack

Backend: Python, FastAPI, PostgreSQL, Redis, Celery  
AI Layer: LangChain, OpenAI or local LLMs, LlamaIndex  
Scraping / Data Ingestion: Playwright, BeautifulSoup, platform APIs  
Git Integration: Forgejo API, GitPython  
Frontend: Next.js, React, Tailwind CSS  
Infrastructure: Docker, Kubernetes (optional)  

---

# Contributing

We welcome developers, designers, writers, and researchers.

Ways to contribute:

- Improve AI idea parsing  
- Expand project templates  
- Build integrations with social platforms  
- Enhance documentation  
- Add new workflow automation  

See notice.md for contributor attribution requirements.

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/projectfoundry/](https://roxanneardary.com/projectfoundry/)

---

# License & Notice Requirements

ProjectFoundry is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- ProjectFoundry specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
