# Joomla 5 Cursor Rules Collection

A comprehensive set of Cursor Rules for professional Joomla 5 development. These rules provide intelligent code assistance, best practices, and security guidelines for building modern Joomla extensions.

## 📋 Available Rules

### Core Development Rules

- **`joomla-5-standards.mdc`** - General development standards, PSR-12 compliance, and coding conventions
- **`joomla-5-security.mdc`** - Security best practices and vulnerability prevention
- **`joomla-5-component.mdc`** - Component development guidelines and MVC architecture
- **`joomla-5-plugin.mdc`** - Plugin development structure and lifecycle
- **`joomla-5-plugin-types.mdc`** - Comprehensive guide to all plugin types and their use cases
- **`joomla-5-module.mdc`** - Module development including helpers and caching
- **`joomla-5-template.mdc`** - Template development and frontend best practices
- **`joomla-5-api.mdc`** - Web Services API development and RESTful practices
- **`joomla-5-reuse-component.mdc`** - Core component integration guidelines
- **`joomla-5-standalone.mdc`** - Standalone extension development without full Joomla installation
- **`joomla-5-packaging.mdc`** - Extension packaging, build scripts, and ZIP creation for installation
- **`joomla-5-structure-correction.mdc`** - ⚠️ CRITICAL: Correct Joomla 5 folder structure (src/ at root level)

## 🚀 Getting Started

### Installation Options

#### Option 1: Full Joomla Installation
1. **Clone or download** this repository to your local machine
2. **Copy the `.cursor` directory** to your Joomla project root
3. **Open your project** in Cursor IDE
4. The rules will be automatically loaded and applied based on file types and contexts

#### Option 2: Standalone Component Development
1. **Create a new directory** for your component project
2. **Copy the `.cursor` directory** to your component project root
3. **Set up your component structure** (admin/, site/, api/ folders)
4. **Open your project** in Cursor IDE
5. The rules will apply automatically based on file patterns and content

#### Option 3: Extension Development Repository
1. **Clone or download** this repository
2. **Copy the `.cursor` directory** to any Joomla extension project
3. The rules work for components, plugins, modules, and templates independently
4. Perfect for maintaining extensions in separate Git repositories

### Rule Configuration

Each rule includes metadata that controls when and how it's applied:

- **`alwaysApply: true`** - Applied to every request (e.g., security standards)
- **`globs: "*.php,*.xml"`** - Applied only to specific file types
- **`description`** - Used by Cursor to understand when to fetch the rule

## 📖 Rule Descriptions

### General Standards (`joomla-5-standards.mdc`)
**Always Applied** - Covers PSR-12 coding standards, security practices, project structure, and integration guidelines that apply to all Joomla development.

### Security Best Practices (`joomla-5-security.mdc`)
**Always Applied** - Essential security guidelines covering input validation, output escaping, CSRF protection, and common vulnerability prevention.

### Component Development (`joomla-5-component.mdc`)
**File Types:** `*.php`, `*.xml`, `components/**/*`
Comprehensive guidelines for building Joomla components including MVC architecture, database interaction, routing, and ACL implementation.

### Plugin Development (`joomla-5-plugin.mdc`)
**File Types:** `*.php`, `*.xml`, `plugins/**/*`
Guidelines for creating secure and compliant plugins covering structure, manifest conventions, and dependency injection.

### Plugin Types Guide (`joomla-5-plugin-types.mdc`)
**File Types:** `plugins/**/*`
Detailed guide to all Joomla plugin types (system, content, authentication, etc.) with use cases and implementation examples.

### Module Development (`joomla-5-module.mdc`)
**File Types:** `*.php`, `*.xml`, `modules/**/*`
Complete guide for developing modules including helper classes, configuration, caching, and template integration.

### Template Development (`joomla-5-template.mdc`)
**File Types:** `*.php`, `*.css`, `*.js`, `templates/**/*`, `templateDetails.xml`
Frontend development guidelines covering responsive design, overrides, and modern web practices.

### API Development (`joomla-5-api.mdc`)
**File Types:** `*.php`, `api/**/*`, `components/**/api/**/*`
Web Services API development including authentication, serialization, and RESTful design patterns.

### Core Integration (`joomla-5-reuse-component.mdc`)
**File Types:** `*.php`, `*.xml`, `components/**/*`
Guidelines for integrating with core Joomla components like categories, users, media, and tags.

### Standalone Development (`joomla-5-standalone.mdc`)
**File Types:** `*.php`, `*.xml`, `*.css`, `*.js`
Comprehensive guide for developing Joomla extensions independently without requiring a full Joomla installation.

### Extension Packaging (`joomla-5-packaging.mdc`)
**File Types:** `*.php`, `*.xml`, `*.json`, `package.json`, `Makefile`
Guidelines for packaging extensions into installable ZIP files with build scripts and automated workflows.

