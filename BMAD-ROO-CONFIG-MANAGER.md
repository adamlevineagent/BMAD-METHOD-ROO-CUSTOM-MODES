# BMAD-ROO Configuration Manager

## Overview

The BMAD-ROO Configuration Manager provides a centralized system for managing all aspects of the BMAD methodology integration with ROO Code. It handles project initialization, mode configuration, template management, and workflow orchestration setup.

## Core Configuration Structure

### Project Configuration Schema
```yaml
# .bmad-config.yml
bmad_project:
  metadata:
    name: "Project Name"
    description: "Project description"
    type: "web_app" | "mobile_app" | "api" | "data_platform" | "enterprise_system"
    complexity: "simple" | "moderate" | "complex" | "enterprise"
    methodology_version: "3.0"
    created_date: "2024-01-01"
    
  team:
    size: 5
    roles_present: ["analyst", "pm", "architect", "designer", "developer"]
    experience_level: "mixed" # junior | mixed | senior
    
  technology:
    primary_stack: ["React", "Node.js", "PostgreSQL"]
    deployment_target: "cloud" # cloud | on_premise | hybrid
    scalability_requirements: "medium" # low | medium | high | enterprise
    
  timeline:
    duration_weeks: 12
    phases:
      analysis: 2
      design: 3
      development: 6
      testing: 1
      
  workflow:
    type: "standard" # standard | agile | waterfall | custom
    parallel_streams: false
    skip_phases: []
    quality_gates: "standard" # minimal | standard | comprehensive
    automation_level: "hybrid" # manual | hybrid | full_auto

  templates:
    customizations:
      project_brief: "standard"
      prd: "saas_template"
      architecture: "microservices_template"
      story: "standard"
    
  validation:
    critical_checklists: ["security", "scalability", "usability"]
    auto_validation: true
    quality_threshold: 85
    
  integrations:
    jira_project_key: "PROJ"
    confluence_space: "PROJ"
    github_repo: "org/project-name"
    slack_channel: "#project-updates"
```

### ROO Mode Configuration Manager
```typescript
interface BMADModeConfig {
  slug: string;
  name: string;
  roleDefinition: string;
  whenToUse: string;
  bmadRole: BMADRole;
  applicablePhases: string[];
  fileRestrictions: FileRestriction[];
  templates: string[];
  checklists: string[];
  tools: ToolGroup[];
  customInstructions: string;
}

class BMADConfigurationManager {
  private projectConfig: BMADProjectConfig;
  private modeConfigs: Map<string, BMADModeConfig>;
  
  initializeProject(projectType: string, complexity: string): BMADProjectConfig {
    return this.generateProjectConfig(projectType, complexity);
  }
  
  setupROOModes(projectConfig: BMADProjectConfig): ROOModeSetup {
    const modes = this.generateModeConfigurations(projectConfig);
    return this.deployModes(modes);
  }
  
  configureWorkflow(projectConfig: BMADProjectConfig): WorkflowConfig {
    return this.generateWorkflowConfig(projectConfig);
  }
}
```

## Auto-Configuration Templates

### Web Application Project
```yaml
# Auto-generated for web_app + moderate complexity
bmad_project:
  metadata:
    type: "web_app"
    complexity: "moderate"
    
  workflow:
    type: "agile"
    parallel_streams: true
    phases:
      - name: "analysis"
        duration_weeks: 1.5
        parallel_with: []
      - name: "design"
        duration_weeks: 2
        parallel_with: ["technical_architecture"]
      - name: "technical_architecture" 
        duration_weeks: 2
        parallel_with: ["design"]
      - name: "development_prep"
        duration_weeks: 0.5
        depends_on: ["design", "technical_architecture"]
        
  templates:
    customizations:
      prd: "web_app_prd"
      architecture: "web_app_architecture" 
      frontend_spec: "react_frontend_spec"
      api_spec: "rest_api_spec"
      
  roo_modes:
    - slug: "bmad-web-analyst"
      name: "🔍 Web App Analyst"
      file_types: [".md", ".txt", ".json"]
      focus_areas: ["user_experience", "business_requirements", "market_analysis"]
      
    - slug: "bmad-web-architect"
      name: "🏗️ Web App Architect"
      file_types: [".md", ".json", ".yml", ".js", ".ts"]
      focus_areas: ["scalability", "performance", "security", "frontend_architecture"]
```

### Enterprise System Project
```yaml
# Auto-generated for enterprise_system + complex
bmad_project:
  metadata:
    type: "enterprise_system"
    complexity: "complex"
    
  workflow:
    type: "waterfall"
    parallel_streams: true
    quality_gates: "comprehensive"
    
  phases:
    analysis:
      duration_weeks: 4
      deliverables: ["business_case", "stakeholder_analysis", "requirements_catalog"]
      quality_gates: ["enterprise_analysis_gate"]
      
    architecture:
      duration_weeks: 6  
      deliverables: ["system_architecture", "integration_architecture", "security_architecture"]
      quality_gates: ["architecture_review_board"]
      
    design:
      duration_weeks: 4
      deliverables: ["detailed_design", "interface_specs", "data_models"]
      quality_gates: ["design_review"]
      
  templates:
    customizations:
      project_brief: "enterprise_brief"
      prd: "enterprise_prd"
      architecture: "enterprise_architecture"
      integration_spec: "enterprise_integration"
      security_spec: "enterprise_security"
      
  validation:
    critical_checklists: [
      "enterprise_security", 
      "compliance_check", 
      "scalability_review",
      "integration_validation",
      "performance_requirements"
    ]
    quality_threshold: 95
```

