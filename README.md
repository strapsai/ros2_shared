Content created by Yaoyu's AI assistant. Use with care.

# ROS 2 Shared

`ros2_shared` is a C++ header-only utility library providing a set of macros and helper functions to simplify common ROS 2 development patterns. It focuses on reducing boilerplate code for parameter management, context handling, and string formatting within ROS 2 nodes.

## Overview

The library provides a collection of C++ headers designed to make ROS 2 code more concise and readable. It is particularly useful for large-scale projects where standardizing parameter access and logging is critical.

## Key Features

- **Parameter Macros**: `param_macros.hpp` provides a simplified interface for declaring and retrieving ROS 2 parameters with default values.
- **Context Management**: `context_macros.hpp` offers helpers for managing node contexts and lifecycle.
- **Enhanced Formatting**: `string_printf.hpp` includes utilities for safe, `printf`-style string formatting in C++.

## Repository Structure

- `include/ros2_shared/`:
    - `param_macros.hpp`: Simplified parameter handling.
    - `context_macros.hpp`: Node context utilities.
    - `string_printf.hpp`: Safe string formatting.

## Prerequisites

- **ROS 2 Humble / Rolling**
- **C++17**
- **Dependencies**:
  - `rclcpp`

## Usage

Include the headers in your C++ ROS 2 node:

```cpp
#include <ros2_shared/param_macros.hpp>

// Example parameter declaration
unsigned int my_param;
GET_PARAM(node, "my_parameter_name", my_param, 100u);
```

## Installation

1. Clone the repository into your ROS 2 workspace:
   ```bash
   cd ~/ros2_ws/src
   git clone https://github.com/strapsai/ros2_shared.git
   ```

2. Build the package:
   ```bash
   cd ~/ros2_ws
   colcon build --packages-select ros2_shared
   ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
