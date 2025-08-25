# Knowledge Base Link Addition Instructions for AI

When a user requests to add a link to the README with a command like:
```
add this link to the readme [URL]
```

Follow these steps to process the request:

## 1. Parse the User's Request

Identify the components in the user's request:
- The URL (required)
- Custom description (optional, in quotes after the URL)
- Custom section (optional, after "to" keyword and in quotes)

## 2. Extract Link Information

For GitHub repositories:
- Extract organization/repo-name from the URL (e.g., "HKUDS/DeepCode" from "https://github.com/HKUDS/DeepCode")
- Use this as the link text in the format: `[organization/repo-name]`

For websites/blogs:
- Extract the domain or resource name from the URL
- Use a capitalized version as the link text: `[Resource Name]`

## 3. Generate Description (if not provided)

If the user didn't provide a custom description:
- For GitHub repos: Visit the repository to understand its purpose
- For websites: Analyze the content of the page
- Create a concise (3-7 words) description that captures the essence of the resource
- Focus on what the resource does or provides, not just its name

## 4. Determine Appropriate Section (if not provided)

If the user didn't specify a section:
- Analyze the URL content and description
- Match the content's topic to the most relevant section from the list below
- For GitHub repos, consider the repository's purpose, tags, and description
- For websites, consider the site's content focus and domain

## 5. Handle Non-Existent Sections

If the specified or determined section doesn't exist in the README:

1. First, check if there's a similar section with slightly different wording
   - If found, use that section instead

2. If no similar section exists, determine the appropriate main category:
   - Learning Resources
   - Engineering Blogs
   - GitHub Repositories
   - Documentation & Websites

3. Add the new section under the appropriate main category:
   - Place it in alphabetical order among other subsections
   - Use the "### New Section Name" format (with 3 hashtags)
   - Add a blank line after the section header
   - Then add the new link

4. Inform the user that a new section was created

## 6. Format and Add the Link

Format the link according to the standard pattern:
```
- [link_text](URL) - Description
```

Then:
1. Read the current README.md file
2. Locate the specified section (or the determined section)
3. Add the new link in alphabetical order by organization/resource name
4. Ensure proper formatting and alignment with other links in the section

## 7. Confirm Addition

After adding the link, confirm to the user:
- The link that was added
- The section it was added to (mention if it's a newly created section)
- The description that was used (especially if auto-generated)

## Request Variations

### Simple Format (determine everything automatically)
```
add this link to the readme https://github.com/HKUDS/DeepCode
```

### With Custom Description
```
add this link to the readme https://github.com/HKUDS/DeepCode "Custom description here"
```

### With Custom Section
```
add this link to the readme https://github.com/HKUDS/DeepCode to "Code Generation & AI Coding"
```

### With Both Custom Description and Section
```
add this link to the readme https://github.com/HKUDS/DeepCode "Custom description here" to "Code Generation & AI Coding"
```

## Available Sections

### Learning Resources
- AI & Machine Learning
- Prompt Engineering & LLMs
- System Design & Architecture
- Databases & Data Engineering
- Programming & Development
- Events & Conferences
- Miscellaneous

### Engineering Blogs
- Major Tech Companies
- Social & Communication Platforms
- Video & Entertainment
- E-commerce & Marketplace
- Travel & Hospitality
- Food Delivery
- Developer Tools & Infrastructure
- Fintech & Payments
- Other Companies

### GitHub Repositories
- AI Agents & Frameworks
- LLM Tools & Applications
- RAG & Knowledge Management
- Code Generation & AI Coding
- MCP (Model Context Protocol)
- Data & Analytics
- AI Research & Learning
- Algorithms & Computer Science
- Finance & Trading
- Media Generation
- Developer Tools
- Workflow & Automation
- Research & Information
- Specialized Tools
- Browser & Web Tools
- Infrastructure & Performance
- Miscellaneous Projects

### Documentation & Websites
- AI Platforms & Tools
- Development Tools
- Research & Learning
- Data & Analytics
- Development Services
- Specialized Tools