### Structure Correction (`joomla-5-structure-correction.mdc`)
**Always Applied** - ⚠️ CRITICAL correction showing proper Joomla 5 folder structure with `src/` at component root level, not inside admin/site folders.

## 🛠️ Usage Examples

### Standalone Component Development
Create a new component project anywhere:
```
my-component/
├── .cursor/rules/          # Copy the rules here
├── admin/                  # Interface files
│   ├── forms/
│   ├── tmpl/
│   ├── sql/
│   └── services/
├── site/                   # Interface files
│   └── tmpl/
├── api/                    # Interface files
├── src/                    # ✅ ROOT LEVEL SOURCE CODE
│   ├── Administrator/      # Admin classes
│   ├── Site/               # Site classes
│   └── Api/                # API classes
├── manifest.xml
├── build.sh               # Build script for packaging
└── dist/                  # Generated ZIP packages
    └── com_mycomponent-1.0.0.zip
```

When working on component files, Cursor will automatically apply:
- General standards and security practices
- Component-specific MVC guidelines
- Database interaction best practices
- Routing and ACL implementation
- **Packaging workflows for installable ZIP creation**

### Plugin Development
Works in any plugin project structure:
```
my-plugin/
├── .cursor/rules/          # Copy the rules here
├── src/
├── language/
├── services/
└── plugin.xml
```

You'll get assistance with:
- Plugin structure and naming conventions
- Event handling and lifecycle management
- Configuration and manifest setup
- Type-specific implementation patterns

### Template Development
Perfect for theme development projects:
```
my-template/
├── .cursor/rules/          # Copy the rules here
├── css/
├── js/
├── html/
├── index.php
└── templateDetails.xml
```

Cursor provides:
- Modern frontend development practices
- Responsive design guidelines
- Asset management with Web Asset Manager
- Accessibility and performance optimization

## 📁 Directory Structure

```
.cursor/
└── rules/
    ├── joomla-5-standards.mdc      # General development standards
    ├── joomla-5-security.mdc       # Security best practices
    ├── joomla-5-component.mdc      # Component development
    ├── joomla-5-plugin.mdc         # Plugin development
    ├── joomla-5-plugin-types.mdc   # Plugin types guide
    ├── joomla-5-module.mdc         # Module development
    ├── joomla-5-template.mdc       # Template development
    ├── joomla-5-api.mdc            # API development
    ├── joomla-5-reuse-component.mdc # Core integration
    ├── joomla-5-standalone.mdc     # Standalone development
    ├── joomla-5-packaging.mdc      # Extension packaging
    └── joomla-5-structure-correction.mdc # Critical structure fixes
```

## 🎯 Key Features

- **Comprehensive Coverage** - Rules for all Joomla extension types
- **Security-First** - Built-in security guidelines and vulnerability prevention
- **Modern Practices** - Up-to-date with Joomla 5 features and PHP 8+ standards
- **Context-Aware** - Rules apply automatically based on file types and project structure
- **Professional Quality** - Based on enterprise-level Joomla development experience

## 🔧 Customization

You can customize these rules by:

1. **Modifying existing rules** - Edit `.mdc` files to match your coding standards
2. **Adding project-specific rules** - Create additional rule files for your specific needs
3. **Adjusting rule metadata** - Change `globs` patterns or `alwaysApply` settings

## 💡 Standalone Development Benefits

### Independent Component Development
- **No Joomla installation required** - Develop components in isolation
- **Repository flexibility** - Keep extensions in separate Git repositories
- **Faster development** - Focus on your extension without full Joomla overhead
- **Version control** - Easier to track changes in focused projects

### Distribution and Packaging
- Develop your component with proper structure
- Package and distribute as installable extensions
- Test in multiple Joomla environments
- Maintain clean separation of concerns

### Team Development
- Multiple developers can work on different extensions
- Each extension can have its own repository and development environment
- Rules ensure consistency across all team members
- No conflicts with core Joomla development

## 📚 Best Practices

1. **Keep rules updated** - Regularly update rules to match Joomla evolution
2. **Follow security guidelines** - Always prioritize security in your development
3. **Use modern PHP features** - Leverage PHP 8+ features and Joomla 5 improvements
4. **Test thoroughly** - Use the guidelines for comprehensive testing practices

## 🤝 Contributing

To contribute to this rule collection:

1. Fork the repository
2. Create a feature branch
3. Add or improve rules following the existing format
4. Test with real Joomla projects
5. Submit a pull request

## 📝 License

This project is open source and available under the MIT License.

## 🏷️ Version

**Current Version:** 1.0.0
**Joomla Compatibility:** 5.0+
**PHP Compatibility:** 8.1+

---

*Created for the Joomla development community to promote best practices, security, and code quality in Joomla 5 extension development.*