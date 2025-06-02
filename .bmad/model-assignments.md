# BMAD-ROO Model Assignments Configuration

This file defines the optimal model assignments for each BMAD mode based on context requirements and intelligence needs.

## Model Assignment Strategy

### Gemini 2.5 Pro (High Context + Maximum Intelligence)
- **bmad-orchestrator**: Needs maximum context (1M+ tokens) and highest intelligence for complex workflow coordination
- **bmad-po**: Requires high context for cross-document validation and comprehensive project state management

### Claude 4 Opus (Maximum Intelligence + 200K Context) 
- **bmad-architect**: Requires highest intelligence for complex system design decisions and architectural reasoning

### Claude 4 Sonnet (High Intelligence + 200K Context)
- **bmad-analyst**: Needs creative intelligence for brainstorming and research analysis
- **bmad-pm**: Requires product intelligence for strategic thinking and requirements analysis  
- **bmad-design-architect**: Needs design intelligence and creative problem-solving for UI/UX
- **bmad-sm**: Requires process intelligence for story creation and sprint planning
- **bmad-dev**: Needs coding intelligence for full-stack development
- **bmad-dev-frontend**: Requires specialized frontend coding intelligence
- **bmad-dev-backend**: Needs specialized backend coding intelligence

### Gemini 2.5 Flash (High Context + Good Performance)
- Not currently assigned but available for modes requiring high context without maximum intelligence

## ROO CODE Integration

ROO CODE's sticky model feature will automatically remember the last model used with each mode. The recommended assignments above optimize for:

1. **Context Capacity**: Ensuring modes with high document cross-referencing needs get high-context models
2. **Intelligence Level**: Matching cognitive complexity requirements with appropriate model capabilities  
3. **Cost Efficiency**: Using the most cost-effective model that meets the mode's requirements
4. **Performance**: Balancing response quality with speed for different workflow phases

## Model Selection Guidelines

When using BMAD modes in ROO CODE:

1. **First Usage**: Manually select the recommended model for each mode
2. **Subsequent Usage**: ROO CODE will automatically use the last selected model
3. **Model Switching**: Change models manually if specific tasks require different capabilities
4. **Context Limits**: Monitor token usage and switch to higher-context models when needed

## Implementation Notes

- Model assignments are suggestions based on typical usage patterns
- Users can override with any available model based on specific project needs
- ROO CODE's sticky model feature ensures efficient workflow without constant reconfiguration
- Consider project complexity when selecting models for first-time usage