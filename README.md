# PxPlus Programming Language Documentation

[![License](https://img.shields.io/badge/License-Documentation-blue.svg)](https://pvxplus.com/)
[![PxPlus](https://img.shields.io/badge/PxPlus-2025-orange.svg)](https://manual.pvxplus.com/)
[![Documentation](https://img.shields.io/badge/Files-2400%2B-brightgreen.svg)]()

Comprehensive documentation for the PxPlus (formerly ProvideX) business programming language. This repository contains 2,400+ markdown files covering all aspects of PxPlus development, structured and optimized for AI coding assistants and developer reference.

## About PxPlus

PxPlus is a modern business application development language derived from Business BASIC. It's designed for developing robust business applications with:

- **Native Business Logic**: Built-in support for keyed file systems, indexed databases, and business-specific data structures
- **Cross-Platform**: Write once, deploy on Windows, Linux, macOS, and Unix systems
- **Rapid GUI Development**: NOMADS visual designer for desktop applications, iNOMADS for web-based interfaces
- **Web Framework**: Webster framework for building web applications and services
- **Database Integration**: ODBC connectivity for SQL databases, native file handling for high-performance data access
- **Modern OOP**: Full object-oriented programming with classes, inheritance, properties, and methods

PxPlus excels in retail, manufacturing, distribution, and enterprise business systems where development speed, data integrity, and cross-platform compatibility are essential.

## Repository Contents

This documentation repository provides complete reference materials for PxPlus programming:

### Language Reference (500+ files)
- **233 Directives** - All PxPlus commands: OPEN, READ, WRITE, IF, FOR, CLASS, TRY, etc.
- **130 Functions** - Built-in functions: STR(), NUM(), LEN(), POS(), MSK(), DTE(), etc.
- **44 System Variables** - ERR, LFO, DAY, TIM, and other system variables
- **237 System Parameters** - SET_PARAM configurations for system behavior
- **184 Mnemonics** - Print and display control codes

### Frameworks & Tools (1,200+ files)
- **NOMADS GUI Development** (252 files) - Complete visual development framework
- **Webster Web Framework** (30 files) - Web application development
- **iNOMADS** (34 files) - Browser-based GUI applications
- **Data Dictionary** (47 files) - Data structure management
- **Report Writer** (54 files) - Report generation system
- **Query Subsystem** - Dynamic query builder and runtime queries

### Development Resources (700+ files)
- **PxPlus User Guide** (192 files) - Comprehensive programming guide
- **How-To Guides** (34 files) - Practical tutorials and examples
- **File Handling** - Keyed files, indexed files, ODBC, file tags
- **Utilities** - Development tools and helper programs
- **Language Interfaces** (63 files) - Integrating with C, .NET, COM, etc.
- **Appendices** - Error codes, ASCII tables, migration guides

### Navigation
- **[DOCS_INDEX.md](DOCS_INDEX.md)** - Complete documentation index with quick reference
- All files in **docs/** directory organized by topic

## Documentation Structure

```
docs/
├── directives/              # 233 command references
├── functions/               # 130 function references
├── variables/               # System variable documentation
├── parameters/              # System parameter configuration
├── file_handling/           # File operations and data structures
├── NOMADS Graphical Application/  # GUI framework (252 files)
├── Webster/                 # Web development framework
├── iNOMADS/                 # Browser-based GUI
├── Data Dictionary/         # Data structure management
├── Report Writer/           # Report generation
├── PxPlus User Guide/       # Programming guide (192 files)
├── How To/                  # Tutorials and examples
├── utilities/               # Development utilities
├── appendix/                # Reference materials
└── [many more categories]
```

See **[DOCS_INDEX.md](DOCS_INDEX.md)** for complete structure and quick navigation.

## Quick Reference Examples

### Basic File Operations
```pxplus
! Open a keyed file and read a record
OPEN (1) "customers.dat"
READ (1, KEY="CUST001") name$, balance
PRINT "Customer: ", name$, " Balance: ", balance
CLOSE (1)
```

### Object-Oriented Programming
```pxplus
! Define a class with properties and methods
DEF CLASS "Customer" CREATE REQUIRED DELETE REQUIRED
    PROPERTY name$ SET ERR
    PROPERTY id$ SET ERR
    PROPERTY balance SET ERR
    FUNCTION GetInfo$()GET_INFO_LABEL
END DEF

ON_CREATE:
    balance = 0
    RETURN

GET_INFO_LABEL:
    RETURN name$ + " (" + id$ + ") - $" + STR(balance:"###,##0.00")
```

### Modern Error Handling
```pxplus
! TRY/CATCH error handling
TRY
    OPEN (1) "datafile.dat"
    READ (1, KEY="KEY001") data$
    PROCESS data$
CATCH err_num
    PRINT "Error ", err_num, ": ", MSG(err_num)
FINALLY
    CLOSE (1, ERR=*NEXT)
END_TRY
```

### Web Services with Webster
```pxplus
! Webster endpoint handler
ENTER method$, path$, params$

IF method$ = "GET" THEN {
    ! Build JSON response
    json$ = "{"
    json$ += $22$ + "status" + $22$ + ":" + $22$ + "success" + $22$
    json$ += "}"
    RETURN json$
}
```

## Key PxPlus Features Documented

### Language Syntax
- Variable types: string ($), numeric, arrays, objects
- Control structures: IF/THEN/ELSE, FOR/NEXT, WHILE/WEND, SWITCH/CASE
- Modern and traditional syntax styles
- Line continuation, multi-line blocks, comments

### File Handling
- Keyed files, indexed files, serial files
- ODBC database connectivity
- Special file types: TCP, HTTP, Memory, PDF, HTML
- Record locking and BSY handling
- IOLISTs for structured I/O

### Object-Oriented Features
- Class definitions with DEF CLASS
- Properties with SET ERR and HIDE modifiers
- Methods and method overloading
- Inheritance with LIKE
- Object lifecycle: CREATE, DELETE, FOR PROGRAM

### Critical Coding Rules
15 essential PxPlus coding rules are included in `context7.json`:
- String variables must end with `$` suffix
- FOR-NEXT loops always execute at least once
- No RETURN inside FOR loops (use flag + BREAK)
- Save LFO immediately after OPEN
- Object reference lifecycle management
- And 10 more critical patterns

## Using This Documentation

### For AI Coding Assistants
This repository is optimized for AI tools via **Context7** and similar services:
- All content in markdown format
- Structured with clear hierarchy
- `context7.json` configuration included
- Critical coding rules extracted

AI assistants using this documentation can provide accurate PxPlus code generation, explain language features, and help debug syntax errors.

### For Developers
Browse the documentation directly:
1. Start with **[DOCS_INDEX.md](DOCS_INDEX.md)** for an overview
2. Navigate to **docs/** for specific topics
3. Search for specific directives in **docs/directives/**
4. Find function references in **docs/functions/**

### For Documentation Tools
- All files are standard markdown
- Cross-references use relative links
- Code examples use \`\`\`pxplus code blocks
- Consistent file naming conventions

## Version Information

- **Documentation Version**: PxPlus 2025
- **Files**: 2,428 markdown documents
- **Last Updated**: October 2024
- **Coverage**: Complete language reference through PxPlus 2025

**Note**: PxPlus is actively developed by PVX Plus Technologies. This documentation reflects the language as of early 2025. For the latest features and updates, visit [manual.pvxplus.com](https://manual.pvxplus.com/).

## Source & Attribution

**Original Documentation**: Copyright © **PVX Plus Technologies Ltd.**
**Official Documentation**: [manual.pvxplus.com](https://manual.pvxplus.com/)
**PxPlus Software**: [pvxplus.com](https://pvxplus.com/)

This repository contains documentation extracted and converted to markdown format from official PVX Plus Technologies documentation sources. All rights to PxPlus language, documentation content, and trademarks belong to PVX Plus Technologies Ltd.

**PxPlus®** is a registered trademark of PVX Plus Technologies Ltd.

### Purpose
This markdown conversion was created to make PxPlus documentation accessible to:
- AI-powered development tools
- Modern documentation browsers
- Developers preferring markdown format
- Integration with development workflows

This is a community-maintained resource intended to supplement (not replace) the official documentation.

## Contributing

Improvements welcome! To contribute:

1. **Documentation fixes**: Correct errors, improve clarity, fix formatting
2. **Examples**: Add practical code examples to existing documentation
3. **Navigation**: Improve cross-references and organization
4. **Updates**: Keep documentation current with new PxPlus releases

Please fork the repository and submit pull requests with clear descriptions.

## Repository Information

**GitHub**: [github.com/Astecom/claude-pxplus-template](https://github.com/Astecom/claude-pxplus-template)
**Maintained by**: Astecom
**Format**: Markdown
**Files**: 2,428 documentation files
**Size**: ~28 MB

## License

Documentation content is copyright PVX Plus Technologies Ltd. See PVX Plus Technologies for official licensing terms.

The markdown formatting and repository structure are provided as-is for use with development tools and AI assistants.

---

**Comprehensive PxPlus documentation for modern development workflows**
