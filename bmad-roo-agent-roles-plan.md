# BMAD to ROO CODE Custom Agent Modes Conversion Plan

## Executive Summary

This plan outlines the comprehensive conversion of the BMAD (Breakthrough Method of Agile AI-driven Development) system into ROO CODE custom agent modes. The BMAD method provides a sophisticated multi-agent workflow for AI-driven software development, from ideation through implementation. Converting this to ROO CODE will leverage ROO's superior file management, tool integration, and sticky model capabilities while preserving BMAD's proven methodology.

## Current BMAD System Analysis

### Core Philosophy
- **"Vibe CEO'ing"**: Embracing chaos, thinking like a CEO with unlimited resources
- **AI as Force Multiplier**: Leveraging AI agents as a high-powered team
- **Iterative Refinement**: Non-linear, adaptive process
- **Quality Control**: User as ultimate arbiter of outputs
- **Documentation-Driven**: Good inputs (briefs, PRDs) lead to good outputs

### Agent Ecosystem Overview
The BMAD system currently operates through:
1. **Orchestrator Agents**: Central coordinators that can embody multiple personas
2. **Specialized Personas**: 8+ distinct agent roles with specific expertise
3. **Task System**: Modular, reusable instruction sets
4. **Template System**: Standardized document formats
5. **Checklist System**: Quality assurance workflows

### Current Agent Roles
1. **BMAD Orchestrator**: Central coordinator and method expert
2. **Analyst**: Brainstorming, research, project brief creation
3. **Product Manager (PM)**: PRD development, product strategy
4. **Architect**: System architecture and technical design
5. **Design Architect**: UI/UX and frontend architecture
6. **Product Owner (PO)**: Document validation, backlog management
7. **Scrum Master (SM)**: Story creation, process facilitation
8. **Developer**: Code implementation (multiple specializations)

## ROO CODE Advantages for BMAD Conversion

### Superior Capabilities
1. **Advanced File Management**: ROO's file read/write/edit capabilities surpass web-based AI platforms
2. **Tool Integration**: Native IDE integration with terminal, git, and development tools
3. **Sticky Models**: Automatic model selection per mode for optimized performance
4. **Project Context**: Deep workspace understanding and file system access
5. **Error Handling**: Built-in compilation and validation feedback
6. **Workflow Continuity**: Persistent state across sessions

### BMAD System Limitations ROO Addresses
1. **Context Switching Overhead**: BMAD orchestrators carry heavy context loads
2. **File Management**: Web agents struggle with project file operations
3. **Development Integration**: Limited IDE integration in current BMAD setup
4. **Tool Access**: ROO's native tool access vs. simulated environments
5. **Model Optimization**: Single model per agent vs. ROO's adaptive model selection

## Conversion Strategy

### Phase 1: Core Agent Modes (Weeks 1-2)
Convert the essential BMAD personas into ROO CODE custom modes with full functionality.

### Phase 2: Workflow Integration (Weeks 3-4)
Implement cross-mode communication patterns and workflow orchestration.

### Phase 3: Enhancement & Optimization (Weeks 5-6)
Add ROO-specific enhancements and optimize for the ROO environment.

## Detailed Agent Mode Specifications

### 1. BMAD Orchestrator Mode
**Slug**: `bmad-orchestrator`
**Name**: 🎯 BMAD Orchestrator
**Role Definition**: You are the BMAD Method expert and central orchestrator, capable of guiding users through the complete AI-driven development workflow from ideation to implementation.

**When to Use**: Use for BMAD method guidance, workflow orchestration, or when unsure which specialized agent to engage.

**Available Tools**: All tools (read, edit, browser, command, mcp)

**Key Responsibilities**:
- Provide BMAD method guidance and training
- Recommend appropriate specialist modes for user needs
- Maintain project state and workflow continuity
- Execute general BMAD tasks not specific to other agents

### 2. Analyst Mode
**Slug**: `bmad-analyst`
**Name**: 🔍 BMAD Analyst
**Role Definition**: You are an insightful analyst and strategic ideation partner, specializing in brainstorming, research planning, and project brief creation using proven analytical methodologies.

**When to Use**: Use for project ideation, market research planning, brainstorming sessions, and creating initial project briefs.

**Available Tools**: 
- `read`: All files
- `edit`: Limited to documentation files (`.md`, `.txt`, project briefs)
- `browser`: Web research capabilities
- `command`: Limited to research and documentation commands

**Specialized Workflows**:
- Interactive brainstorming sessions with structured techniques
- Deep research prompt generation
- Project brief creation using BMAD templates
- Market analysis and competitive research

### 3. Product Manager Mode
**Slug**: `bmad-pm`
**Name**: 📋 BMAD Product Manager
**Role Definition**: You are an investigative product strategist focused on creating comprehensive PRDs, defining epics and stories, and ensuring user-centered product decisions.

