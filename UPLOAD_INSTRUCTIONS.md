# Instructions for Uploading TIA Portal Documentation

This guide provides step-by-step instructions for uploading your TIA Portal documentation to this repository, including handling the combined documentation files.

## Prerequisites

1. [Git](https://git-scm.com/downloads) installed on your computer
2. GitHub account with access to this repository
3. Basic knowledge of Git commands

## Setup Steps

### 1. Clone the Repository

```bash
git clone https://github.com/SANHAJIFX/tia-portal-docs.git
cd tia-portal-docs
```

### 2. Upload the Combined Documentation Files

The combined documentation files in `C:\TIA_Exported\PRINT\structered print all\program blocks\full version_backup\combined` are already split into manageable sizes (under 25MB each), so they can be uploaded directly:

```bash
# Create the directory if it doesn't exist
mkdir -p program-blocks/combined

# Copy all the PDF files to the repository
# Windows Command Prompt:
copy "C:\TIA_Exported\PRINT\structered print all\program blocks\full version_backup\combined\*.pdf" program-blocks\combined\

# Windows PowerShell:
Copy-Item "C:\TIA_Exported\PRINT\structered print all\program blocks\full version_backup\combined\*.pdf" -Destination "program-blocks\combined\"
```

### 3. Commit and Push the Files

```bash
# Add the files to Git
git add program-blocks/combined/*.pdf

# Commit the changes
git commit -m "Add combined TIA Portal documentation files"

# Push to GitHub
git push origin main
```

### 4. Optional: Set Up Git LFS for Other Large Files

For files larger than 25MB, you'll need to use Git LFS. Follow these steps:

1. Install Git LFS (see [GIT_LFS_SETUP.md](./GIT_LFS_SETUP.md) for details)
2. Set up Git LFS for the repository:

```bash
git lfs install
git lfs track "*.pdf"
git add .gitattributes
git commit -m "Configure Git LFS for tracking PDF files"
```

3. Add and commit your large files:

```bash
git add path/to/large/file.pdf
git commit -m "Add large documentation file"
git push origin main
```

## Alternate Method: Upload Files Through GitHub Web Interface

For smaller PDF files (under 25MB), you can also use the GitHub web interface:

1. Navigate to the appropriate directory in this repository on GitHub
2. Click the "Add file" button and select "Upload files"
3. Drag and drop your files or use the file selector
4. Add a commit message
5. Click "Commit changes"

## Checking Upload Status

To verify that your files have been properly uploaded:

1. Navigate to the repository on GitHub
2. Check the `program-blocks/combined/` directory
3. Confirm that all files are listed and accessible

## Troubleshooting

- If you encounter "file too large" errors, make sure you're using Git LFS for files over 25MB
- If Git LFS is not working, check that you've followed the setup instructions in [GIT_LFS_SETUP.md](./GIT_LFS_SETUP.md)
- For any other issues, please open an issue in the repository

## Need Help?

If you need assistance with uploading your documentation, please:

1. Check the [CONTRIBUTING.md](./CONTRIBUTING.md) and [GIT_LFS_SETUP.md](./GIT_LFS_SETUP.md) files
2. Open an issue in the repository describing your problem
3. Include any error messages or screenshots that might help diagnose the issue