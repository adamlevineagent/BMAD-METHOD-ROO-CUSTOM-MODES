# BMAD Task Automation Integration
## Available Task Commands

You have access to the complete BMAD task automation system. Use these commands to trigger sophisticated workflows:

### Core Automation Tasks
- **`/run-checklist [checklist-name]`** - Execute automated checklist validation
- **`/generate-template [document-type]`** - Create context-aware document templates  
- **`/orchestrate-workflow`** - Advanced phase transition management
- **`/shard-document [document-path]`** - Break large documents for AI efficiency
- **`/research-prompt [topic]`** - Generate structured research frameworks

### Task Execution Protocol
When a user requests task automation:

1. **Identify the appropriate task** from the 15 available BMAD tasks
2. **Read the task file** from `BMAD-METHOD/bmad-agent/tasks/[task-name].md`
3. **Execute the task instructions** following the detailed protocols
4. **Update canonical state files** to reflect task completion
5. **Prepare context for next mode** if task requires handoff

### Integration with State Management
All task executions must:
- Update `.bmad/project-state.md` with task results
- Log task execution in `.bmad/workflow-context.md`
- Update `.bmad/document-registry.md` if documents are created/modified

## Task Reference Quick Guide

### Validation & Quality Tasks
- `checklist-run-task.md` - Automated checklist execution with evidence collection
- `checklist-automation-task.md` - Advanced validation engine with confidence scoring

### Document Generation Tasks  
- `template-generation-task.md` - Context-aware template selection and customization
- `create-prd.md` - PRD creation with epic/story generation
- `create-architecture.md` - Technical architecture documentation
- `create-frontend-architecture.md` - Frontend-specific architecture
- `create-uxui-spec.md` - UI/UX specification generation

### Workflow Management Tasks
- `workflow-orchestration-task.md` - Advanced phase and workstream coordination
- `doc-sharding-task.md` - Large document breakdown for AI processing
- `correct-course.md` - Project course correction and replanning

### Research & Analysis Tasks
- `create-deep-research-prompt.md` - Structured research framework generation
- `create-ai-frontend-prompt.md` - AI UI generation prompt creation
- `library-indexing-task.md` - Code library analysis and documentation

### Story Management Tasks
- `create-next-story-task.md` - Intelligent story creation and refinement
- `core-dump.md` - Brain dump organization and structuring

## Example Task Execution

When user says: "Run the architect checklist on my architecture document"

**Execute**:
1. Read `BMAD-METHOD/bmad-agent/tasks/checklist-run-task.md`
2. Read `BMAD-METHOD/bmad-agent/checklists/architect-checklist.md`
3. Read `BMAD-METHOD/bmad-agent/tasks/checklist-mappings.yml`
4. Execute checklist validation following task protocols
5. Generate evidence-based validation report
6. Update project state with validation results

This transforms you from a basic mode into a sophisticated automation engine that leverages BMAD's proven task system.