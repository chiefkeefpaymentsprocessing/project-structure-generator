# Project Structure Generator

Automatically generate a clean and organized project directory structure for documentation and analysis. Perfect for developers needing a clear overview of large codebases.

## Features
- **Ignore Specific Directories**: Easily configure which directories should be ignored.
- **File Extension Filtering**: Only include files with specified extensions.
- **Pattern Matching**: Identify and group files based on regular expressions.
- **Special Directories**: Handle directories that follow special naming patterns differently.
- **Custom Output File**: Save the generated project structure to a customizable output file.

## Configuration

You can configure the script by modifying the following variables in the script:

- `ignore_dirs`: List of directory names to ignore. By default includes '**node_modules**, **lib**, **libs**, **.git**, **venv**, **chrome.app**, **.vscode**, **.pytest_cache**, **__pycache__**'.
- `extensions_to_include`: Define the file extensions of interest, such as '**.py**, **.json**, **.php**, **.csv**'.
- `patterns`: Define the patterns for identifying unique files. Example patterns: '**links_(\d+)-(\d+)\.csv**, **part_\d+\.csv**, **links_\d+\.csv**, **(.*)_part_(\d+)\.csv**'.
- `special_dir_patterns`: Define patterns for special directories, such as '**run_\d+**'.
- `output_file`: Output file path, which is '**project_structure.txt**' by default.

## Example Output
The script generates a text file (`project_structure.txt`) with the following format:

```
project_root/
│   ├── project_structure_generator.py
├── config/
│   ├── update_files.py
│   ├── initial_setup/
│   │   └── structure.py
│   │
├── data/
│   ├── processed_files/
│   │   ├── Categories.json
│   │   ├── Combined_File.json
├── src/
│   ├── data_fetch/
│   │   └── fetch_feeds.py
│   │
│   ├── data_processing/
│   │   ├── combine_feeds.py
│   │   └── populate_reference_files.py
├── tests/
│   ├── test_combine_feeds.py
│   └── test_integration.py
│
├── woopoint/
│   └── woopoint.php
```
