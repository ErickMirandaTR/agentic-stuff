---
name: generate-readme
description: Create a README file following the awesome-copilot documentation format. Generates comprehensive README files with instruction tables, discovery sections, and best practices guidance for custom instructions or skill documentation.
compatibility: Works with any repository documenting custom instructions, skills, or tools. Follows GitHub Copilot awesome-copilot template standards.
metadata:
  author: Agentic Stuff
  version: "1.0"
---

## Purpose
This skill produces README files following the awesome-copilot directory structure and format, enabling consistent documentation across projects that extend GitHub Copilot functionality.

## Workflow Overview
Input → Gather Context → Format Sections → Create/Update README → Validate Output

---

## Step 1: Gather Project Context
1. **Determine README Purpose**: Identify if documenting:
   - Custom `.instructions.md` files (like `instructions/README.md`)
   - `SKILL.md` files (like `skills/README.md`)
   - Tool recommendations or framework guides
   - Mixed content (instructions + skills + tools)

2. **Collect Required Information**:
   - Project name and description
   - 3-5 featured items with titles, links, and descriptions
   - Categories/organization structure (if applicable)
   - External reference repository (if linking to awesome-copilot or similar)
   - Installation/usage instructions specific to the project
   - Related documentation or official resources

3. **Identify Applicable Sections**:
   - Header with emoji and brief description (required)
   - "How to Use" installation/application section (required)
   - Item table with name (as link), description (required)
   - "Discover More" section for extended resources (required for >5 items)
   - "Official Documentation" reference section (required)
   - Additional sections (optional): How Items Work, Contributing, etc.

---

## Step 2: Format Header Section
1. **Add Emoji + Title**
   - Use relevant emoji (📋 for instructions, 🛠️ for skills, 📚 for documentation)
   - Use format: `# 📋 Custom Instructions` or `# 🛠️ Agent Skills`

2. **Brief Description** (1-2 sentences)
   - Explain what section documents
   - Include file naming convention if applicable (e.g., `*.instructions.md`, `*.md`)

---

## Step 3: Create "How to Use" Section
1. **Installation subsection**:
   - Explain how to add items to workspace
   - Include file naming conventions (e.g., `.github/instructions/`, `.github/skills/`)
   - Provide copy-paste or CLI instructions

2. **Application subsection**:
   - How Copilot discovers and applies items
   - File locations (`copilot-instructions.md`, `.github/instructions/`, `.github/skills/`)
   - When items take effect (workspace-level vs task-specific)

3. **External link** (if applicable):
   - Link to awesome-copilot or official documentation
   - Example format: "For more instructions, visit [awesome-copilot repository](https://github.com/github/awesome-copilot)"

---

## Step 4: Build Item Reference Table
1. **Table Format**:
   ```markdown
   | Item | Description |
   |---|---|
   | [Item Name](link/to/item) | One-line description of purpose/benefit |
   ```

2. **Item Selection** (3-7 recommended):
   - Choose representative examples
   - Link to actual files (local or external repository)
   - Write concise descriptions (10-20 words each)
   - Include diverse examples if applicable

3. **Link Configuration**:
   - **Local files**: `[name](./path/to/file.md)` relative paths
   - **External (awesome-copilot)**: `[name](https://raw.githubusercontent.com/github/awesome-copilot/main/path/to/file.instructions.md)` or `https://github.com/github/awesome-copilot/blob/main/path/to/file.instructions.md`
   - **Custom repos**: Use appropriate full URLs

---

## Step 5: Create "Discover More" Section (if needed)
Include if documenting >7 items or referring to external source:

1. **Section structure**:
   ```markdown
   ## Discover More [Items]
   
   For additional [instructions/skills], visit the [awesome-copilot repository](https://github.com/github/awesome-copilot) organized by:
   - Languages (Python, JavaScript, Java, C#, etc.)
   - Frameworks (React, Vue, Angular, etc.)
   - Tools & Platforms (Azure, AWS, GitHub Actions, etc.)
   - Development practices (Testing, Security, Performance, etc.)
   ```

2. **Link to external discovery**:
   - awesome-copilot repo: https://github.com/github/awesome-copilot/tree/main/instructions
   - Include category examples to guide users

---

## Step 6: Add Reference Sections
1. **Official Documentation** section:
   ```markdown
   ## Official Documentation
   
   - [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
   - [How Custom Instructions Work](https://docs.github.com/en/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot)
   ```

2. **Optional Additional Sections**:
   - "How [Items] Work" - Brief explanation of system
   - "Contributing" - How to add/improve items
   - "License" - Licensing information
   - "Quick Start" - Example usage

---

## Step 7: Create/Update README File
1. **File location**: Create at `<project>/docs/` with awesome-copilot naming convention: `README.md`, `README.instructions.md`, `README.skills.md`, etc.

2. **Content assembly**:
   - Combine all sections from Steps 1-6
   - Ensure markdown formatting is clean (proper spacing, list formatting)
   - Validate all links resolve correctly

3. **README structure example**:
   ```
   # 📋 Custom Instructions
   
   [Brief description]
   
   ## How to Use Custom Instructions
   
   **To Install:**
   - [Installation steps]
   
   **To Use/Apply:**
   - [Application steps]
   
   | Item | Description |
   |---|---|
   | [Item1](link) | Description |
   
   ## Discover More Instructions
   
   [Discovery text and links]
   
   ## Official Documentation
   
   - [Links]
   ```

---

## Step 8: Validate and Finalize
1. **Quality checks**:
   - ✅ All links resolve (no 404s)
   - ✅ Table formatting renders correctly in Markdown
   - ✅ Emoji displays properly
   - ✅ Descriptions are clear and concise
   - ✅ External URL formatting matches awesome-copilot style (if referencing)

2. **Format verification**:
   - ✅ Follows awesome-copilot structure
   - ✅ Consistent with other project READMEs
   - ✅ Proper heading hierarchy (H1, H2, H3)

3. **Presentation**:
   - Render in VS Code preview to confirm appearance
   - Test all markdown links work
   - Verify emoji display

---

## Output Deliverables
Provide user with:
- Path to generated/updated README file
- Summary of included items (count and types)
- Links tested and confirmed
- Confirmation that awesome-copilot format was applied
- Recommendations for additional improvements (if any)

---

## Reference Example
The [docs/README.instructions.md](../../../docs/README.instructions.md) file in this workspace demonstrates the generated output format with:
- 📋 header
- How to Use section linking to awesome-copilot
- Table of 3 example instructions
- Discover More section pointing to awesome-copilot repository
- Official Documentation reference

---

## Key Principles
1. **Consistency**: Match awesome-copilot template exactly
2. **Linkability**: Ensure all references are clickable and resolve
3. **Discovery**: Provide pathways for users to find additional resources
4. **Clarity**: Keep descriptions brief, scannable, and benefit-focused
5. **Maintenance**: Organize items logically for future updates