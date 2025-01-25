# Description
This is a template for an c++ project.

# Compile and Run
## Manually
1. Configure the project:
   ```
   cmake -B build -DCMAKE_BUILD_TYPE=Release
   ```
2. Compile using 8 cores:
   ```
   cmake --build build --config Release -j 8
   ```
3. Run:
   ```
   ./build/src/main/main_app
   ```

## VSCode
1. Execute script:
   ```
   ./use_default_vscode_configs.sh
   ```
2. Press F5 to run "CMAKE BUILD DEBUG" task and then "DEBUG APP" configuration

# Using as a Template for a New Project
## Setup
1. Update the `CMakeLists.txt` file and `create_new_module.sh` script:
   - Replace all occurrences of `projectname` with your desired project name.
2. Remove example modules:
   - Delete the `src/hello_world` and `src/main` directories.
3. Create your own modules using the `create_new_module.sh` script. Examples:
   - For an application module:
     ```
     ./create_new_module.sh app main
     ```
   - For a library module:
     ```
     ./create_new_module.sh lib app-utils
     ```
4. Apply default VS Code configurations:
   ```
   ./use_default_vscode_configs.sh
   ```
