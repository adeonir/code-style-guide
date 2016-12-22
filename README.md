# Code Style Guide

> "Every line of code should appear to be written by a single person, no matter the number of contributors." - Chinese Proverb.

The following document describes the rules of writing in development languages that I use: HTML, CSS and JS.

The idea of this repository is not to be complete code guide, but just a place for me, and other developers who participate in my projects, be able to inform the coding standards used.

This is a live document, changes may occur at any time.

## Summary

1. [Syntax](#syntax)
1. [Declaration](#declaration)
1. [Class Name](#class-name)
1. [Performance](#performance)
1. [Comments](#comments)

<a name="syntax"></a>
## 1. Syntax

Use soft-tabs with two spaces:

```css
/* Good */
.nav-item {
  color: #fff;
}

/* Bad */
.nav-item {
    color: #fff;
}
```

Always use double quotes:

```css
/* Good */
.nav-item:after {
  content: "";
}

/* Bad */
.nav-item:after {
  content: '';
}
```

Include a single space before the opening bracket of a ruleset:

```css
/* Good */
.header {
  margin-bottom: 20px;
}

/* Bad */
.header{
  margin-bottom: 20px;
}
```

Include a single space after the colon of a declaration:

```css
/* Good */
.header {
  margin-bottom: 20px;
}

/* Bad */
.header {
  margin-bottom:20px;
}
```

Include a semi-colon at the end of the last declaration in a declaration block:

```css
/* Good */
.header {
  margin-bottom: 20px;
}

/* Bad */
.header {
  margin-bottom: 20px
}
```

Keep one declaration per line:

```css
/* Good */
.nav,
.footer,
.btn {
  color: #fff;
}

/* Bad */
.nav, .footer, .btn {
  color: #fff;
}
```

Separate each ruleset by a blank line:

```css
/* Good */
.nav {
  color: #fff;
}

.btn {
    color: #fff;
}

/* Bad */
.nav {
  color: #fff;
}
.btn {
  color: #fff;
}
```

Use lowercase and shorthand hex values:

```css
/* Good */
.footer {
  color: #fff;
}

/* Bad */
.footer {
  color: #ffffff;
}
```

Avoid specifying units in zero-values:

```css
/* Good */
.nav-item {
  padding: 0;
}

/* Bad */
.nav-item {
  padding: 0px;
}
```

Do not use values starting with zero:

```css
/* Good */
.nav-item {
  transition: color .3s;
}

/* Bad */
.nav-item {
  transition: color 0.3s;
}
```

<a name="declaration"></a>
## 2. Declaration

The declarations should be added in alphabetical order:

```css
/* Good */
.btn {
  background: #000;
  color: #fff;
  display: inline-block;
  margin: 0;
  padding: 10px;
}

/* Bad */
.btn {
  color: #fff;
  background: #000;
  margin: 0;
  padding: 10px;
  display: inline-block;
}
```

<a name="class-name"></a>
## 3. Class Name

Keep class lowercase and use dashes to separate the classname.

```css
/* Good */
.nav-item {
  background: #000;
}

/* Bad */
.navItem {
  background: #000;
}

.nav_item {
  background: #000;
}
```

Avoid giving too short names for class and always choose meaningful names that provide the class function.

```css
/* Good */
.btn {
  color: #fff;
}
.page-header {
  margin-bottom: 20px;
}
.progress-bar {
  padding: 0;
}

/* Bad */
.s {
  color: #fff;
}
.ph {
  margin-bottom: 20px;
}
.block {
  padding: 0;
}
```

<a name="performance"></a>
## 4. Performance

Never use IDs:

```css
/* Good */
.header {
  margin-bottom: 20px;
}

/* Bad */
#header {
  margin-bottom: 20px;
}
```

Do not use default selectors for generic rules, always preferring the use of classes:

```css
/* Good */
.form-control {
  border: 0;
}

/* Bad */
input[type="text"] {
  border: 0;
}
```

<a name="comments"></a>
## 5. Comments

Examples:

```css
/* Section block comment
======================================== */

/* Sub-section block comment
-------------------- */

/**
 * Block comment
 */

/* Basic comment */
```