## Dynamic Configuration Generation

### Project Type Detection
```typescript
class ProjectTypeDetector {
  analyzeProject(projectPath: string): ProjectAnalysis {
    const files = this.scanProjectFiles(projectPath);
    const packageFiles = this.findPackageFiles(files);
    const frameworks = this.detectFrameworks(packageFiles);
    const architecture = this.inferArchitecture(files, frameworks);
    
    return {
      projectType: this.determineProjectType(frameworks, architecture),
      complexity: this.assessComplexity(files, frameworks),
      recommendedWorkflow: this.suggestWorkflow(projectType, complexity),
      techStack: frameworks,
      suggestedTemplates: this.selectTemplates(projectType, frameworks)
    };
  }
  
  private determineProjectType(frameworks: string[], architecture: Architecture): ProjectType {
    if (frameworks.includes('React') || frameworks.includes('Vue') || frameworks.includes('Angular')) {
      return architecture.hasBackend ? 'web_app' : 'frontend_app';
    }
    if (frameworks.includes('React Native') || frameworks.includes('Flutter')) {
      return 'mobile_app';
    }
    if (frameworks.includes('Express') || frameworks.includes('FastAPI') && !architecture.hasFrontend) {
      return 'api';
    }
    return 'general_software';
  }
}
```

### Intelligent Mode Selection
```typescript
class IntelligentModeSelector {
  selectOptimalModes(projectConfig: BMADProjectConfig): BMADModeConfig[] {
    const baseRoles = this.getRequiredRoles(projectConfig.type, projectConfig.complexity);
    const specializedRoles = this.getSpecializedRoles(projectConfig.technology);
    
    return [...baseRoles, ...specializedRoles].map(role => 
      this.generateModeConfig(role, projectConfig)
    );
  }
  
  private getRequiredRoles(type: ProjectType, complexity: Complexity): BMADRole[] {
    const baseRoles = ['analyst', 'pm'];
    
    if (complexity !== 'simple') {
      baseRoles.push('architect');
    }
    
    if (type === 'web_app' || type === 'mobile_app') {
      baseRoles.push('designer', 'frontend_architect');
    }
    
    if (complexity === 'enterprise') {
      baseRoles.push('security_architect', 'integration_architect');
    }
    
    return baseRoles;
  }
}
```

## Configuration Validation Engine

### Validation Rules
```typescript
interface ValidationRule {
  name: string;
  check: (config: BMADProjectConfig) => ValidationResult;
  severity: 'error' | 'warning' | 'info';
  suggestion?: string;
}

class ConfigurationValidator {
  private rules: ValidationRule[] = [
    {
      name: 'timeline_consistency',
      check: (config) => this.validateTimelineConsistency(config),
      severity: 'error',
      suggestion: 'Ensure phase durations sum to total project duration'
    },
    {
      name: 'role_coverage',
      check: (config) => this.validateRoleCoverage(config),
      severity: 'warning', 
      suggestion: 'Consider adding missing roles for project complexity level'
    },
    {
      name: 'template_compatibility',
      check: (config) => this.validateTemplateCompatibility(config),
      severity: 'error',
      suggestion: 'Selected templates must be compatible with project type'
    }
  ];
  
  validate(config: BMADProjectConfig): ValidationReport {
    const results = this.rules.map(rule => ({
      rule: rule.name,
      result: rule.check(config),
      severity: rule.severity,
      suggestion: rule.suggestion
    }));
    
    return {
      valid: results.every(r => r.severity !== 'error' || r.result.valid),
      errors: results.filter(r => r.severity === 'error' && !r.result.valid),
      warnings: results.filter(r => r.severity === 'warning' && !r.result.valid),
      suggestions: results.filter(r => !r.result.valid).map(r => r.suggestion)
    };
  }
}
```

## Setup Automation Scripts

### Project Initialization
```bash
#!/bin/bash
# bmad-init.sh - Automated BMAD-ROO project setup

echo "🚀 Initializing BMAD-ROO Project..."

# Detect project characteristics
PROJECT_TYPE=$(detect_project_type)
COMPLEXITY=$(assess_complexity)
TECH_STACK=$(identify_tech_stack)

echo "📊 Detected: $PROJECT_TYPE project with $COMPLEXITY complexity"
echo "🛠️  Tech Stack: $TECH_STACK"

# Generate configuration
generate_bmad_config "$PROJECT_TYPE" "$COMPLEXITY" "$TECH_STACK"

# Setup ROO modes
setup_roo_modes

# Initialize templates
initialize_templates

# Create directory structure
create_bmad_directories

# Setup automation
configure_automation

echo "✅ BMAD-ROO project initialized successfully!"
echo "📝 Configuration saved to .bmad-config.yml"
echo "🎯 Run 'bmad status' to view current project state"
```