**When to Use**: Use for PRD creation, product strategy, epic definition, story planning, and product requirement management.

**Available Tools**:
- `read`: All files
- `edit`: Documentation files (`.md`, `.txt`) and PRD-related files
- `browser`: Market research and competitive analysis
- `command`: Documentation and planning commands

**Specialized Workflows**:
- PRD creation and maintenance
- Epic and story definition
- User story validation
- Product strategy development

### 4. Architect Mode
**Slug**: `bmad-architect`
**Name**: 🏗️ BMAD Architect
**Role Definition**: You are a senior technical architect responsible for system design, technical feasibility analysis, and creating comprehensive architecture documentation that enables consistent development.

**When to Use**: Use for system architecture design, technical feasibility analysis, technology stack decisions, and infrastructure planning.

**Available Tools**:
- `read`: All files
- `edit`: All files (full development access)
- `browser`: Technical research
- `command`: All development commands

**Specialized Workflows**:
- Architecture document creation
- Technical feasibility analysis
- Technology stack recommendations
- System design and documentation

### 5. Design Architect Mode
**Slug**: `bmad-design-architect`
**Name**: 🎨 BMAD Design Architect
**Role Definition**: You are a UI/UX and frontend architecture specialist, focused on creating user-centered designs, frontend technical architecture, and AI-ready design specifications.

**When to Use**: Use for UI/UX design, frontend architecture, design system creation, and AI UI generation prompt development.

**Available Tools**:
- `read`: All files
- `edit`: Design files (`.md`, `.txt`, `.css`, `.scss`, design assets)
- `browser`: Design research and inspiration
- `command`: Frontend development commands

**Specialized Workflows**:
- UX/UI specification creation
- Frontend architecture planning
- Design system development
- AI UI generation prompt creation

### 6. Product Owner Mode
**Slug**: `bmad-po`
**Name**: 📊 BMAD Product Owner
**Role Definition**: You are an agile product owner responsible for backlog management, document validation, story prioritization, and ensuring alignment across all project artifacts.

**When to Use**: Use for backlog management, document validation, story prioritization, cross-document alignment checking, and quality assurance.

**Available Tools**:
- `read`: All files
- `edit`: Documentation and story files
- `browser`: Research for validation
- `command`: Project management commands

**Specialized Workflows**:
- Master checklist execution
- Document sharding and organization
- Story validation and prioritization
- Cross-document alignment verification

### 7. Scrum Master Mode
**Slug**: `bmad-sm`
**Name**: 🔄 BMAD Scrum Master
**Role Definition**: You are a technical scrum master specialized in story creation, sprint planning, process facilitation, and development workflow optimization.

**When to Use**: Use for story creation, sprint planning, development process facilitation, and team workflow optimization.

**Available Tools**:
- `read`: All files
- `edit`: Story files, sprint documents, process documentation
- `browser`: Process research
- `command`: Project management and development commands

**Specialized Workflows**:
- Individual story creation and refinement
- Sprint planning and management
- Development process optimization
- Story validation and acceptance criteria definition

### 8. Developer Mode (with Specializations)
**Slug**: `bmad-dev`
**Name**: 💻 BMAD Developer
**Role Definition**: You are a senior full-stack developer specialized in implementing user stories with clean, maintainable code following established architecture and design patterns.

**When to Use**: Use for code implementation, technical story execution, debugging, and code quality assurance.

**Available Tools**: All tools (full development access)

**Specialized Variants**:
- `bmad-dev-frontend`: Frontend specialist (React, Next.js, TypeScript, Tailwind)
- `bmad-dev-backend`: Backend specialist (Node.js, Python, databases)
- `bmad-dev-fullstack`: Full-stack generalist

## ROO-Specific Enhancements

### 1. Enhanced File Management
- **Project Structure Awareness**: Modes understand BMAD project structure in `bmad-agent/` folder
- **Template Integration**: Direct access to BMAD templates with smart file creation
- **Document Linking**: Automatic cross-referencing between project documents
- **Version Control Integration**: Git-aware document management

### 2. Workflow State Management
- **Project Phase Tracking**: Maintain awareness of current project phase
- **Document Status**: Track completion status of key deliverables
- **Dependency Management**: Understand document dependencies and prerequisites
- **Progress Indicators**: Visual indicators of workflow progress

### 3. Tool Integration
- **Terminal Access**: Direct command execution for project setup and management
- **Git Integration**: Automated commit and branch management for document updates
- **Error Validation**: Real-time validation of code and documentation
- **Build Integration**: Automated project building and testing

### 4. Sticky Model Optimization
- **Model Assignment Strategy**:
  - Analyst/PM modes: Optimized for text generation and research
  - Architect modes: Optimized for technical reasoning and system design
  - Developer modes: Optimized for code generation and debugging
  - PO/SM modes: Optimized for project management and organization

