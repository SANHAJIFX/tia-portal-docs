# Contributing to TIA Portal Documentation Repository

Thank you for your interest in contributing to the TIA Portal Documentation Repository. This guide will help you understand how to add your own TIA Portal documentation to this repository.

## How to Add Documentation

### For Small Files (< 25MB)

For smaller files that are under GitHub's file size limit (25MB per file), you can add them directly:

1. Fork this repository
2. Clone your fork to your local machine
3. Add your documentation files to the appropriate directory:
   - Function Blocks → `/program-blocks/function-blocks/`
   - Functions → `/program-blocks/functions/`
   - Data Blocks → `/program-blocks/data-blocks/`
   - etc.
4. Commit your changes
5. Push to your fork
6. Create a pull request

### For Large Files (> 25MB)

For larger files, you have several options:

1. **Split the files**: If possible, split large PDF files into smaller sections.

2. **Use Git LFS**: For files up to 100MB, you can use Git Large File Storage:
   - Install Git LFS: https://git-lfs.github.com/
   - Initialize Git LFS: `git lfs install`
   - Track large files: `git lfs track "*.pdf"`
   - Ensure `.gitattributes` is committed
   - Add and commit your files as normal

3. **Use external storage**: For very large files (>100MB), upload them to an external storage service and add a link to the README.

## Exporting TIA Portal Documentation

### Steps to export documentation from TIA Portal:

1. Open your TIA Portal project
2. Select the desired program blocks
3. Right-click and select "Print"
4. Choose the desired output format (PDF recommended)
5. Save the exported documentation
6. Add the exported files to the appropriate directory in this repository

## Organization Guidelines

- Include clear file names that describe the content
- Update the README in the respective directory with details about the new files
- Follow the existing structure for consistency

## Questions

If you have any questions about contributing, please open an issue in the repository.

Thank you for helping to improve the TIA Portal documentation!