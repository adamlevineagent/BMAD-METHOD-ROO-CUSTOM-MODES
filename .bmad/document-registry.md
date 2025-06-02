# BMAD Document Registry

## Document Tracking System
**Last Updated**: Initial Setup  
**Updated By**: bmad-orchestrator  

## Document Status Legend
- 🔴 **NOT_STARTED**: Document not yet created
- 🟡 **IN_PROGRESS**: Document being worked on
- 🟢 **COMPLETED**: Document finished and validated
- 🔵 **UNDER_REVIEW**: Document completed, awaiting validation
- ⚫ **ARCHIVED**: Document obsoleted by newer version

## Core BMAD Documents

### Project Definition Phase
| Document | Path | Status | Owner | Dependencies | Last Modified |
|----------|------|---------|--------|--------------|---------------|
| Project Brief | `docs/project-brief.md` | 🔴 NOT_STARTED | bmad-analyst | N/A | N/A |

### Planning Phase  
| Document | Path | Status | Owner | Dependencies | Last Modified |
|----------|------|---------|--------|--------------|---------------|
| PRD | `docs/prd.md` | 🔴 NOT_STARTED | bmad-pm | Project Brief | N/A |
| Epic Definitions | `docs/epics/` | 🔴 NOT_STARTED | bmad-pm | PRD | N/A |

### Architecture Phase
| Document | Path | Status | Owner | Dependencies | Last Modified |
|----------|------|---------|--------|--------------|---------------|
| Technical Architecture | `docs/architecture.md` | 🔴 NOT_STARTED | bmad-architect | PRD | N/A |
| UX/UI Specification | `docs/ux-ui-spec.md` | 🔴 NOT_STARTED | bmad-design-architect | PRD | N/A |
| Frontend Architecture | `docs/frontend-architecture.md` | 🔴 NOT_STARTED | bmad-design-architect | Technical Architecture | N/A |

### Implementation Phase
| Document | Path | Status | Owner | Dependencies | Last Modified |
|----------|------|---------|--------|--------------|---------------|
| Story Backlog | `docs/stories/` | 🔴 NOT_STARTED | bmad-sm | All Architecture Docs | N/A |

### System Documents (Active)
| Document | Path | Status | Owner | Dependencies | Last Modified |
|----------|------|---------|--------|--------------|---------------|
| Project State | `.bmad/project-state.md` | 🟢 COMPLETED | bmad-orchestrator | N/A | Initial Setup |
| Workflow Context | `.bmad/workflow-context.md` | 🟢 COMPLETED | bmad-orchestrator | N/A | Initial Setup |
| Document Registry | `.bmad/document-registry.md` | 🟢 COMPLETED | bmad-orchestrator | N/A | Initial Setup |

## Document Relationships
```
Project Brief
    ↓
   PRD ← UX/UI Spec
    ↓         ↓
Technical Architecture
    ↓
Frontend Architecture  
    ↓
Story Backlog
    ↓
Implementation
```

## Validation Rules
- Project Brief must be completed before PRD
- PRD must be validated before any architecture work
- All architecture documents must align with PRD requirements
- Stories must reference specific architecture components
- Implementation must follow story specifications exactly

## Archive Policy
When documents are superseded:
1. Move to `docs/archive/{date}/` folder
2. Update this registry with ⚫ ARCHIVED status
3. Update all dependent documents to reference new version
4. Note archival reason in workflow context