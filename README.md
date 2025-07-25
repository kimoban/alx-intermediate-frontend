# alx-intermediate-frontend
This project focuses on building a solid foundation in Semantic HTML while emphasizing accessibility, SEO optimization, and the implementation of ARIA roles for enhanced usability. Through incremental tasks, a web page is structured and enhanced to make it not only visually structured but also optimized for screen readers and search engines. The project will lead to an understanding of the importance of semantic elements and accessibility features in modern web development.

## CSS Preprocessors: SASS/SCSS for Efficient Styling
### Objective
Learn to use CSS preprocessors for more efficient and manageable styling by exploring SASS/SCSS features and techniques.

#### Topics Covered
##### Introduction to SASS/SCSS
What is SASS/SCSS? SASS (Syntactically Awesome Style Sheets) and SCSS (Sassy CSS) are popular CSS preprocessors that add powerful features to CSS. They allow developers to write code that is more maintainable, scalable, and readable by introducing variables, nesting, modules, mixins, and more.

### Why Use SASS/SCSS?

**Enhanced CSS**: SASS/SCSS extends CSS with advanced features.
**Maintainability**: Easier to manage large stylesheets.
**Reusability**: Encourages code reuse with mixins and modules.  

### Variables and Nesting
#### Variables

Variables allow you to store values that can be reused throughout your stylesheet, making it easier to maintain consistent styling. They are declared using the $ symbol.

$primary-color: #333;
$font-stack: Helvetica, sans-serif;

body {  
  font: 100% $font-stack;  
  color: $primary-color;  
}  

#### Nesting

Nesting enables you to write CSS rules in a hierarchical structure that mirrors the HTML structure, improving readability and organization.

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

### Mixins and Functions
#### Mixins

Mixins allow you to create reusable chunks of CSS. You can pass arguments to mixins to make them more flexible.

```
@mixin theme($theme: DarkGray) {  
  background: $theme;  
  box-shadow: 0 0 1px rgba($theme, 0.25);  
  color: #fff;  
}  

.info {  
  @include theme;  
}  
.alert {  
  @include theme(DarkRed);  
}  
```

#### Functions

SASS functions let you perform calculations and return values. They are useful for creating dynamic styles.
```
@function double($number) {  
  @return $number * 2;  
}  

.box {  
  width: double(20px);  
}  
```
### Partials and Import
#### Partials

Partials are small SASS files that contain snippets of CSS. They are useful for organizing styles into modular, reusable pieces. A partial file name begins with an underscore (e.g., _variables.scss).

Importing Partials You can import partials into your main SASS file using the @use or @import rule to keep your styles organized.
```
// styles.scss  
@use 'variables';  
@use 'mixins';  

body {  
  font: 100% variables.$font-stack;  
}  
```
### Compiling SASS/SCSS
#### Tools for Compiling

To use SASS/SCSS, you need to compile it into standard CSS. This can be done using command-line tools, task runners, or build systems like:

**Command Line**: sass input.scss output.css
**Watching Files**: sass --watch input.scss:output.css
**Build Tools**: Webpack, Gulp, or Grunt

### Workflow Integration

Integrating SASS/SCSS compilation into your development workflow ensures that your styles are always up-to-date.

By mastering these features of SASS/SCSS, you can create more efficient and manageable stylesheets that improve the maintainability and scalability of your projects.

## Instructions on Set Up:

Inside the alx-intermediate-frontend repository, create a new directory called 0x03-sass_scss

### Linux installation (Optional)
In your ubuntu terminal install node version 20.16 as follows:  
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash  
Exit the terminal using the exit command then reopen it.  

### Installation Anywhere (Optional)
Install SASS by using the following command if you have node installed:  
npm install sass -v 3.7.4  
Create an empty file 0-installation-script.  




# 0x00-semantic_html

# Semantic HTML Project

## Overview

This project demonstrates the progressive implementation of semantic HTML elements, accessibility features, and best practices for web development. The project consists of four HTML files that showcase different levels of semantic markup and accessibility implementation.

## Project Structure

```
0x00-semantic_html/
├── README.md
├── 0-index.html          # Basic semantic structure
├── 1-index.html          # Enhanced meta tags and SEO
├── 2-index.html          # Advanced semantic elements
└── 3-index.html          # Complete with accessibility features
```

## File Descriptions

### 0-index.html

