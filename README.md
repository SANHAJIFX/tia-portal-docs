# TIA Portal Documentation

This repository serves as a centralized location for TIA Portal documentation and resources. It provides a structured way to organize and access various documentation related to TIA Portal projects.

## Repository Purpose

- To maintain consistent documentation for TIA Portal projects
- To provide easy access to documentation for team members
- To version control documentation alongside code
- To establish documentation standards for TIA Portal projects

## Structure

- `/program-blocks/`: Contains documentation for program blocks (FBs, FCs, DBs, etc.)
  - `/program-blocks/function-blocks/`: Function Blocks (FB) documentation
  - `/program-blocks/functions/`: Functions (FC) documentation
  - `/program-blocks/data-blocks/`: Data Blocks (DB) documentation
  - `/program-blocks/organization-blocks/`: Organization Blocks (OB) documentation
  - `/program-blocks/tool-blocks/`: Tool Function Blocks (TB) and Tool Functions (TC)
  - `/program-blocks/safety/`: Safety-related blocks and administration
  - `/program-blocks/combined/`: Complete documentation split into manageable files

- `/protocols/`: Protocol documentation and specifications

- `/layouts/`: System layouts and diagrams

## Contents

The repository contains exported documentation from TIA Portal, including:

- Function Blocks (FB)
- Functions (FC)
- Data Blocks (DB) - Global, Instance, and SCADA
- Organization Blocks (OB)
- Tool Function Blocks (TB) and Tool Functions (TC)
- Safety blocks and administration
- Protocol specifications
- System layouts and diagrams

## How to Use This Repository

1. **Browse Documentation**: Navigate through the directory structure to find the documentation you need.
2. **Download Files**: Each folder contains README files with details about the available documentation.
3. **Combined Documentation**: For a complete set of all program blocks, check the `/program-blocks/combined/` directory which contains the entire documentation split into manageable PDF files (each under 20MB).
4. **Add Documentation**: See [CONTRIBUTING.md](./CONTRIBUTING.md) for instructions on how to add your own documentation.

## Adding Large Files

Due to GitHub file size limitations (25MB for standard uploads, 100MB for Git LFS), large documentation files need special handling:

1. For files up to 100MB, use Git Large File Storage (LFS)
2. For files over 100MB, consider splitting them into smaller parts or hosting them externally

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed instructions and [GIT_LFS_SETUP.md](./GIT_LFS_SETUP.md) for Git LFS setup.

## Documentation Standards

To maintain consistency:

1. Use clear and descriptive filenames
2. Place files in the appropriate directory based on content
3. Update README files with descriptions of added documentation
4. Include version numbers and dates when applicable

## Local Setup for Documentation Work

For working with TIA Portal documentation:

1. TIA Portal V16 or later recommended for exporting documentation
2. Use PDF format for maximum compatibility
3. For large exports, consider using the "Split PDFs" option in TIA Portal print settings, as was done for the files in the `/program-blocks/combined/` directory

## Contact

If you have questions about this repository or need assistance with TIA Portal documentation, please open an issue in this repository.