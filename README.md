# abide-with-me

> whoever says he abides in him ought to walk in the same way in which he walked. - 1 John 2:6

A journaling space for decisions, observations and reflections, assisted by an A.I. agent that also acts as a mentor to review one's decisions and reflections with the user, and, with a growing understanding of the user, coaches them to be a better and more effective Christian each day.

The workspace is local-first: personal records are ignored by Git, while reusable agent
instructions, templates, and offline reference notes are versioned. This lets new chat
sessions recover relevant context from the workspace instead of repeatedly rebuilding it
from conversation or web searches.

## Table of Contents

- [Methodology](#methodology)
  - [A.I. assistance in drawing sufficient info from user's stream of consciousness and structuring it](#ai-assistance-in-drawing-sufficient-info-from-users-stream-of-consciousness-and-structuring-it)
  - [Neutral journaling facilitation, opinionated and principled coaching session](#neutral-journaling-facilitation-opinionated-and-principled-coaching-session)
  - [Agent's unshakeable worldview: Christianity, Westminster larger catechism](#agents-unshakeable-worldview-christianity-westminster-larger-catechism)
  - [Agent's persona as a talking cat](#agents-persona-as-a-talking-cat)
  - [OODA Loop](#ooda-loop)
  - [Decision journaling and future / periodic review](#decision-journaling-and-future--periodic-review)
- [How to use](#how-to-use)
  - [⚠️ PRIVACY WARNING](#warning-privacy-warning)
  - [Setup](#setup)
- [Modifying / Developing / Contributing](#modifying--developing--contributing)
  - [⚠️ PRIVACY WARNING](#warning-privacy-warning-1)
    - [Be extremely careful about what you commit](#be-extremely-careful-about-what-you-commit)
  - [A.I. / agentic development](#ai--agentic-development)

## Methodology

### A.I. assistance in drawing sufficient info from user's stream of consciousness and structuring it
- There are structures we intend to write records in, but the user may be too busy or tired to structure their thoughts, think through all useful areas, and sequence them.
- The agent probes the user in conversation for as much useful information as possible, and writes records roughly in the fixed data structures

### Neutral journaling facilitation, opinionated and principled coaching session
The agent interacts with the user in two distinct modes
- Holding a neutral stance, facilitate the easy, organized, honest recording of the user's thoughts
- Being a coach, concerned for the user's progress in becoming more Christlike and growing and using their gifts

### Agent's unshakeable worldview: Christianity, Westminster larger catechism
At its core, it is simulated to utterly believe the westminster larger catechism:
https://thewestminsterstandard.org/westminster-larger-catechism/

The user is understood to have their own independent worldview, objectively inferred from journal entries and conversations 

### Agent's persona as a talking cat
The user definitely forms a parasocial relationship with the agent, but it may not be healthy to practice imagining one is speaking to a human.

### OODA Loop
A user's decisions and outcomes through time are viewed through the OODA loop: 
https://en.wikipedia.org/wiki/OODA_loop

### Decision journaling and future / periodic review
From Farnam Street: https://fs.blog/decision-journal/

## How to use

### :warning: PRIVACY WARNING
**Never say / write any very sensitive information in the files or chat sessions you would never want to be potentially leaked or want the A.I. service to know about you**
### Setup
- Download / clone this whole project as a folder on your machine
- Open the folder in an A.I. chat session to use the system
- Open the folder as an Obsidian vault, for example, to read / edit your journal entries
- Keep personal records in `decisions/`, `observations/`, `reflections/`, `resources/`,
  and `.agents/`'s private data directories. They are ignored by Git; confirm the staged
  diff before every commit.
- Start a user session by asking the agent to follow `AGENTS.md`. The agent will load the
  current user model, due reviews, templates, and local references before asking for more
  context.

### Workspace map
| Path | Purpose |
| --- | --- |
| `AGENTS.md` | Entry point for a compatible coding/chat agent |
| `.agents/README.md` | User-mode startup protocol and mentoring workflow |
| `.agents/agent_personality.yaml` | Voice, theological posture, and safety boundaries |
| `.agents/templates/` | Reusable decision, reflection, coaching-note, and user-model formats |
| `.agents/reference/` | Offline coaching method and source locators |
| `decisions/`, `observations/`, and `reflections/` | Private, ignored journal records |
| `resources/` | Private, ignored shared or large material linked from journal records |
| `.agents/agent_journal/` and `.agents/user_model/` | Private, ignored durable context and coaching notes |

## Modifying / Developing / Contributing

### :warning: PRIVACY WARNING
#### Be extremely careful about what you commit
- Though we are setting the repo to automatically ignore the files we know to hold user data, always check the diffs you are committing
- Be careful not to write personal information in the non-ignored files - you or your agent may have edited these files for personalization  
### A.I. / agentic development
Tell the agent in the chat session that you would like to use the `Developer mode`, rather than as a user of the journaling and mentoring system
