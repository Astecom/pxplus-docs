# PxPlus Documentation for AI Assistants

[![License](https://img.shields.io/badge/License-Documentation-blue.svg)](https://github.com/Astecom/claude-pxplus-template)
[![PxPlus](https://img.shields.io/badge/PxPlus-Business_BASIC-orange.svg)](https://manual.pvxplus.com/)
[![Context7](https://img.shields.io/badge/Optimized_for-Context7-brightgreen.svg)](https://context7.com)

A comprehensive, AI-optimized documentation repository for PxPlus programming language, designed for use with Context7, Claude Code, and other AI-powered development tools.

## What is PxPlus?

PxPlus (formerly ProvideX) is a modern business application development language derived from Business BASIC. It combines the simplicity of BASIC with powerful features for:

- **Business Applications**: Native support for keyed file systems, indexed databases, and business logic
- **Cross-Platform Development**: Write once, run on Windows, Linux, macOS, and Unix
- **GUI Development**: NOMADS visual designer for desktop applications
- **Web Development**: Webster framework for web applications and iNOMADS for browser-based GUIs
- **Database Connectivity**: ODBC support for integration with SQL databases
- **Object-Oriented Programming**: Modern OOP features with classes, inheritance, and properties

PxPlus is particularly strong in retail, manufacturing, distribution, and business management systems where rapid development and reliable data handling are critical.

## What This Repository Contains

This repository contains the complete PxPlus documentation converted to markdown format and organized for optimal AI assistant consumption:

- **1,700+ documentation files** covering all aspects of PxPlus development
- **233 directive references** (commands like OPEN, READ, WRITE, IF, FOR)
- **130 function references** (built-in functions like STR(), NUM(), LEN(), POS())
- **44 system variables** (ERR, LFO, DAY, TIM, etc.)
- **237 system parameters** (SET_PARAM configurations)
- **324 object property references**
- **Complete guides** for NOMADS GUI development, Webster web framework, database integration, and more
- **Structured index** (DOCS_INDEX.md) for quick navigation
- **Best practices and rules** (INSTRUCTIONS_AND_RULES.md) for PxPlus development

All documentation is extracted from official PVX Plus Technologies sources and formatted for efficient parsing by AI language models.

## How to Use with Context7

[Context7](https://context7.com) is an AI-powered coding platform that provides intelligent code completion and assistance. This repository is specifically optimized for Context7 submission.

### Quick Start with Context7

1. **Submit this repository to Context7**:
   - Visit [context7.com](https://context7.com)
   - Create a new context or add to an existing one
   - Submit the GitHub repository URL: `https://github.com/Astecom/claude-pxplus-template`

2. **Reference the documentation**:
   - Context7 will index all documentation files
   - Use natural language queries to find specific directives, functions, or concepts
   - The AI will understand PxPlus syntax and conventions

3. **Start coding**:
   - Context7 will provide intelligent completions based on the documentation
   - Get instant help with PxPlus syntax, functions, and best practices
   - Receive context-aware suggestions for your specific use case

### What Context7 Learns from This Repository

- Complete PxPlus language syntax and semantics
- All built-in functions and their parameters
- File handling patterns and IOLIST structures
- Object-oriented programming conventions
- Error handling best practices
- NOMADS GUI development patterns
- Webster web development framework
- Common pitfalls and how to avoid them

## How to Use with Claude Code

This repository is designed to work seamlessly with [Claude Code](https://claude.com/claude-code), Anthropic's official CLI for development assistance.

### Setup for Claude Code

1. **Clone or download this repository**:
   ```bash
   git clone https://github.com/Astecom/claude-pxplus-template.git
   cd claude-pxplus-template
   ```

2. **Install the documentation**:
   ```bash
   # The .pxplus-claude directory should be copied to your home directory
   cp -r .pxplus-claude ~/
   ```

3. **Configure PxPlus executable path** (optional, for syntax checking):
   ```bash
   # Edit the config file
   nano ~/.pxplus-claude/pxplus-config.json

   # Set your PxPlus installation path:
   {
     "pxplus_executable_path": "/path/to/your/pxplus"
   }
   ```

4. **Start using Claude Code**:
   - Claude Code will automatically reference documentation from `~/.pxplus-claude/pxplus-docs/`
   - Use natural language to ask about PxPlus features
   - Claude will provide code examples, explanations, and debugging assistance

### Example Claude Code Interactions

```
You: "How do I open a keyed file in PxPlus?"
Claude: [Reads from ~/.pxplus-claude/pxplus-docs/directives/open.md and provides detailed explanation]

You: "Create a class that handles customer data with properties for name, ID, and balance"
Claude: [References OOP documentation and creates proper DEF CLASS structure]

You: "Why is my EXTRACT statement timing out?"
Claude: [Consults error handling docs and suggests BSY= error handling options]
```

## How to Use with Other AI Editors

This documentation works with any AI-powered editor that can access local files or reference external documentation:

### VS Code + GitHub Copilot
- Place `.pxplus-claude` in your home directory
- Reference documentation files in your workspace
- Use comments to guide Copilot: `// See ~/.pxplus-claude/pxplus-docs/directives/open.md`

### Cursor
- Import this repository as a documentation source
- Cursor will index all markdown files
- Use `@docs` to query specific documentation

### Cody by Sourcegraph
- Add `.pxplus-claude/pxplus-docs/` to your workspace
- Cody will use documentation for context-aware completions
- Ask questions about PxPlus directly in the sidebar

### Any AI Assistant with File Access
- Point the assistant to `~/.pxplus-claude/pxplus-docs/`
- Reference specific files: `Read the documentation at ~/.pxplus-claude/pxplus-docs/directives/read.md`
- Use DOCS_INDEX.md to navigate the documentation structure

## Documentation Structure Overview

The documentation is organized into the following categories:

### Core Language Reference
```
directives/         - 233 PxPlus commands (OPEN, READ, WRITE, IF, FOR, etc.)
functions/          - 130 built-in functions (STR(), NUM(), LEN(), MSK(), etc.)
variables/          - 44 system variables (ERR, LFO, DAY, TIM, etc.)
parameters/         - 237 system parameters (SET_PARAM configurations)
mnemonics/          - 184 print/display control mnemonics
```

### File Handling & Data
```
file_handling/      - File types, keyed files, indexed files, native files
command_tags/       - Special file tags (TCP, HTTP, Serial, etc.)
Data Dictionary/    - Data dictionary maintenance and usage
odbc/               - ODBC database connectivity
```

### GUI & Web Development
```
NOMADS Graphical Application/  - Complete NOMADS GUI framework (252 files)
Extended NOMADS Objects/       - Advanced NOMADS features
iNOMADS/                       - Web-based NOMADS applications
Webster/                       - Web development framework
Web Server Reference/          - Web server configuration and usage
control_object_properties/     - GUI control properties reference
```

### Development Tools
```
utilities/          - Various utility programs
Report Writer/      - Report generation tools
PxPlus User Guide/  - Comprehensive programming guide (192 files)
PxIO Library/       - I/O library reference
```

### Learning Resources
```
How To/             - Tutorial-style guides for common tasks
appendix/           - Error codes, ASCII tables, reference materials
conversion/         - Migration guides from other BASIC dialects
Language Interfaces/ - Interfacing with other programming languages
```

**See [DOCS_INDEX.md](.pxplus-claude/docs-index.md) for complete documentation structure and navigation guide.**

## Quick Start Examples

### Hello World
```pxplus
! Simple hello world program
PRINT "Hello, World!"
```

### Reading from a Keyed File
```pxplus
! Open a customer file and read a record
OPEN (1) "customers.dat"
customer_id$ = "CUST001"
READ (1, KEY=customer_id$) customer_name$, balance
PRINT "Customer: ", customer_name$, " Balance: ", balance
CLOSE (1)
```

### Object-Oriented Class
```pxplus
! Define a customer class
DEF CLASS "Customer" CREATE REQUIRED DELETE REQUIRED
    PROPERTY name$ SET ERR
    PROPERTY id$ SET ERR
    PROPERTY balance SET ERR
    FUNCTION GetInfo$()GET_INFO_LABEL
END DEF

ON_CREATE:
    ! Initialize object
    RETURN

ON_DELETE:
    ! Cleanup
    RETURN

GET_INFO_LABEL:
    RETURN name$ + " (" + id$ + ") - Balance: " + STR(balance)
```

### Modern Error Handling
```pxplus
! Modern TRY/CATCH error handling
TRY
    OPEN (1) "datafile.dat"
    READ (1, KEY="KEY001") data$
    PRINT data$
CATCH err_num
    PRINT "Error: ", MSG(err_num)
FINALLY
    CLOSE (1, ERR=*NEXT)
END_TRY
```

### Web Service with Webster
```pxplus
! Simple Webster web service endpoint
ENTER method$, path$, query$, body$

IF method$ = "GET" THEN {
    ! Return JSON response
    response$ = "{" + $22$ + "status" + $22$ + ": " + $22$ + "success" + $22$ + "}"
    RETURN response$
}
```

## Version and Updates

- **Documentation Version**: PxPlus 2025 (accurate as of January 2025)
- **Last Updated**: October 2025
- **Update Frequency**: This repository is updated periodically to reflect new PxPlus versions

**Note**: PxPlus is actively developed by PVX Plus Technologies. Always refer to the [official documentation](https://manual.pvxplus.com/) for the most current information on new features and changes.

To check for updates to this documentation repository, watch the GitHub repository for new releases.

## Original Source & Attribution

- **Repository**: [github.com/Astecom/claude-pxplus-template](https://github.com/Astecom/claude-pxplus-template)
- **Maintained by**: Astecom
- **Documentation Source**: All PxPlus documentation is copyright **PVX Plus Technologies Ltd.**
- **Official Manual**: [manual.pvxplus.com](https://manual.pvxplus.com/)

### Attribution

This repository contains documentation extracted and reformatted from official PVX Plus Technologies documentation. All rights to the PxPlus language, documentation content, and trademarks belong to **PVX Plus Technologies Ltd.**

The markdown conversion and AI optimization were performed to make PxPlus development more accessible through modern AI-powered development tools. This is an unofficial, community-maintained resource intended to supplement (not replace) the official documentation.

**PxPlus®** is a registered trademark of PVX Plus Technologies Ltd.

## Contributing

Contributions to improve documentation clarity, fix formatting issues, or add helpful examples are welcome. Please:

1. Fork the repository
2. Make your changes
3. Submit a pull request with a clear description

For issues or questions, please open an issue on GitHub.

## License

The documentation content is copyright PVX Plus Technologies Ltd. The markdown formatting and repository structure are provided as-is for use with AI development tools.

See the official PVX Plus Technologies licensing for PxPlus software and documentation usage terms.

---

**Ready to start coding in PxPlus with AI assistance?**

- Submit to [Context7](https://context7.com) for intelligent code completion
- Use with [Claude Code](https://claude.com/claude-code) for conversational development
- Reference from any AI editor for instant PxPlus expertise

Happy coding!