### Mode Deployment Script
```bash
#!/bin/bash
# deploy-modes.sh - Deploy BMAD ROO modes

echo "🎭 Deploying BMAD ROO Modes..."

# Read project configuration
source .bmad-config.yml

# Generate mode configurations
for role in "${BMAD_ROLES[@]}"; do
    echo "Creating mode: bmad-$role"
    generate_mode_config "$role" "$PROJECT_TYPE" "$COMPLEXITY"
done

# Deploy to ROO
deploy_to_roo_global
deploy_to_roo_project

# Validate deployment
validate_mode_deployment

echo "✅ All BMAD modes deployed successfully!"
```

## Interactive Configuration Wizard

### CLI Wizard Implementation
```typescript
class BMADConfigWizard {
  async runInteractiveSetup(): Promise<BMADProjectConfig> {
    console.log('🧙‍♂️ BMAD-ROO Configuration Wizard');
    
    const projectInfo = await this.gatherProjectInfo();
    const teamInfo = await this.gatherTeamInfo();
    const techInfo = await this.gatherTechnologyInfo();
    const workflowInfo = await this.gatherWorkflowPreferences();
    
    const suggestedConfig = this.generateSuggestedConfig({
      ...projectInfo,
      ...teamInfo, 
      ...techInfo,
      ...workflowInfo
    });
    
    const finalConfig = await this.reviewAndCustomize(suggestedConfig);
    
    return this.validateAndSave(finalConfig);
  }
  
  private async gatherProjectInfo(): Promise<ProjectInfo> {
    return {
      name: await prompt('Project name:'),
      description: await prompt('Project description:'),
      type: await select('Project type:', [
        'web_app', 'mobile_app', 'api', 'data_platform', 'enterprise_system'
      ]),
      complexity: await select('Project complexity:', [
        'simple', 'moderate', 'complex', 'enterprise'
      ])
    };
  }
  
  private async reviewAndCustomize(config: BMADProjectConfig): Promise<BMADProjectConfig> {
    console.log('\n📋 Suggested Configuration:');
    console.log(yaml.stringify(config, { indent: 2 }));
    
    const approved = await confirm('Accept this configuration?');
    
    if (!approved) {
      return await this.customizeConfiguration(config);
    }
    
    return config;
  }
}
```

## Configuration Migration Tools

### Version Migration
```typescript
class ConfigurationMigrator {
  migrateConfig(oldVersion: string, newVersion: string, config: any): BMADProjectConfig {
    const migrations = this.getMigrationPath(oldVersion, newVersion);
    
    return migrations.reduce((currentConfig, migration) => {
      console.log(`Applying migration: ${migration.name}`);
      return migration.transform(currentConfig);
    }, config);
  }
  
  private getMigrationPath(from: string, to: string): Migration[] {
    const migrations = [
      {
        from: '2.0',
        to: '2.1', 
        name: 'Add workflow automation',
        transform: (config) => ({
          ...config,
          workflow: { ...config.workflow, automation_level: 'hybrid' }
        })
      },
      {
        from: '2.1',
        to: '3.0',
        name: 'ROO integration',
        transform: (config) => ({
          ...config,
          roo_modes: this.generateROOModes(config),
          integrations: this.setupIntegrations(config)
        })
      }
    ];
    
    return this.findMigrationPath(from, to, migrations);
  }
}
```

## Usage Examples

### Quick Start
```bash
# Initialize new BMAD-ROO project
bmad init

# Initialize with specific parameters
bmad init --type=web_app --complexity=moderate --framework=react

# Import existing project
bmad import --scan-project --auto-detect

# Validate current configuration
bmad validate

# Update configuration
bmad config update --workflow=agile --add-role=security_architect
```

### Programmatic Usage
```typescript
import { BMADConfigManager } from '@bmad/roo-config';

// Initialize configuration manager
const configManager = new BMADConfigManager();

// Auto-detect and configure
const autoConfig = await configManager.autoDetectAndConfigure('./project');

// Custom configuration
const customConfig = configManager.createConfig({
  projectType: 'web_app',
  complexity: 'moderate',
  techStack: ['React', 'Node.js', 'PostgreSQL'],
  team: { size: 5, experienceLevel: 'mixed' }
});

// Deploy configuration
await configManager.deploy(customConfig);

// Validate setup
const validation = await configManager.validate();
console.log(`Setup ${validation.valid ? '✅ Valid' : '❌ Invalid'}`);
```

This configuration manager provides the foundation for easy setup and management of the entire BMAD-ROO system, making it accessible to teams of all experience levels while maintaining the flexibility for advanced customization.