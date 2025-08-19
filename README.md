# Joomla 5 Cursor Rules Collection

A **streamlined and optimized** set of Cursor Rules for professional Joomla 5 development. These rules provide intelligent code assistance, best practices, and security guidelines with **zero redundancy** and **maximum efficiency**.

## 🎯 Optimized for Productivity

**6 Essential Rules** covering 90% of Joomla development scenarios:
- ✅ **50% reduction** from original 12 rules
- ✅ **Zero overlap** between rules  
- ✅ **Comprehensive coverage** without redundancy
- ✅ **Specialized rules preserved** in backup for future use

## 📋 Core Rules (Always Active)

### Essential Standards & Security
- **`joomla-5-standards.mdc`** ⚠️ *Always Applied* - PSR-12, coding conventions, and **correct Joomla 5 structure**
- **`joomla-5-security.mdc`** ⚠️ *Always Applied* - Complete security guidelines and vulnerability prevention

### Extension Development
- **`joomla-5-component.mdc`** - Component development with MVC architecture (80% of projects)
- **`joomla-5-standalone.mdc`** - Standalone development + packaging workflows
- **`joomla-5-plugin.mdc`** - Plugin development with common plugin types
- **`joomla-5-api.mdc`** - Web Services API development and RESTful practices

## 💾 Backup Rules (Available When Needed)

Specialized rules preserved in `backup/cursor-rules/` for future use:
- `joomla-5-template.mdc` - Template/theme development
- `joomla-5-module.mdc` - Module development  
- `joomla-5-packaging.mdc` - Advanced build scripts (merged into standalone)
- `joomla-5-structure-correction.mdc` - Structure fixes (merged into standards)
- `joomla-5-plugin-types.mdc` - Detailed plugin types (merged into plugin)
- `joomla-5-reuse-component.mdc` - Core component integration

**To restore a backup rule:**
```bash
cp backup/cursor-rules/joomla-5-template.mdc .cursor/rules/
```

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
**Always Applied** - PSR-12 standards, security basics, **correct Joomla 5 folder structure**, and integration guidelines. **Includes critical structure correction** showing `src/` at component root level.

### Security Best Practices (`joomla-5-security.mdc`)
**Always Applied** - Comprehensive security covering input validation, output escaping, CSRF protection, database security, and vulnerability prevention.

### Component Development (`joomla-5-component.mdc`)
**File Types:** `*.php`, `*.xml`, `components/**/*`
MVC architecture, database interaction, routing, ACL implementation. **Security sections removed** (handled by security.mdc).

### Standalone Development (`joomla-5-standalone.mdc`)
**File Types:** `*.php`, `*.xml`, `*.css`, `*.js`
Independent extension development with **integrated packaging workflows**. Build scripts and ZIP creation for installation.

### Plugin Development (`joomla-5-plugin.mdc`)
**File Types:** `*.php`, `*.xml`, `plugins/**/*`
Plugin structure, lifecycle management, **includes common plugin types** (system, content, authentication).

### API Development (`joomla-5-api.mdc`)
**File Types:** `*.php`, `api/**/*`, `components/**/api/**/*`
Web Services development with authentication, serialization, and RESTful patterns.

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
- General standards and security practices (always active)
- Component-specific MVC guidelines  
- Database interaction best practices
- Routing and ACL implementation

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
- Common plugin types (system, content, authentication)

### Standalone Development with Packaging
Build and package your extensions:
```
my-component/
├── .cursor/rules/          # Copy the rules here
├── admin/                  # Interface files
├── site/                   # Interface files  
├── src/                    # ✅ ROOT LEVEL SOURCE CODE
├── media/                  # Assets
├── mycomponent.xml         # Manifest
├── build.sh               # Build script
└── dist/                   # Generated packages
    └── com_mycomponent-1.0.0.zip
```

Cursor provides:
- Standalone development workflow
- Integrated build scripts for ZIP packaging
- Proper Joomla 5 folder structure enforcement
- Complete development-to-distribution pipeline

## 📁 Directory Structure

```
.cursor/
└── rules/
    ├── joomla-5-standards.mdc      # ⚠️ Always applied - Standards + structure
    ├── joomla-5-security.mdc       # ⚠️ Always applied - Security practices  
    ├── joomla-5-component.mdc      # Component development (80% of projects)
    ├── joomla-5-standalone.mdc     # Standalone dev + packaging
    ├── joomla-5-plugin.mdc         # Plugin development + types
    └── joomla-5-api.mdc            # API/REST development

backup/cursor-rules/              # 🔒 Not committed to git
├── joomla-5-template.mdc         # Template development
├── joomla-5-module.mdc           # Module development
├── joomla-5-packaging.mdc        # Advanced build scripts  
├── joomla-5-structure-correction.mdc # Structure fixes
├── joomla-5-plugin-types.mdc     # Detailed plugin types
└── joomla-5-reuse-component.mdc  # Core integration
```

## 🎯 Key Features

- **Optimized Efficiency** - 6 focused rules covering 90% of development scenarios
- **Zero Redundancy** - Each rule has a unique purpose, no overlapping content
- **Security-First** - Comprehensive security guidelines in dedicated rule
- **Modern Practices** - Up-to-date with Joomla 5 and PHP 8+ standards
- **Backup System** - Specialized rules preserved for future use
- **Context-Aware** - Rules apply automatically based on file types
- **Professional Quality** - Enterprise-level development standards

## 🔧 Customization

You can customize these rules by:

1. **Modifying existing rules** - Edit `.mdc` files to match your coding standards
2. **Adding project-specific rules** - Create additional rule files for your specific needs
3. **Adjusting rule metadata** - Change `globs` patterns or `alwaysApply` settings

## 💡 Standalone Development Benefits

### Streamlined Workflow
- **Focused rules** - Only 6 essential rules, no confusion
- **No redundancy** - Each rule serves a unique purpose
- **Integrated packaging** - Build scripts included in standalone rule
- **Proper structure** - Correct Joomla 5 folder structure enforced

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

1. **Use core 6 rules** - Cover 90% of Joomla development needs
2. **Restore backup rules when needed** - Add specialized rules for specific projects
3. **Follow security guidelines** - Comprehensive security rule always applied
4. **Proper structure** - Standards rule enforces correct Joomla 5 structure

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

**Current Version:** 2.0.0 - **Optimized Release**
- ✅ 50% reduction in rule count (12 → 6)
- ✅ Zero overlapping content
- ✅ Backup system for specialized needs
- ✅ Enhanced security and structure enforcement

**Joomla Compatibility:** 5.0+
**PHP Compatibility:** 8.1+

---

*Optimized for the Joomla development community - **maximum efficiency, zero redundancy, professional results.***