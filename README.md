![Image ALT](https://raw.githubusercontent.com/CalestialAshley35/Standard-Storage-Language/refs/heads/main/images/file-SyE2uKvuarZU8s3Xinksn2.webp)

# Standard Storage Language (SSL)

## Overview
The **Standard Storage Language (SSL)** is a C++ program that provides a simple interface to store and retrieve data using string identifiers. It leverages `std::variant` to handle different types of data (`int`, `double`, and `std::string`) and uses an `unordered_map` for efficient lookups.

The SSL program supports the following commands:
1. `store`: Store data associated with a name.
2. `see`: Retrieve and display data by its name.

## Features
- **Multiple Data Types**: Supports `int`, `double`, and `std::string` (or text).
- **Interactive CLI**: Command-line interface for storing and retrieving data.
- **Input Validation**: Ensures valid input for the specified data type.
- **Flexible Text Input**: Allows multi-word strings or text values.

## Structure

### 1. **`StandardStorage` Class**
   - **Purpose**: Manages data storage and retrieval.
   - **Methods**:
     - `store(const std::string& dataName, const std::variant<int, double, std::string>& data)`: Stores the data.
     - `see(const std::string& dataName)`: Displays the stored data, handling its type dynamically.
   - **Private Members**:
     - `std::unordered_map<std::string, std::variant<int, double, std::string>> storage`: The data container.

### 2. **Utility Functions**
   - `is_integer(const std::string& str)`: Checks if a string represents a valid integer.
   - `is_double(const std::string& str)`: Checks if a string represents a valid floating-point number.

### 3. **Main Function**
   - **Interactive Commands**:
     - `store`: Prompts for a name, type, and value, and stores the data.
     - `see`: Displays the value of a given name, if it exists.
     - `exit`: Terminates the program.

## Usage

### Running the Program
Compile and run the program in a terminal:
```bash
g++ -std=c++17 -o standard_storage standard_storage.cpp
./standard_storage

   - **Private Members**:
     - `std::unordered_map<std::string, std::variant<int, double, std::string>> storage`: The storage container, mapping each data name to a `std::variant` containing the data.

### 2. **Main Function**
   - **Purpose**: A loop that allows the user to interact with the program by entering commands to either store or view data.
   - **Commands**:
     - `store`: Prompts the user to enter the data name and type (`int`, `double`, or `string`) and then stores the value.
     - `see`: Prompts the user to enter the data name and displays the corresponding stored value.
     - `exit`: Exits the program.

## How to Use

1. **Start the program** by running the compiled executable.
2. **Enter a command**:
   - To **store** data, use the `store` command:
     ```
     Enter a command (store or see) or 'exit' to quit: store
     Enter the name of the data: myData
     Enter the type of data (int, double, string): int
     Enter an integer value: 42
     ```
   - To **see** stored data, use the `see` command:
     ```
     Enter a command (store or see) or 'exit' to quit: see
     Enter the name of the data: myData
     Data (myData): 42
     ```
   - To **exit** the program, type `exit`:
     ```
     Enter a command (store or see) or 'exit' to quit: exit
     ```
```
## Example

Enter a command (store or see) or 'exit' to quit: store
Enter the name of the data: age
Enter the type of data (int, double, string, text): int
Enter an integer value: 30

Enter a command (store or see) or 'exit' to quit: store
Enter the name of the data: height
Enter the type of data (int, double, string, text): double
Enter a double value: 5.9

Enter a command (store or see) or 'exit' to quit: store
Enter the name of the data: message
Enter the type of data (int, double, string, text): text
Enter a string (text) value: Hello, world!

Enter a command (store or see) or 'exit' to quit: see
Enter the name of the data: age
Data (age): 30

Enter a command (store or see) or 'exit' to quit: see
Enter the name of the data: height
Data (height): 5.9

Enter a command (store or see) or 'exit' to quit: see
Enter the name of the data: message
Data (message): Hello, world!

Enter a command (store or see) or 'exit' to quit: exit

## Requirements
- A C++ compiler that supports C++17 or higher (for `std::variant`).

## **Compiling and Running the C++ Program**

```bash
### **1. On Linux **

# Step 1: Install Dependencies
pkg install clang
pkg install g++

# Step 2: Create a Folder for the Project
mkdir main
cd main

# Step 3: Download the C++ File
wget https://raw.githubusercontent.com/CalestialAshley35/Standard-Storage-Language/refs/heads/main/main/standard_storage.cpp

# Step 4: Compile the Program
g++ -std=c++17 -o standard_storage standard_storage.cpp

# Step 5: Run the Program
./standard_storage

The program will prompt you to enter a command like store, see, or exit.
```

---

2. On Windows (Code::Blocks)

```bash
# Step 1: Install Code::Blocks
# Download and install Code::Blocks from http://www.codeblocks.org/downloads/26.
# Make sure to select the version that includes MinGW (C++ compiler).

# Step 2: Open Code::Blocks
# - Open Code::Blocks, then create a new project by selecting `File > New > Project...` 
# - Choose the `Console Application` template, and follow the prompts.

# Step 3: Add the C++ File
# - Download the `standard_storage.cpp` file from the GitHub repository.
# - In Code::Blocks, right-click on the project folder in the left sidebar and choose `Add files...` to add the `standard_storage.cpp` file.

# Step 4: Compile the Program
# - Click the **Build** button (the gear icon) or press `Ctrl+F9` to compile the program.

# Step 5: Run the Program
# - Click the **Run** button (the green play icon) or press `Ctrl+F10` to run the program.
# The program will prompt for input like `store`, `see`, or `exit`.```
---
```

3. On macOS

```
# Step 1: Install Xcode Command Line Tools
# Ensure you have `g++` installed by running:
xcode-select --install

# Step 2: Create a Folder for the Project
mkdir main
cd main

# Step 3: Download the C++ File
curl -O https://raw.githubusercontent.com/CalestialAshley35/Standard-Storage-Language/refs/heads/main/main/standard_storage.cpp

# Step 4: Compile the Program
g++ -std=c++17 -o standard_storage standard_storage.cpp

# Step 5: Run the Program
./standard_storage

The program will prompt you to enter a command like store, see, or exit.
