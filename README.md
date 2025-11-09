# AI Research Assistant Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain, update, and customize your AI Research Assistant landing page. Whether you're updating text, fixing links, or adding new pages, we'll walk through each step together.

---

## Table of Contents

1. [Understanding Your Landing Page Structure](#understanding-your-landing-page-structure)
2. [Updating Text and Content](#updating-text-and-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Color Customization](#color-customization)
7. [Responsive Design Best Practices](#responsive-design-best-practices)
8. [Troubleshooting Common Issues](#troubleshooting-common-issues)

---

## Understanding Your Landing Page Structure

Before making changes, let's understand how your landing page is organized:

### The Main Sections

Your landing page contains these key sections, in order from top to bottom:

| Section | Purpose | Location in Code |
|---------|---------|-----------------|
| **Header Navigation** | Logo, menu links, CTA button | Lines 78-135 |
| **Hero Section** | Main headline and introduction | Lines 137-207 |
| **Features Section** | Three main features (Reports, Market Analysis, Integration) | Lines 209-261 |
| **Benefits Section** | Four key benefits with icons | Lines 263-328 |
| **CTA Section** | Call-to-action with gradient background | Lines 330-354 |
| **Testimonials Section** | Customer reviews and ratings | Lines 356-460 |
| **About Us Section** | Company mission and values | Lines 462-483 |
| **FAQ Section** | Frequently asked questions with toggles | Lines 485-586 |
| **Footer** | Links, contact info, social media, copyright | Lines 588-691 |

### How the Page Works

Your landing page uses three main technologies working together:

- **HTML** - The structure and content (what appears on the page)
- **Tailwind CSS** - The styling and layout (how things look and position)
- **JavaScript** - The interactivity (what happens when you click things)

---

## Updating Text and Content

### Section 1: Header Navigation

The header appears at the very top of your page and stays visible as users scroll.

#### **Updating the Logo Text**

**Location:** Line 85-88

**Current code:**
```html
<span class="text-2xl font-bold" style="color: #5B4BFF;">AIResearch</span>
```

**To change "AIResearch" to your company name:**

1. Find the text `AIResearch` in the code
2. Replace it with your desired name
3. Example: `<span class="text-2xl font-bold" style="color: #5B4BFF;">ResearchAI Pro</span>`

**What each part means:**
- `text-2xl` = Makes text extra large
- `font-bold` = Makes text bold/thick
- `style="color: #5B4BFF;"` = Makes text purple

---

#### **Updating Navigation Menu Links**

**Location:** Lines 93-98 (Desktop Menu)

**Current code:**
```html
<a href="#features" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">FAQ</a>
```

**To rename a menu item:**

1. Find the menu link you want to change
2. Change the text between `>` and `</a>`
3. Example: Change `Features` to `Our Services`

```html
<a href="#features" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">Our Services</a>
```

**Important:** Keep the `href="#features"` the same—that's what makes the link work!

---

### Section 2: Hero Section (Main Headline)

The hero section is the first thing visitors see. It has a big headline and introduction.

#### **Updating the Main Headline**

**Location:** Lines 161-163

**Current code:**
```html
<h1 class="text-5xl md:text-6xl lg:text-6xl font-bold tracking-tight leading-tight" style="color: #5B4BFF;">
    AI Research Assistant
</h1>
```

**To change the headline:**

1. Find `AI Research Assistant`
2. Replace with your new headline
3. Keep the tags (`<h1>` and `</h1>`) exactly as they are

**Example:**
```html
<h1 class="text-5xl md:text-6xl lg:text-6xl font-bold tracking-tight leading-tight" style="color: #5B4BFF;">
    Revolutionize Your Research Today
</h1>
```

**Understanding the sizing classes:**
- `text-5xl` = Size on small screens (phones)
- `md:text-6xl` = Size on medium screens (tablets)
- `lg:text-6xl` = Size on large screens (desktops)

---

#### **Updating the Hero Description**

**Location:** Lines 165-170

**Current code:**
```html
<p class="text-lg md:text-xl text-gray-600 font-light leading-relaxed max-w-2xl">
    Experience cutting-edge artificial intelligence designed to revolutionize your research workflow. Our advanced AI research assistant offers unprecedented capabilities without the complexity of traditional development.
</p>
```

**To change the description:**

1. Find the paragraph text
2. Replace it with your new description
3. Keep the HTML tags (`<p>` and `</p>`) the same

**Example:**
```html
<p class="text-lg md:text-xl text-gray-600 font-light leading-relaxed max-w-2xl">
    Unlock powerful insights in minutes, not weeks. Our AI-powered platform transforms how teams conduct research and make data-driven decisions.
</p>
```

---

#### **Updating Hero Buttons**

**Location:** Lines 172-180

**Current code:**
```html
<a href="https://www.upflexdigital.com/contact" class="gradient-btn px-8 py-4 rounded-lg text-white font-bold text-lg text-center hover:scale-105 transition-transform duration-300">
    Start Your Journey
</a>
<button class="px-8 py-4 rounded-lg border-2 border-[#5B4BFF] text-[#5B4BFF] font-bold text-lg hover:bg-[#EEF0FF] transition-all duration-300">
    Learn More
</button>
```

**To change button text:**

1. Change `Start Your Journey` to your new text
2. Change `Learn More` to your new text
3. Don't change the `href` attribute (the link address)

**Example:**
```html
<a href="https://www.upflexdigital.com/contact" class="gradient-btn px-8 py-4 rounded-lg text-white font-bold text-lg text-center hover:scale-105 transition-transform duration-300">
    Get Started Free
</a>
<button class="px-8 py-4 rounded-lg border-2 border-[#5B4BFF] text-[#5B4BFF] font-bold text-lg hover:bg-[#EEF0FF] transition-all duration-300">
    Schedule Demo
</button>
```

---

#### **Updating Hero Feature Badges**

**Location:** Lines 182-195

**Current code:**
```html
<div class="flex items-center gap-2">
    <span class="material-symbols-rounded text-[#00E5A8] text-2xl">check_circle</span>
    <span class="text-sm font-medium text-gray-700">Instant Results</span>
</div>
<div class="flex items-center gap-2">
    <span class="material-symbols-rounded text-[#00E5A8] text-2xl">shield</span>
    <span class="text-sm font-medium text-gray-700">Enterprise Security</span>
</div>
<div class="flex items-center gap-2">
    <span class="material-symbols-rounded text-[#00E5A8] text-2xl">bolt</span>
    <span class="text-sm font-medium text-gray-700">Lightning Fast</span>
</div>
```

**To change the badge text:**

1. Find the text you want to change (e.g., "Instant Results")
2. Replace it with new text
3. Keep everything else the same

**Example:**
```html
<div class="flex items-center gap-2">
    <span class="material-symbols-rounded text-[#00E5A8] text-2xl">check_circle</span>
    <span class="text-sm font-medium text-gray-700">Real-Time Analysis</span>
</div>
```

**To change the icon:**

1. Find the icon name (e.g., `check_circle`)
2. Replace with a different [Material Symbol](https://fonts.google.com/icons)
3. Example: `check_circle` → `verified` or `shield` → `lock`

---

### Section 3: Features Section

This section showcases your three main features.

#### **Updating Feature Cards**

**Location:** Lines 218-261

**Current code for Feature 1:**
```html
<div class="card-hover bg-white rounded-2xl p-8 border border-[#EEF0FF] shadow-lg hover:shadow-2xl">
    <div class="w-16 h-16 bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] rounded-xl flex items-center justify-center mb-6 shadow-lg">
        <span class="material-symbols-rounded text-white text-3xl">description</span>
    </div>
    <h3 class="text-2xl font-bold mb-4" style="color: #5B4BFF;">Comprehensive Reports</h3>
    <p class="text-gray-600 font-light leading-relaxed mb-4">
        Generate detailed, professional reports instantly. Our AI analyzes complex data patterns and presents them in clear, actionable formats that stakeholders can immediately understand and act upon.
    </p>
    <div class="flex items-center gap-2 text-[#00E5A8] font-bold hover:gap-3 transition-all duration-300 cursor-pointer">
        <span>Learn More</span>
        <span class="material-symbols-rounded text-xl">arrow_forward</span>
    </div>
</div>
```

**To change a feature title:**

1. Find `Comprehensive Reports`
2. Replace with your new title

**To change the feature description:**

1. Find the paragraph text
2. Replace with your new description

**To change the feature icon:**

1. Find `description` (the icon name)
2. Replace with a different [Material Symbol](https://fonts.google.com/icons)
3. Example: `description` → `assessment` or `document`

**Complete example with all changes:**
```html
<div class="card-hover bg-white rounded-2xl p-8 border border-[#EEF0FF] shadow-lg hover:shadow-2xl">
    <div class="w-16 h-16 bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] rounded-xl flex items-center justify-center mb-6 shadow-lg">
        <span class="material-symbols-rounded text-white text-3xl">assessment</span>
    </div>
    <h3 class="text-2xl font-bold mb-4" style="color: #5B4BFF;">Advanced Analytics</h3>
    <p class="text-gray-600 font-light leading-relaxed mb-4">
        Dive deep into your data with powerful analytics tools. Uncover hidden patterns and gain actionable insights that drive business growth.
    </p>
    <div class="flex items-center gap-2 text-[#00E5A8] font-bold hover:gap-3 transition-all duration-300 cursor-pointer">
        <span>Learn More</span>
        <span class="material-symbols-rounded text-xl">arrow_forward</span>
    </div>
</div>
```

---

### Section 4: Benefits Section

This section highlights four key benefits with icons and descriptions.

#### **Updating Benefits**

**Location:** Lines 289-328

**Current code for Benefit 1:**
```html
<div class="flex gap-6 items-start">
    <div class="flex-shrink-0">
        <div class="w-14 h-14 bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] rounded-xl flex items-center justify-center shadow-lg">
            <span class="material-symbols-rounded text-white text-2xl">auto_awesome</span>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold mb-3" style="color: #5B4BFF;">Intelligent Inference</h3>
        <p class="text-gray-600 font-light leading-relaxed">
            Our advanced AI doesn't just process data—it understands context and makes intelligent inferences. Draw meaningful conclusions from complex datasets with AI that thinks like a researcher, identifying patterns and correlations you might miss.
        </p>
    </div>
</div>
```

**To update a benefit:**

1. Change the icon: Replace `auto_awesome` with another icon
2. Change the title: Replace `Intelligent Inference`
3. Change the description: Replace the paragraph text

**Example:**
```html
<div class="flex gap-6 items-start">
    <div class="flex-shrink-0">
        <div class="w-14 h-14 bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] rounded-xl flex items-center justify-center shadow-lg">
            <span class="material-symbols-rounded text-white text-2xl">psychology</span>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold mb-3" style="color: #5B4BFF;">Smart Insights</h3>
        <p class="text-gray-600 font-light leading-relaxed">
            Get intelligent recommendations based on your data. Our AI learns your preferences and suggests actions that have the highest impact on your goals.
        </p>
    </div>
</div>
```

---

### Section 5: Testimonials Section

Update customer testimonials to match your actual users.

#### **Updating Testimonial Content**

**Location:** Lines 410-460

**Current code for Testimonial 1:**
```html
<div class="card-hover bg-white rounded-2xl p-8 border border-[#EEF0FF] shadow-lg hover:shadow-2xl">
    <div class="flex gap-1 mb-4">
        <span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
        <span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
        <span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
        <span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
        <span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
    </div>
    <p class="text-gray-700 font-light leading-relaxed mb-6">
        "This AI research assistant has completely revolutionized how our team conducts market analysis. What used to take weeks now takes hours. The reports are incredibly detailed and the insights are spot-on. We've already seen a 40% improvement in our research turnaround time."
    </p>
    <div class="flex items-center gap-4">
        <div class="w-12 h-12 bg-gradient-to-br from-[#5B4BFF] to-[#00E5A8] rounded-full flex items-center justify-center text-white font-bold">
            SR
        </div>
        <div>
            <p class="font-bold text-gray-900">Sarah Richardson</p>
            <p class="text-sm text-gray-600 font-light">Head of Research, TechVentures Inc</p>
        </div>
    </div>
</div>
```

**To update a testimonial:**

1. **Change the quote text:** Replace the text between the quotation marks
2. **Change the customer name:** Replace `Sarah Richardson`
3. **Change the job title:** Replace `Head of Research, TechVentures Inc`
4. **Change the initials:** Replace `SR` with the customer's actual initials

**Example:**
```html
<p class="text-gray-700 font-light leading-relaxed mb-6">
    "The platform is intuitive and powerful. Our team was able to implement it within a week and immediately saw results. Highly recommended!"
</p>
<!-- ... -->
<p class="font-bold text-gray-900">John Smith</p>
<p class="text-sm text-gray-600 font-light">CEO, DataTech Solutions</p>
```

**To change the star rating:**

If you want fewer stars, simply remove star lines:
```html
<!-- 5 stars (current) -->
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>

<!-- 4 stars (remove one line) -->
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
<span class="material-symbols-rounded text-[#00E5A8] text-2xl">star</span>
```

---

### Section 6: FAQ Section

Update frequently asked questions relevant to your business.

#### **Updating FAQ Items**

**Location:** Lines 530-586

**Current code for FAQ Item 1:**
```html
<div class="faq-item bg-white border border-[#EEF0FF] rounded-xl overflow-hidden shadow-md hover:shadow-lg transition-shadow duration-300">
    <button class="faq-question w-full px-8 py-6 flex items-center justify-between cursor-pointer hover:bg-[#EEF0FF] transition-colors duration-300">
        <h3 class="text-lg font-bold text-left" style="color: #5B4BFF;">How does the AI research assistant work?</h3>
        <span class="faq-icon material-symbols-rounded text-[#5B4BFF] text-2xl transition-transform duration-300">expand_more</span>
    </button>
    <div class="faq-answer hidden px-8 pb-6 bg-[#EEF0FF] bg-opacity-30">
        <p class="text-gray-700 font-light leading-relaxed">
            Our AI research assistant leverages advanced machine learning models, specifically Claude AI by Anthropic, to process and analyze complex datasets. It works by ingesting your data, identifying patterns and correlations, applying sophisticated inference algorithms, and then presenting findings in comprehensive, actionable reports. The system learns from your specific research methodologies and continuously improves its accuracy over time. You simply input your research parameters, and our AI handles the heavy lifting—data processing, analysis, insight generation, and report creation—all within seconds.
        </p>
    </div>
</div>
```

**To update a FAQ question:**

1. Find the question text (e.g., "How does the AI research assistant work?")
2. Replace with your new question

**To update a FAQ answer:**

1. Find the answer paragraph
2. Replace with your new answer

**Example:**
```html
<h3 class="text-lg font-bold text-left" style="color: #5B4BFF;">What are your pricing plans?</h3>

<!-- Later in the answer section: -->
<p class="text-gray-700 font-light leading-relaxed">
    We offer flexible pricing starting at $99/month for small teams, with enterprise plans available. All plans include 24/7 support and access to our full feature set.
</p>
```

---

### Section 7: Footer

The footer contains important links and information at the bottom of the page.

#### **Updating Footer Text**

**Location:** Lines 595-691

**Current code for footer tagline:**
```html
<p class="text-gray-400 font-light leading-relaxed">
    Transforming research with cutting-edge AI technology powered by Claude.
</p>
```

**To change the tagline:**

1. Replace the text between `<p>` and `</p>`

**Example:**
```html
<p class="text-gray-400 font-light leading-relaxed">
    Your trusted partner in intelligent research and data analysis.
</p>
```

#### **Updating Footer Contact Information**

**Location:** Lines 649-671

**Current code:**
```html
<div class="flex items-center gap-4">
    <div class="w-12 h-12 bg-gray-800 rounded-lg flex items-center justify-center">
        <span class="material-symbols-rounded text-[#00E5A8]">mail</span>
    </div>
    <div>
        <p class="text-gray-400 text-sm font-light">Email</p>
        <p class="text-white font-bold"><a href="mailto:info@upflexdigital.com" class="hover:text-[#00E5A8] transition-colors duration-300">info@upflexdigital.com</a></p>
    </div>
</div>
```

**To change the email address:**

1. Find `info@upflexdigital.com` (appears twice)
2. Replace both instances with your email

**Example:**
```html
<p class="text-white font-bold"><a href="mailto:support@yourcompany.com" class="hover:text-[#00E5A8] transition-colors duration-300">support@yourcompany.com</a></p>
```

**To change the location:**

1. Find the location section
2. Replace `San Francisco, CA` with your location

---

#### **Updating Footer Copyright**

**Location:** Lines 676-679

**Current code:**
```html
<p class="text-gray-400 font-light text-center md:text-left">
    &copy; 2025 Upflex Digital. All rights reserved. Powered by Claude AI.
</p>
```

**To change the copyright:**

1. Replace `2025` with the current year
2. Replace `Upflex Digital` with your company name
3. Keep `&copy;` (it displays as ©)

**Example:**
```html
<p class="text-gray-400 font-light text-center md:text-left">
    &copy; 2025 Your Company Name. All rights reserved. Powered by Claude AI.
</p>
```

---

## Modifying Tailwind CSS Classes

Tailwind CSS uses utility classes to style your page. These are the short class names you see in the HTML.

### Understanding Common Classes

**Text Sizing:**
```
text-sm    = Small text
text-base  = Normal text
text-lg    = Large text
text-xl    = Extra large text
text-2xl   = 2x extra large text
text-5xl   = 5x extra large text
```

**Text Styling:**
```
font-light    = Thin text
font-normal   = Regular text
font-bold     = Thick/bold text
text-gray-600 = Dark gray color
text-white    = White text
```

**Spacing:**
```
p-4    = Padding (internal space) - 4 units
px-8   = Horizontal padding - 8 units
py-6   = Vertical padding - 6 units
gap-4  = Space between items - 4 units
mb-6   = Bottom margin (external space) - 6 units
```

**Layout:**
```
flex              = Display items in a row
flex-col          = Display items in a column
items-center      = Vertically center items
justify-between   = Space items apart
rounded-lg        = Slightly rounded corners
rounded-2xl       = Very rounded corners
```

**Responsive:**
```
md:text-6xl   = On medium screens (tablets), use text-6xl
lg:flex       = On large screens (desktops), use flex
hidden        = Hide element
md:hidden     = Hide on medium+ screens
```

### Common Modifications

#### **Changing Button Size**

**Current code:**
```html
<a href="https://www.upflexdigital.com/contact" class="gradient-btn px-8 py-4 rounded-lg text-white font-bold text-lg">
    Get Started
</a>
```

**To make button larger:**
- Change `px-8 py-4` to `px-10 py-5`
- Change `text-lg` to `text-xl`

**To make button smaller:**
- Change `px-8 py-4` to `px-6 py-3`
- Change `text-lg` to `text-base`

---

#### **Changing Spacing Between Sections**

**Current code:**
```html
<section class="py-24 md:py-32 px-6 md:px-8 bg-white">
```

**Understanding the spacing:**
- `py-24` = Vertical padding on small screens
- `md:py-32` = Vertical padding on medium+ screens
- `px-6` = Horizontal padding on small screens
- `md:px-8` = Horizontal padding on medium+ screens

**To add more vertical space:**
- Change `py-24` to `py-32` (or higher)
- Change `md:py-32` to `md:40`

**Example:**
```html
<section class="py-32 md:py-40 px-6 md:px-8 bg-white">
```

---

#### **Changing Text Alignment**

**Current code:**
```html
<h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-6">
    Powerful Features Built for You
</h2>
```

**To center text:**
- Add `text-center` to the class list

**Example:**
```html
<h2 class="text-4xl md:text-5xl font-bold tracking-tight mb-6 text-center">
    Powerful Features Built for You
</h2>
```

**To right-align text:**
- Add `text-right` to the class list

---

#### **Changing Card Layout**

**Current code:**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**Understanding grid:**
- `grid-cols-1` = 1 column on small screens
- `md:grid-cols-3` = 3 columns on medium+ screens
- `gap-8` = Space between cards

**To change to 2 columns:**
- Change `md:grid-cols-3` to `md:grid-cols-2`

**Example:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

**To add more space between cards:**
- Change `gap-8` to `gap-12` or `gap-16`

---

### Adding Custom Styling

If you need styling that Tailwind doesn't provide, you can add custom CSS in the `<style>` section.

**Location:** Lines 20-76

**Example - Making all buttons have rounded corners:**

1. Find the `<style>` section
2. Add your custom CSS at the end:

```css
/* Add this at the end of the <style> section */
button {
    border-radius: 10px;
}
```

**Example - Changing the default font size:**

```css
body {
    font-size: 16px;
}
```

---

## Fixing and Managing Links

Your landing page has many links that need to work correctly. Let's go through each one.

### Understanding Links

A link in HTML looks like this:
```html
<a href="https://example.com">Click here</a>
```

- `<a>` = Anchor tag (creates the link)
- `href` = The destination (where the link goes)
- Text between `>` and `</a>` = What users see and click

### Link Types on Your Page

There are three types of links on your landing page:

1. **Internal Links** - Links to sections on the same page (start with `#`)
2. **External Links** - Links to other websites (start with `http://` or `https://`)
3. **Email Links** - Links to send emails (start with `mailto:`)

---

### Navigation Menu Links (Header)

**Location:** Lines 93-98 (Desktop) and Lines 108-113 (Mobile)

**Current code:**
```html
<!-- Desktop Menu -->
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#testimonials" class="...">Testimonials</a>
<a href="#faq" class="...">FAQ</a>
```

**How these work:**
- `#features` = Takes users to the section with `id="features"`
- `#benefits` = Takes users to the section with `id="benefits"`
- And so on...

**To add a new menu link:**

1. Find the desktop menu (around line 93)
2. Add a new line before the closing `</div>`:

```html
<a href="#pricing" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">Pricing</a>
```

3. Do the same for the mobile menu (around line 108)

**Important:** Make sure you also add a section with `id="pricing"` somewhere on the page, or the link won't work!

---

### Header CTA Button

**Location:** Line 102 (Desktop) and Line 115 (Mobile)

**Current code:**
```html
<a href="https://www.upflexdigital.com/contact" class="gradient-btn px-8 py-3 rounded-lg text-white font-bold text-sm">
    Get Started
</a>
```

**To change the button link:**

1. Find `https://www.upflexdigital.com/contact`
2. Replace with your desired URL

**Examples:**
```html
<!-- Link to your contact form -->
<a href="https://yourcompany.com/contact" class="...">Get Started</a>

<!-- Link to sign up page -->
<a href="https://yourcompany.com/signup" class="...">Get Started</a>

<!-- Link to external service -->
<a href="https://app.yourcompany.com/start" class="...">Get Started</a>
```

---

### Hero Section Buttons

**Location:** Lines 172-180

**Current code:**
```html
<a href="https://www.upflexdigital.com/contact" class="gradient-btn px-8 py-4 rounded-lg text-white font-bold text-lg text-center hover:scale-105 transition-transform duration-300">
    Start Your Journey
</a>
<button class="px-8 py-4 rounded-lg border-2 border-[#5B4BFF] text-[#5B4BFF] font-bold text-lg hover:bg-[#EEF0FF] transition-all duration-300">
    Learn More
</button>
```

**To change the primary button link:**

1. Find the first link and replace the URL:

```html
<a href="https://yourcompany.com/contact" class="...">Start Your Journey</a>
```

**To make the "Learn More" button work:**

The "Learn More" button is currently just a button, not a link. To make it do something, you have two options:

**Option 1: Make it a link**
```html
<a href="https://yourcompany.com/learn-more" class="px-8 py-4 rounded-lg border-2 border-[#5B4BFF] text-[#5B4BFF] font-bold text-lg hover:bg-[#EEF0FF] transition-all duration-300">
    Learn More
</a>
```

**Option 2: Make it scroll to a section**
```html
<a href="#features" class="px-8 py-4 rounded-lg border-2 border-[#5B4BFF] text-[#5B4BFF] font-bold text-lg hover:bg-[#EEF0FF] transition-all duration-300">
    Learn More
</a>
```

---

### CTA Section Buttons

**Location:** Lines 344-351

**Current code:**
```html
<a href="https://www.upflexdigital.com/contact" class="px-10 py-4 rounded-lg bg-white text-[#5B4BFF] font-bold text-lg hover:scale-105 transition-transform duration-300 shadow-lg">
    Get Started Now
</a>
<button class="px-10 py-4 rounded-lg border-2 border-white text-white font-bold text-lg hover:bg-white hover:bg-opacity-10 transition-all duration-300">
    Schedule Demo
</button>
```

**To change the links:**

1. Update the first button URL:
```html
<a href="https://yourcompany.com/contact" class="...">Get Started Now</a>
```

2. Make the "Schedule Demo" button work (use one of the options from above)

---

### Footer Links

The footer contains many links organized in columns. Let's go through each section.

#### **Footer Product Links**

**Location:** Lines 617-624

**Current code:**
```html
<h4 class="text-lg font-bold mb-6">Product</h4>
<ul class="space-y-3">
    <li><a href="#features" class="...">Features</a></li>
    <li><a href="#benefits" class="...">Benefits</a></li>
    <li><a href="#" class="...">Pricing</a></li>
    <li><a href="#" class="...">Security</a></li>
</ul>
```

**To update these links:**

1. `#features` and `#benefits` already work (they go to sections on this page)
2. For `Pricing` and `Security`, replace `#` with actual URLs:

```html
<li><a href="https://yourcompany.com/pricing" class="...">Pricing</a></li>
<li><a href="https://yourcompany.com/security" class="...">Security</a></li>
```

---

#### **Footer Company Links**

**Location:** Lines 626-633

**Current code:**
```html
<h4 class="text-lg font-bold mb-6">Company</h4>
<ul class="space-y-3">
    <li><a href="#" class="...">About Us</a></li>
    <li><a href="blog.html" class="...">Blog</a></li>
    <li><a href="#" class="...">Careers</a></li>
    <li><a href="#" class="...">Contact</a></li>
</ul>
```

**To update these links:**

```html
<li><a href="https://yourcompany.com/about" class="...">About Us</a></li>
<li><a href="https://yourcompany.com/blog" class="...">Blog</a></li>
<li><a href="https://yourcompany.com/careers" class="...">Careers</a></li>
<li><a href="https://yourcompany.com/contact" class="...">Contact</a></li>
```

---

#### **Footer Legal Links**

**Location:** Lines 635-642

**Current code:**
```html
<h4 class="text-lg font-bold mb-6">Legal</h4>
<ul class="space-y-3">
    <li><a href="privacy.html" class="...">Privacy Policy</a></li>
    <li><a href="terms.html" class="...">Terms of Service</a></li>
    <li><a href="#" class="...">Cookie Policy</a></li>
    <li><a href="#" class="...">Compliance</a></li>
</ul>
```

**These are important!** See the next section for updating privacy and terms links.

---

#### **Footer Contact Email**

**Location:** Lines 649-655

**Current code:**
```html
<a href="mailto:info@upflexdigital.com" class="hover:text-[#00E5A8] transition-colors duration-300">info@upflexdigital.com</a>
```

**To change the email:**

1. Replace `info@upflexdigital.com` with your email (appears twice):

```html
<a href="mailto:support@yourcompany.com" class="...">support@yourcompany.com</a>
```

---

#### **Footer Bottom Links**

**Location:** Lines 679-685

**Current code:**
```html
<div class="flex gap-6">
    <a href="privacy.html" class="...">Privacy</a>
    <a href="terms.html" class="...">Terms</a>
    <a href="blog.html" class="...">Blog</a>
</div>
```

These links should match your actual pages. See the next section for updating privacy and terms.

---

### Social Media Links

**Location:** Lines 607-615

**Current code:**
```html
<a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-[#5B4BFF] transition-colors duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To add your social media links:**

Replace `#` with your actual social media URLs:

```html
<!-- Facebook -->
<a href="https://facebook.com/yourcompany" class="...">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/yourcompany" class="...">
    <i class="fab fa-twitter"></i>
</a>

<!-- LinkedIn -->
<a href="https://linkedin.com/company/yourcompany" class="...">
    <i class="fab fa-linkedin-in"></i>
</a>

<!-- GitHub -->
<a href="https://github.com/yourcompany" class="...">
    <i class="fab fa-github"></i>
</a>
```

---

## Adding Privacy and Terms Pages

Your landing page currently links to `privacy.html` and `terms.html`, but these files probably don't exist yet. Let's create them!

### Step 1: Create the Privacy Policy File

1. **Create a new file** in the same folder as your `index.html`
2. **Name it:** `privacy.html`
3. **Copy this code** into the file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - AI Research Assistant">
    <title>Privacy Policy - AI Research Assistant</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
        }
        
        header {
            background-color: #FFFFFF;
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 50;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-6 md:px-8 py-4 flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center gap-3">
                <span class="text-2xl font-bold" style="color: #5B4BFF;">AIResearch</span>
            </div>
            
            <!-- Back to Home Link -->
            <a href="index.html" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">
                ← Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 px-6 md:px-8 bg-white">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl md:text-6xl font-bold tracking-tight mb-8" style="color: #5B4BFF;">
                Privacy Policy
            </h1>
            
            <p class="text-lg text-gray-600 font-light mb-12">
                Last updated: January 2025
            </p>
            
            <div class="space-y-8 text-gray-700 leading-relaxed font-light">
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">1. Introduction</h2>
                    <p>
                        Welcome to AI Research Assistant ("we," "us," "our," or "Company"). We are committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">2. Information We Collect</h2>
                    <p class="mb-4">We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site or when you choose to participate in various activities related to the Site.</li>
                        <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the Site.</li>
                        <li>Data From Third Parties: Information received from third parties, including but not limited to marketing partners and social media platforms.</li>
                    </ul>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">3. Use of Your Information</h2>
                    <p class="mb-4">Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Email you regarding your account or order</li>
                        <li>Fulfill and manage purchases, orders, payments, and other transactions related to the Site</li>
                        <li>Generate a personal profile about you so that future visits to the Site will be personalized as possible</li>
                        <li>Increase the efficiency and operation of the Site</li>
                        <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                    </ul>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">4. Disclosure of Your Information</h2>
                    <p>
                        We may share information we have collected about you in certain situations:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4 mt-4">
                        <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information about you is necessary to comply with the law, enforce our Site policies, or protect ours or others' rights, property, and safety.</li>
                        <li><strong>Third-Party Service Providers:</strong> We may share your information with parties who perform services for us, including payment processing, data analysis, email delivery, hosting services, customer service, and marketing assistance.</li>
                        <li><strong>Business Transfers:</strong> We may share or transfer your information in connection with, or during negotiations of, any merger, sale of company assets, financing, or acquisition of all or a portion of our business to another company.</li>
                    </ul>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">5. Security of Your Information</h2>
                    <p>
                        We use administrative, technical, and physical security measures to protect your personal information. However, perfect security cannot be guaranteed. Your use of our Site and services is at your own risk.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">6. Contact Us</h2>
                    <p>
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:privacy@upflexdigital.com" class="text-[#5B4BFF] hover:text-[#00E5A8]">privacy@upflexdigital.com</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-8 px-6 md:px-8">
        <div class="max-w-7xl mx-auto text-center">
            <p class="text-gray-400 font-light">
                &copy; 2025 Upflex Digital. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Step 2: Create the Terms of Service File

1. **Create a new file** in the same folder as your `index.html`
2. **Name it:** `terms.html`
3. **Copy this code** into the file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - AI Research Assistant">
    <title>Terms of Service - AI Research Assistant</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Space Grotesk', sans-serif;
        }
        
        header {
            background-color: #FFFFFF;
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 50;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-6 md:px-8 py-4 flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center gap-3">
                <span class="text-2xl font-bold" style="color: #5B4BFF;">AIResearch</span>
            </div>
            
            <!-- Back to Home Link -->
            <a href="index.html" class="text-gray-700 hover:text-[#5B4BFF] transition-colors duration-300 font-medium">
                ← Back to Home
            </a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 md:py-32 px-6 md:px-8 bg-white">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl md:text-6xl font-bold tracking-tight mb-8" style="color: #5B4BFF;">
                Terms of Service
            </h1>
            
            <p class="text-lg text-gray-600 font-light mb-12">
                Last updated: January 2025
            </p>
            
            <div class="space-y-8 text-gray-700 leading-relaxed font-light">
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">1. Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">2. Use License</h2>
                    <p class="mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on AI Research Assistant's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                    </ul>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">3. Disclaimer</h2>
                    <p>
                        The materials on AI Research Assistant's website are provided on an 'as is' basis. AI Research Assistant makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">4. Limitations</h2>
                    <p>
                        In no event shall AI Research Assistant or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on AI Research Assistant's website, even if AI Research Assistant or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on AI Research Assistant's website could include technical, typographical, or photographic errors. AI Research Assistant does not warrant that any of the materials on its website are accurate, complete, or current. AI Research Assistant may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">6. Links</h2>
                    <p>
                        AI Research Assistant has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by AI Research Assistant of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">7. Modifications</h2>
                    <p>
                        AI Research Assistant may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>
                
                <section>
                    <h2 class="text-3xl font-bold mb-4" style="color: #5B4BFF;">9. Contact Information</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:legal@upflexdigital.com" class="text-[#5B4BFF] hover:text-[#00E5A8]">legal@upflexdigital.com</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-8 px-6 md:px-8">
        <div class="max-w-7xl mx-auto text-center">
            <p class="text-gray-400 font-light">
                &copy; 2025 Upflex Digital. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

---

### Step 3: Verify the Links Work

After creating these files, verify the links work:

1. **From your footer**, click on "Privacy Policy" or "Terms of Service"
2. **You should be taken** to the respective pages
3. **The "Back to Home" link** should take you back to your main page

**If links don't work:**

1. Make sure the files are saved as `privacy.html` and `terms.html` (exactly this spelling)
2. Make sure they're in the same folder as your `index.html`
3. Check that the links in your `index.html` match the filenames exactly

---

### Step 4: Customize Your Policy Pages

The privacy and terms pages I provided are templates. You should customize them:

**For Privacy Policy:**
- Replace contact email with your actual email
- Add any specific data practices your company uses
- Add information about cookies or tracking

**For Terms of Service:**
- Replace company name throughout
- Add any specific terms relevant to your service
- Add payment terms if applicable

---

## Color Customization

Your landing page uses a specific color scheme. Let's learn how to change it.

### Current Color Scheme

| Color | Hex Code | Usage |
|-------|----------|-------|
| Primary Purple | `#5B4BFF` | Headlines, primary buttons, icons |
| Accent Mint | `#00E5A8` | Accents, hover states, secondary highlights |
| Soft Lavender | `#EEF0FF` | Background sections |
| Gray Text | `#1F2937` | Main body text |
| Light Gray | `#6B7280` | Secondary text |

---

### How Colors Are Used in the Code

**In inline styles:**
```html
<h1 style="color: #5B4BFF;">AI Research Assistant</h1>
```

**In Tailwind classes:**
```html
<div class="text-[#5B4BFF]">Text</div>
<div class="bg-[#5B4BFF]">Background</div>
<div class="border-[#5B4BFF]">Border</div>
```

---

### Changing All Primary Colors (Purple)

To change all purple (`#5B4BFF`) to a different color:

1. **Open your `index.html` file**
2. **Use Find & Replace** (Ctrl+H or Cmd+H in most editors)
3. **Find:** `#5B4BFF`
4. **Replace with:** Your new color code
5. **Click "Replace All"**

**Example - Changing to blue:**
- Find: `#5B4BFF`
- Replace with: `#0066FF`

---

### Changing All Accent Colors (Mint)

To change all mint (`#00E5A8`) to a different color:

1. **Use Find & Replace** (Ctrl+H or Cmd+H)
2. **Find:** `#00E5A8`
3. **Replace with:** Your new color code
4. **Click "Replace All"**

**Example - Changing to gold:**
- Find: `#00E5A8`
- Replace with: `#FFD700`

---

### Changing Background Colors

**Soft Lavender background:**

Find: `#EEF0FF`
Replace with: Your new color

**Example:**
```html
<!-- Current -->
<section class="bg-soft-lavender">

<!-- After changing #EEF0FF to #F0F4FF -->
<section class="bg-soft-lavender">
```

---

### Creating a Custom Color Palette

If you want to use a completely different color scheme:

**Step 1: Choose your colors**
- Primary color (for headings and buttons)
- Accent color (for highlights and hover effects)
- Background color (for alternate sections)

**Step 2: Replace all instances**

| Original | Find | Replace With |
|----------|------|--------------|
| Primary Purple | `#5B4BFF` | Your primary color |
| Accent Mint | `#00E5A8` | Your accent color |
| Soft Lavender | `#EEF0FF` | Your background color |

---

### Color Recommendations

**Professional Blue Theme:**
- Primary: `#0066FF` (Blue)
- Accent: `#00D9FF` (Cyan)
- Background: `#F0F7FF` (Light Blue)

**Energetic Green Theme:**
- Primary: `#22C55E` (Green)
- Accent: `#F59E0B` (Amber)
- Background: `#F0FDF4` (Light Green)

**Modern Dark Purple Theme:**
- Primary: `#7C3AED` (Purple)
- Accent: `#EC4899` (Pink)
- Background: `#FAF5FF` (Light Purple)

---

## Responsive Design Best Practices

Your landing page automatically adapts to different screen sizes. Let's understand how and how to maintain this.

### Breakpoints (Screen Sizes)

Your page uses Tailwind's responsive breakpoints:

| Breakpoint | Screen Size | Class Prefix |
|-----------|-------------|--------------|
| Small | < 768px | (none) |
| Medium | ≥ 768px | `md:` |
| Large | ≥ 1024px | `lg:` |
| Extra Large | ≥ 1280px | `xl:` |

---

### How Responsive Classes Work

**Example:**
```html
<h1 class="text-5xl md:text-6xl lg:text-6xl">
    AI Research Assistant
</h1>
```

This means:
- On small screens (phones): `text-5xl` (large)
- On medium screens (tablets): `md:text-6xl` (extra large)
- On large screens (desktops): `lg:text-6xl` (extra large)

---

### Testing Responsive Design

**In Your Browser:**

1. **Open your landing page**
2. **Press F12** (or right-click → Inspect)
3. **Click the device icon** (top-left of developer tools)
4. **Select different devices** to test

**Common devices to test:**
- iPhone (375px)
- iPad (768px)
- Desktop (1920px)

---

### When Adding New Content

Always include responsive classes:

**Bad (only works on desktop):**
```html
<div class="text-4xl">This text is too big on phones!</div>
```

**Good (works on all screens):**
```html
<div class="text-2xl md:text-3xl lg:text-4xl">This text scales nicely!</div>
```

---

### Common Responsive Patterns on Your Page

**Grid Layout:**
```html
<!-- 1 column on small, 3 columns on medium+ -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**Flex Layout:**
```html
<!-- Column on small, row on medium+ -->
<div class="flex flex-col md:flex-row gap-8">
```

**Padding:**
```html
<!-- Less padding on small, more on large -->
<section class="px-6 md:px-8">
```

**Text Size:**
```html
<!-- Smaller on phones, larger on desktop -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```

---

### Maintaining Responsiveness

**When you modify the page:**

1. **Test on mobile** (using browser dev tools)
2. **Test on tablet** (using browser dev tools)
3. **Test on desktop** (normal viewing)
4. **Check that:**
   - Text is readable
   - Buttons are clickable
   - Images fit properly
   - No horizontal scrolling

---

## Troubleshooting Common Issues

### Issue 1: Links Not Working

**Problem:** Clicking a link does nothing or shows a 404 error.

**Solution:**

1. **Check the URL spelling** - URLs are case-sensitive
2. **For internal links** (starting with `#`), make sure a section exists with that ID:
   ```html
   <!-- Link -->
   <a href="#features">Features</a>
   
   <!-- Section must exist with matching ID -->
   <section id="features">...</section>
   ```
3. **For external links**, make sure the URL is complete:
   - Wrong: `upflexdigital.com`
   - Right: `https://upflexdigital.com`

---

### Issue 2: Text Not Changing

**Problem:** You edited text in the HTML but it's not showing up on the page.

**Solution:**

1. **Save the file** (Ctrl+S or Cmd+S)
2. **Hard refresh your browser** (Ctrl+Shift+R or Cmd+Shift+R)
3. **Check that you edited the right section**
4. **Make sure you didn't accidentally delete HTML tags**

---

### Issue 3: Styling Looks Wrong

**Problem:** Colors are off, spacing is weird, or layout is broken.

**Solution:**

1. **Check for typos in class names:**
   - Wrong: `text-gray-600` (missing hyphen)
   - Right: `text-gray-600`
2. **Make sure you didn't delete closing tags:**
   - Wrong: `<div class="...">Content</div` (missing `>`)
   - Right: `<div class="...">Content</div>`
3. **Verify color codes are correct:**
   - Wrong: `#5B4BFF0` (too many digits)
   - Right: `#5B4BFF`

---

### Issue 4: Mobile Menu Not Working

**Problem:** Mobile menu button doesn't open/close the menu.

**Solution:**

1. **Make sure JavaScript is enabled** in your browser
2. **Check that you didn't delete the JavaScript code** (at the bottom of the HTML)
3. **Test in a different browser** to rule out browser issues
4. **Check browser console for errors:**
   - Press F12
   - Click "Console" tab
   - Look for red error messages

---

### Issue 5: Page Layout Broken on Mobile

**Problem:** Content overlaps, text is too large, or layout is weird on phones.

**Solution:**

1. **Check responsive classes** are present:
   ```html
   <!-- Good -->
   <h1 class="text-2xl md:text-4xl">
   
   <!-- Bad (only one size) -->
   <h1 class="text-4xl">
   ```
2. **Test with browser dev tools** (F12 → device mode)
3. **Make sure you didn't add fixed widths** that prevent scaling

---

### Issue 6: Images Not Showing

**Problem:** Image placeholders or broken image icons appear.

**Solution:**

1. **Check the image URL** is correct
2. **Make sure the image file exists** in the correct location
3. **Use absolute URLs** for external images:
   - Wrong: `image.jpg`
   - Right: `https://example.com/image.jpg`

---

### Issue 7: Colors Not Changing

**Problem:** You changed a color code but it didn't update.

**Solution:**

1. **Make sure you changed ALL instances** of that color
2. **Use Find & Replace** to change all at once (Ctrl+H)
3. **Hard refresh the browser** (Ctrl+Shift+R)
4. **Check for typos in color codes:**
   - Wrong: `#5B4BF` (missing digit)
   - Right: `#5B4BFF`

---

### Issue 8: Footer Links Go to Wrong Pages

**Problem:** Footer links don't go where they should.

**Solution:**

1. **Check the href attribute:**
   ```html
   <!-- Check this is correct -->
   <a href="https://yourcompany.com/contact">Contact</a>
   ```
2. **For privacy/terms pages**, make sure files exist:
   - `privacy.html` in the same folder as `index.html`
   - `terms.html` in the same folder as `index.html`
3. **Use browser dev tools** to check what URL it's trying to visit

---

## Quick Reference: Common Tasks

### Updating Company Name
1. Find all instances of "Upflex Digital"
2. Replace with your company name
3. Find all instances of "AIResearch"
4. Replace with your product name

### Changing Button Links
1. Find `href="https://www.upflexdigital.com/contact"`
2. Replace with your URL
3. Test the link works

### Adding a New Section
1. Copy an existing section's HTML
2. Modify the content
3. Add an `id` attribute for linking
4. Add link to navigation menu

### Updating Social Media Links
1. Find social media links in footer (lines 607-615)
2. Replace `#` with your social media URLs
3. Test links work

### Changing Font Sizes
1. Change `text-lg` to `text-sm` (smaller) or `text-xl` (larger)
2. Use `md:text-xl` for medium screens
3. Use `lg:text-2xl` for large screens

---

## Getting Help

If you encounter issues:

1. **Check the HTML syntax** - Make sure all tags are properly closed
2. **Use browser dev tools** (F12) to see error messages
3. **Test in a different browser** to rule out browser issues
4. **Make a backup** before making major changes
5. **Validate your HTML** at [validator.w3.org](https://validator.w3.org)

---

## Best Practices

1. **Always backup** before making major changes
2. **Test on mobile** using browser dev tools
3. **Use Find & Replace** for bulk changes
4. **Keep a changelog** of what you've modified
5. **Test all links** after making changes
6. **Hard refresh** (Ctrl+Shift+R) when testing changes
7. **Keep file names consistent** (all lowercase, no spaces)
8. **Comment your changes** in the code for future reference

---

## Conclusion

You now have a comprehensive understanding of how to maintain and customize your AI Research Assistant landing page. Remember:

- **HTML** = Content (what appears)
- **CSS/Tailwind** = Styling (how it looks)
- **JavaScript** = Interactivity (what happens when you click)

Feel free to experiment, and don't hesitate to refer back to this guide when you need help!