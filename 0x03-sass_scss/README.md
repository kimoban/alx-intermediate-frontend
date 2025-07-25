# 0x03 - Sass/SCSS Learning Project

## 📋 Project Overview

This project is part of the ALX Intermediate Frontend Development curriculum, focusing on learning and implementing Sass/SCSS fundamentals. It demonstrates key Sass features including debug statements, variables, nested selectors, and mixins.

## 🎯 Learning Objectives

By the end of this project, you should be able to:

- Understand what Sass means and its benefits over regular CSS
- Write Sass/SCSS code using the SCSS syntax
- Use Sass variables to store and reuse values
- Implement nested selectors for better code organization
- Create and use mixins for reusable code blocks
- Understand Sass debugging with `@debug` directive
- Compile Sass files to CSS using various methods

## 🛠️ Prerequisites

- Basic knowledge of HTML and CSS
- Node.js and npm installed on your system
- A text editor or IDE (VS Code recommended)

## ⚙️ Installation

### Method 1: Using the Installation Script

1. Make the installation script executable and run it:

   ```bash
   chmod +x 0-installation-script
   ./0-installation-script
   ```

### Method 2: Manual Installation

1. **Install Node.js using NVM (recommended):**

   ```bash
   # Install NVM
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
   
   # Restart your terminal or source the profile
   source ~/.bashrc
   
   # Install Node.js version 20.16.0
   nvm install 20.16.0
   nvm use 20.16.0
   ```

2. **Install Sass globally:**

   ```bash
   npm install -g sass
   ```

3. **Verify installation:**

   ```bash
   sass --version
   ```

## 📁 Project Structure

```
0x03-sass_scss/
├── 0-debug_log.scss          # Debug statement example
├── 0-debug_log.css           # Compiled CSS from debug example
├── 0-debug_log.css.map       # Source map for debugging
├── 0-installation-script     # Automated installation script
├── 1-color_variable.scss     # Variables demonstration
├── 2-nested_tag.scss         # Nested selectors example
├── 3-mixin_margins.scss      # Mixins implementation
└── README.md                 # Project documentation
```

## 📚 File Descriptions

### `0-debug_log.scss`

Demonstrates the use of Sass `@debug` directive for debugging purposes.

```scss
@debug "Hello world";
```

### `1-color_variable.scss`

Shows how to define and use Sass variables for consistent styling.

```scss
$text-color: #3D3D3D;

body {
  color: $text-color;
}

p {
  color: $text-color;
}
```

### `2-nested_tag.scss`

Illustrates nested selectors for better code organization and hierarchy.

```scss
body {
  margin: 0px;
  padding: 0px; 
  
  p {
    margin: 10px; 
  }
}
```

```
nav {  
  ul {  
    margin: 0;  
    padding: 0;  
    list-style: none;  
  }  
  li {  
    display: inline-block;  
  }  
  a {  
    display: block;  
    padding: 6px 12px;  
    text-decoration: none;  
  }  
}
```

### `3-mixin_margins.scss`

Demonstrates the creation and usage of mixins for reusable code blocks.

```scss
@mixin set-margin($left, $right) {
  margin-left: $left;
  margin-right: $right;
}

body {
  @include set-margin(10px, 10px);
}

div {
  @include set-margin(15px, 15px);
}
```

## 🚀 Usage

### Compiling Sass Files

1. **Compile a single file:**

   ```bash
   sass input.scss output.css
   ```

2. **Compile with source maps:**

   ```bash
   sass --source-map input.scss output.css
   ```

3. **Watch for changes:**

   ```bash
   sass --watch input.scss:output.css
   ```

4. **Watch entire directory:**

   ```bash
   sass --watch scss:css
   ```

### Example Commands for This Project

```bash
# Compile the debug log file
sass 0-debug_log.scss 0-debug_log.css

# Compile with watch mode
sass --watch 1-color_variable.scss:1-color_variable.css

# Compile all SCSS files
sass --watch .:. --style expanded
```

## 🔍 Key Sass Features Demonstrated

### 1. Variables

- Store reusable values like colors, fonts, and dimensions
- Syntax: `$variable-name: value;`

### 2. Nesting

- Write CSS selectors inside other selectors
- Follows the same visual hierarchy as HTML

### 3. Mixins

- Create reusable blocks of CSS declarations
- Can accept parameters for dynamic styling
- Syntax: `@mixin name($param) { ... }` and `@include name(value);`

### 4. Debug Statements

- Use `@debug` to output messages during compilation
- Helpful for troubleshooting and development

## 🎨 Sass vs SCSS

This project uses **SCSS** syntax, which is:

- Fully CSS-compatible
- Uses curly braces `{}` and semicolons `;`
- More familiar to developers coming from CSS

## 🧪 Testing Your Installation

1. Create a test SCSS file:

   ```scss
   $primary-color: #007bff;
   
   .test {
     color: $primary-color;
     
     &:hover {
       color: darken($primary-color, 10%);
     }
   }
   ```

2. Compile it:

   ```bash
   sass test.scss test.css
   ```

3. Check the output CSS file for proper compilation.

## 🛠️ Troubleshooting

### Common Issues

1. **"sass: command not found"**
   - Ensure Node.js and npm are installed
   - Install Sass globally: `npm install -g sass`

2. **Permission denied on installation script**
   - Make the script executable: `chmod +x 0-installation-script`

3. **Compilation errors**
   - Check syntax for missing semicolons or braces
   - Ensure proper indentation
   - Verify variable names are correct

## 📖 Additional Resources

- [Official Sass Documentation](https://sass-lang.com/documentation)
- [Sass Guidelines](https://sass-guidelin.es/)
- [Learn Sass in Y Minutes](https://learnxinyminutes.com/docs/sass/)
- [Sass Functions Reference](https://sass-lang.com/documentation/modules)

## 🤝 Contributing

This is a learning project. Feel free to:

1. Fork the repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

## 📝 License

This project is part of the ALX Software Engineering Program curriculum.

## 👨‍💻 Author

### Isaiah Kimoban

- ALX Software Engineering Program
- Intermediate Frontend Development Track

## Happy Styling with Sass! 🎨