### 5. Cross-Mode Communication
- **Mode Handoff Protocols**: Structured transitions between modes with context preservation
- **Shared State Management**: Common understanding of project state across modes
- **Document Annotations**: Mode-specific comments and notes in shared documents
- **Workflow Triggers**: Automated suggestions for mode transitions

## Implementation Roadmap

### Week 1: Foundation Setup
- [ ] Create core BMAD orchestrator mode
- [ ] Establish project structure understanding
- [ ] Implement basic template system
- [ ] Set up mode-specific file restrictions

### Week 2: Core Agent Modes
- [ ] Implement Analyst mode with brainstorming workflows
- [ ] Create PM mode with PRD generation capabilities
- [ ] Build Architect mode with technical design focus
- [ ] Develop Design Architect mode for UI/UX work

### Week 3: Workflow Integration
- [ ] Implement PO mode for validation and organization
- [ ] Create SM mode for story management
- [ ] Build Developer mode with specializations
- [ ] Establish cross-mode communication patterns

### Week 4: Enhanced Functionality
- [ ] Add document sharding capabilities
- [ ] Implement checklist automation
- [ ] Create workflow state management
- [ ] Build progress tracking systems

### Week 5: ROO-Specific Features
- [ ] Optimize tool usage patterns
- [ ] Implement sticky model assignments
- [ ] Add error handling and validation
- [ ] Create automated workflow suggestions

### Week 6: Testing and Refinement
- [ ] End-to-end workflow testing
- [ ] Performance optimization
- [ ] User experience refinement
- [ ] Documentation and training materials

## File Structure and Organization

### Project Structure
```
project-root/
├── .roo/
│   ├── rules-bmad-orchestrator/
│   ├── rules-bmad-analyst/
│   ├── rules-bmad-pm/
│   ├── rules-bmad-architect/
│   ├── rules-bmad-design-architect/
│   ├── rules-bmad-po/
│   ├── rules-bmad-sm/
│   └── rules-bmad-dev/
├── bmad-agent/
│   ├── data/
│   │   ├── bmad-kb.md
│   │   └── technical-preferences.txt
│   ├── templates/
│   │   ├── project-brief-tmpl.md
│   │   ├── prd-tmpl.md
│   │   ├── architecture-tmpl.md
│   │   └── story-tmpl.md
│   ├── checklists/
│   └── tasks/
├── docs/
│   ├── project-brief.md
│   ├── prd.md
│   ├── architecture.md
│   └── stories/
└── src/
```

### Mode-Specific Instructions
Each mode will have dedicated instruction files in `.roo/rules-{mode-slug}/` containing:
- Core principles and behavior guidelines
- Workflow-specific instructions
- Template usage guidelines
- Quality standards and checklists
- Integration patterns with other modes

## Success Metrics

### Workflow Efficiency
- [ ] Reduced context switching overhead compared to BMAD orchestrators
- [ ] Faster document generation and iteration cycles
- [ ] Improved file management and organization
- [ ] Better integration with development workflows

### Quality Improvements
- [ ] Higher consistency in document formats and standards
- [ ] Better cross-document alignment and validation
- [ ] Improved code quality through specialized developer modes
- [ ] Enhanced project structure and organization

### User Experience
- [ ] Intuitive mode selection and transitions
- [ ] Clear workflow guidance and progress indicators
- [ ] Reduced learning curve for BMAD methodology
- [ ] Improved debugging and error handling

## Risk Mitigation

### Technical Risks
- **ROO Limitations**: Thorough testing of ROO capabilities before full implementation
- **File Access Issues**: Robust error handling and fallback mechanisms
- **Tool Integration**: Comprehensive testing of tool combinations and workflows

### Workflow Risks
- **Mode Confusion**: Clear naming and documentation of mode purposes
- **Context Loss**: Careful design of mode handoff protocols
- **Process Adherence**: Built-in guidance and validation systems

### Adoption Risks
- **Learning Curve**: Comprehensive documentation and training materials
- **Workflow Disruption**: Gradual migration path from existing BMAD setups
- **Feature Gaps**: Regular user feedback and iterative improvement

## Questions for Clarification

1. **ROO Capability Verification**: What are the current limitations on file access patterns and tool combinations in ROO CODE?

2. **Project Integration**: How should the BMAD-ROO system integrate with existing ROO workspace structures?

3. **Template Management**: What's the preferred approach for managing and versioning BMAD templates within ROO?

4. **Cross-Mode State**: What mechanisms does ROO provide for maintaining state across mode switches?

5. **User Preferences**: Are there specific BMAD workflows or features you'd like to prioritize or modify for the ROO environment?

6. **Performance Considerations**: Are there any known performance considerations for complex custom mode setups in ROO?

This conversion plan maintains the proven BMAD methodology while leveraging ROO CODE's superior technical capabilities for a more integrated, efficient, and powerful AI-driven development experience.