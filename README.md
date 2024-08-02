# Dace Menu
DACE and associated projects.



## Cloning the Repository with Submodules Set to Main Branch

To clone the repository and ensure all submodules are set to the `main` branch, you can use the following script:

```bash
#!/bin/bash

# Clone the repository recursively
git clone --recursive https://github.com/YanghuiWu/locality_dir.git
cd locality_dir

# Set each submodule to track the 'main' branch
git submodule foreach 'git checkout main || git checkout -b main origin/main'

# Update each submodule to the latest commit on the 'main' branch
git submodule update --remote --merge