- **Purpose**: Basic semantic HTML structure
- **Features**:
  - Fundamental HTML5 semantic elements (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`)
  - Basic navigation structure
  - Minimal but proper document structure
  - Responsive viewport meta tag

### 1-index.html

- **Purpose**: Enhanced SEO and meta tag implementation
- **Features**:
  - Comprehensive meta tags for SEO
  - Keywords and description meta tags
  - Author meta tag
  - Enhanced document metadata
  - Same semantic structure as 0-index.html

### 2-index.html

- **Purpose**: Advanced semantic elements and content structure
- **Features**:
  - Blog-style content structure
  - Proper heading hierarchy (h1, h2, h3)
  - Time element with datetime attribute
  - Figure and figcaption elements
  - Code element for inline code snippets
  - Article header and footer
  - Structured navigation with lists
  - Publication date and author information

### 3-index.html

- **Purpose**: Complete implementation with accessibility features
- **Features**:
  - All features from 2-index.html
  - Accessible form implementation
  - ARIA attributes (aria-labelledby, aria-required, aria-label, aria-live)
  - Form validation and user feedback
  - Screen reader friendly markup
  - Proper form labeling and input associations

## Semantic HTML Elements Used

| Element | Purpose | File(s) |
|---------|---------|---------|
| `<header>` | Page/section header | All files |
| `<nav>` | Navigation container | All files |
| `<main>` | Main content area | All files |
| `<article>` | Self-contained content | All files |
| `<section>` | Thematic grouping | All files |
| `<footer>` | Page/section footer | All files |
| `<h1>`, `<h2>`, `<h3>` | Heading hierarchy | 2-index.html, 3-index.html |
| `<time>` | Date/time information | 2-index.html, 3-index.html |
| `<figure>` | Self-contained content | 2-index.html, 3-index.html |
| `<figcaption>` | Figure caption | 2-index.html, 3-index.html |
| `<code>` | Inline code | 2-index.html, 3-index.html |
| `<form>` | User input form | 3-index.html |
| `<label>` | Form input labels | 3-index.html |

## Accessibility Features

### ARIA Attributes

- `aria-labelledby`: Associates form with its title
- `aria-required`: Indicates required form fields
- `aria-label`: Provides accessible names for elements
- `aria-live`: Announces dynamic content changes
- `role`: Defines element purpose for assistive technologies

### Form Accessibility

- Proper label-input associations using `for` and `id` attributes
- Required field indicators
- Accessible submit button
- Live region for form feedback
- Semantic form structure

## SEO Features

### Meta Tags (1-index.html onwards)

- **Description**: Concise page description for search engines
- **Keywords**: Relevant keywords for content discovery
- **Author**: Content attribution
- **Viewport**: Mobile-responsive design support

### Content Structure

- Proper heading hierarchy for content outline
- Semantic markup for better content understanding
- Structured data through semantic elements

## Best Practices Demonstrated

1. **Progressive Enhancement**: Each file builds upon the previous one
2. **Semantic Markup**: Meaningful HTML elements for content structure
3. **Accessibility First**: Screen reader and keyboard navigation support
4. **SEO Optimization**: Meta tags and semantic structure for search engines
5. **Responsive Design**: Mobile-friendly viewport configuration
6. **Form Usability**: Accessible and user-friendly form implementation

## Browser Compatibility

These HTML files use standard HTML5 elements and are compatible with:

- All modern browsers (Chrome, Firefox, Safari, Edge)
- Internet Explorer 9+
- Mobile browsers (iOS Safari, Chrome Mobile, etc.)

## Validation

All HTML files follow W3C HTML5 standards and can be validated using:

- [W3C Markup Validator](https://validator.w3.org/)
- [WAVE Web Accessibility Evaluator](https://wave.webaim.org/)

## Learning Objectives

This project demonstrates:

- Understanding of HTML5 semantic elements
- Implementation of accessibility best practices
- SEO optimization techniques
- Progressive enhancement methodology
- Form accessibility and usability
- Proper document structure and hierarchy

## Usage

1. Open any HTML file in a web browser
2. Use browser developer tools to inspect the semantic structure
3. Test accessibility using screen readers or accessibility tools
4. Validate markup using W3C validators
5. Compare different implementations across files

## Future Enhancements

Potential improvements could include:

- CSS styling for visual presentation
- JavaScript for form validation and interactivity
- Additional ARIA landmarks
- Microdata or JSON-LD structured data
- Enhanced error handling and user feedback

## Contributing

When contributing to this project:

1. Maintain semantic HTML structure
2. Follow accessibility guidelines (WCAG 2.1)
3. Ensure W3C validation compliance
4. Test with screen readers
5. Document any new features or elements used

## Resources

- [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3C HTML5 Specification](https://www.w3.org/TR/html52/)
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/)

## License

This project is created for educational purposes as part of the ALX Professional Development program.

### Last updated: July 25, 2025
