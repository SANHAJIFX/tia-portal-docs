# Setting Up Git LFS for TIA Portal Documentation

This guide explains how to set up Git Large File Storage (LFS) to handle the large PDF files in this TIA Portal documentation repository.

## What is Git LFS?

Git LFS is an extension to Git that helps manage large files more efficiently. Instead of storing large files directly in the Git repository, Git LFS stores a pointer to the file and the actual file content is stored separately.

## Installation

### Windows

1. Download the Git LFS installer from [git-lfs.github.com](https://git-lfs.github.com/)
2. Run the installer and follow the instructions
3. Open a new Git Bash or Command Prompt window

### macOS

Using Homebrew:
```
brew install git-lfs
```

### Linux

Debian/Ubuntu:
```
sudo apt-get install git-lfs
```

RHEL/CentOS:
```
sudo yum install git-lfs
```

## Setup for This Repository

1. Clone the repository:
   ```
   git clone https://github.com/SANHAJIFX/tia-portal-docs.git
   cd tia-portal-docs
   ```

2. Initialize Git LFS for your user account (you only need to do this once):
   ```
   git lfs install
   ```

3. Configure Git LFS to track PDF files:
   ```
   git lfs track "*.pdf"
   ```

4. Make sure the `.gitattributes` file is committed:
   ```
   git add .gitattributes
   git commit -m "Configure Git LFS to track PDF files"
   ```

## Working with Git LFS

After setting up Git LFS, you can work with large files as you normally would with Git:

1. Add a large PDF file:
   ```
   git add path/to/large/file.pdf
   ```

2. Commit the file:
   ```
   git commit -m "Add documentation file"
   ```

3. Push to GitHub:
   ```
   git push
   ```

## Checking LFS Status

To see which files are being managed by Git LFS:
```
git lfs ls-files
```

## Troubleshooting

If you encounter issues with Git LFS:

1. Make sure Git LFS is installed correctly:
   ```
   git lfs version
   ```

2. Verify that Git LFS is initialized:
   ```
   git lfs install
   ```

3. Check if the file is being tracked by Git LFS:
   ```
   git lfs status
   ```

4. If a file is not being tracked correctly, you may need to remove it from the repository and add it again:
   ```
   git rm --cached path/to/file.pdf
   git add path/to/file.pdf
   ```

## LFS Storage Limits

Be aware that GitHub has storage and bandwidth limits for Git LFS:

- Free accounts: 1GB of free storage and 1GB of free bandwidth per month
- Paid accounts: Higher limits depending on the plan

For more information, see the [GitHub documentation on Git LFS](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage).

## Additional Resources

- [Official Git LFS documentation](https://git-lfs.github.com/)
- [GitHub's Git LFS documentation](https://docs.github.com/en/repositories/working-with-files/managing-large-files)