# BMAD-ROO System Initialization Guide

## 🎉 System Status: COMPLETE & READY

The BMAD to ROO CODE conversion is complete! You now have a fully functional AI-driven development workflow with 10 specialized agent modes.

## 🚀 Quick Start

### 1. Verify Installation
Your system is ready with:
- ✅ 10 specialized BMAD modes configured in `.roomodes`
- ✅ Canonical state management system in `.bmad/` folder
- ✅ Mode-specific instructions for all agents
- ✅ Project structure following BMAD conventions
- ✅ Model assignment guidelines for optimal performance

### 2. First Usage
1. **Switch to Orchestrator Mode**: Use ROO's mode selector and choose "🎯 BMAD Orchestrator"
2. **Select Recommended Model**: Use Gemini 2.5 Pro for maximum context and intelligence
3. **Begin Workflow**: Ask the orchestrator to guide you through your first BMAD project

### 3. Model Setup (One-Time)
For optimal performance, set up these model assignments on first use:

- **🎯 BMAD Orchestrator** → Gemini 2.5 Pro
- **🔍 BMAD Analyst** → Claude 4 Sonnet  
- **📋 BMAD Product Manager** → Claude 4 Sonnet
- **🏗️ BMAD Architect** → Claude 4 Opus
- **🎨 BMAD Design Architect** → Claude 4 Sonnet
- **📊 BMAD Product Owner** → Gemini 2.5 Pro
- **🔄 BMAD Scrum Master** → Claude 4 Sonnet
- **💻 BMAD Developer** → Claude 4 Sonnet
- **🌐 BMAD Frontend Developer** → Claude 4 Sonnet
- **⚙️ BMAD Backend Developer** → Claude 4 Sonnet

ROO's sticky model feature will remember these selections for future use.

## 🔄 Recommended Workflow

### Phase 1: Ideation & Planning
1. **Start with Orchestrator** to understand project goals
2. **Switch to Analyst** for brainstorming and project brief creation
3. **Switch to PM** for PRD and epic development
4. **Use PO** for validation and alignment checking

### Phase 2: Architecture & Design  
1. **Switch to Architect** for technical architecture
2. **Switch to Design Architect** for UI/UX specifications
3. **Use PO** for architectural validation and document organization

### Phase 3: Implementation
1. **Switch to SM** for story creation and sprint planning
2. **Use specialized Developer modes** for implementation
3. **Use PO** for ongoing validation and quality assurance

## 🎯 Key Features

### Canonical State Management
- **Project State**: `.bmad/project-state.md` - Always current project phase and status
- **Workflow Context**: `.bmad/workflow-context.md` - Cross-mode communication and handoffs
- **Document Registry**: `.bmad/document-registry.md` - Master tracking of all project documents

### Intelligent Context Transfer
- Each mode automatically reads relevant state files before acting
- Mode handoffs include complete context packages
- Document dependencies are tracked and maintained
- Quality gates ensure proper phase transitions

### Self-Organizing Documentation
- Documents are automatically tracked and linked
- Obsolete documents are properly archived
- Cross-document consistency is maintained
- Template usage ensures standardization

## 🛠️ Advanced Features

### Mode Handoff Protocol
Each mode follows structured handoff protocols ensuring no context is lost when switching between agents.

### Quality Assurance System
Built-in validation checklists ensure document quality and cross-alignment before phase transitions.

### Template Integration
Direct access to proven BMAD templates with smart file creation and validation.

### Archive Management
Automatic archiving of superseded documents with clear provenance tracking.

## 🎓 Learning Path

### Beginner: Start Simple
1. Use Orchestrator to understand the system
2. Try a simple project with Analyst → PM → Developer flow
3. Focus on understanding the canonical state files

### Intermediate: Full Workflow
1. Use complete BMAD workflow for a real project
2. Experiment with different mode combinations
3. Customize mode instructions for your needs

### Advanced: System Mastery
1. Create custom mode variants for specific tech stacks
2. Optimize workflow patterns for your team
3. Extend the system with additional specialized modes

## 🚨 Important Notes

### Always Check State Files
Before major actions, agents read:
- `.bmad/project-state.md` for current status
- `.bmad/workflow-context.md` for handoff context
- `.bmad/document-registry.md` for document relationships

### Mode Specialization
Each mode has specific file access permissions and tool restrictions optimized for their role in the workflow.

### Context Continuity
The system is designed to maintain context across mode switches, ensuring no information is lost in transitions.

## 🎯 Next Steps

You're ready to begin! Switch to the BMAD Orchestrator mode and start your first AI-driven development project. The system will guide you through the complete workflow from ideation to implementation.

**Recommended First Command**: "Help me start my first BMAD project. I want to build [describe your project idea]."