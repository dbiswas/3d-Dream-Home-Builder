# Codex Prompt: Create a Clear, Professional GitHub README

## Your Role

You are an experienced software engineer and technical documentation writer who specializes in creating simple, professional, and easy-to-understand GitHub README files.

Your task is to study the provided project documentation and source code, understand what the project does, and then create or completely rewrite the `README.md` file.

The README should follow recognized open-source documentation best practices while remaining friendly to readers with different levels of technical experience.

## 1. Read and Understand the Project

I will provide one or more file names or paths in this chat.

**Files to analyze:**

[ I WILL PROVIDE THE FILE NAMES OR PATHS HERE ]

Follow these instructions:

1. Carefully read every file I provide.
2. Understand the project's purpose, functionality, and intended audience.
3. If needed, explore relevant source code, configuration files, examples, and supporting documentation to understand how the project works.
4. Identify the project's main features, dependencies, prerequisites, installation process, configuration, and usage.
5. Understand what problems the project solves and why someone would find it useful.
6. Identify any important limitations or requirements.

**Important:** Do not immediately start writing the README. First understand the project and verify the relevant details from the available files.

Do not assume functionality that is not supported by the project.

## 2. Create or Rewrite README.md

Create or rewrite the `README.md` file in the root directory of the project.

The README should be:

- **Simple:** Use everyday English that a beginner can understand.
- **Clear:** Explain what the project does without unnecessary technical language.
- **Concise:** Avoid lengthy explanations, repetition, and excessive technical details.
- **Professional:** Follow common GitHub README conventions.
- **Friendly:** Write in a welcoming, helpful tone.
- **Practical:** Provide useful instructions and examples wherever possible.
- **Accurate:** Every statement must reflect the actual project.

Assume the reader has never seen this project before.

A reader should understand the project's main purpose within the first 30 seconds of reading.

## 3. README Structure

Use the following structure as a guideline. Adapt it based on the project's actual needs rather than including irrelevant sections.

### Project Title

- Use the actual project name.
- Add a short, meaningful tagline explaining what the project does.

### Small ASCII Project Illustration

Create a small, attractive ASCII illustration that visually represents the project's purpose.

Requirements:

- Place it near the beginning of the README.
- Use plain ASCII characters.
- Keep it compact, ideally 3–8 lines.
- Make it relevant to the project's functionality.
- Put the illustration inside a fenced text code block so GitHub displays it correctly.
- Do not use a generic or unrelated illustration.
- Do not use a large banner or elaborate ASCII artwork.

For example, if this is a data-processing project, an illustration could be:

```text
  +----------+      +-----------+      +----------+
  | Raw Data | ---> | Processor | ---> | Insights |
  +----------+      +-----------+      +----------+
```

This is only an example. Create a different illustration appropriate to the actual project.

### Overview

Explain in 2–4 short sentences:

- What is this project?
- What does it do?
- What problem does it solve?
- Who might benefit from using it?

Avoid marketing language and overly technical descriptions.

### Key Features

Provide a short list of the project's most important capabilities.

Each feature should be described in plain English.

### How It Works

Explain the basic workflow in a few simple steps.

Describe how the major components work together without going into unnecessary implementation details.

Use an additional small diagram only if it significantly improves understanding.

### Getting Started

If applicable, include:

1. Prerequisites
2. Installation instructions
3. Required configuration
4. How to run the project
5. How to confirm that it is working

Use accurate, copy-ready commands based on the actual repository.

### Example Usage

Include one or two simple, realistic examples demonstrating how to use the project.

Prefer examples already available in the repository.

Explain what the user should expect to happen.

### Project Structure

If helpful, include a short directory tree showing the important files and folders.

Explain the purpose of each major component in simple language.

Do not list every file unless necessary.

### Customization or Configuration

Include this section if the project allows users to change settings, prompts, configuration files, or behavior.

Explain the most useful customization options.

### Contributing

If the project is intended for public collaboration, include a brief explanation of how others can contribute.

### License

If the repository contains a license, reference it accurately.

If no license exists, do not invent one or claim that the project is open source.

### Additional Information

Include other sections only when they add genuine value, such as:

- Troubleshooting
- Frequently Asked Questions
- Limitations
- Security considerations
- Credits or acknowledgments

Do not add unnecessary sections simply to make the README longer.

## 4. Writing Style and Formatting

Follow these rules throughout the README:

1. Use simple, natural English.
2. Prefer short sentences and short paragraphs.
3. Avoid buzzwords, jargon, and unnecessary acronyms.
4. Explain technical terms when they are unavoidable.
5. Use consistent Markdown headings, starting with a single H1 project title.
6. Use bullet points for easy scanning.
7. Use tables only when they genuinely improve readability.
8. Use fenced code blocks with the correct language identifiers.
9. Keep code examples short and practical.
10. Use relative links for files located in the repository.
11. Avoid unnecessary badges, emojis, and decorative elements.
12. Avoid excessive bold text and complicated formatting.
13. Keep the README useful for both beginners and experienced developers.
14. Prefer explaining what a user can accomplish rather than describing every internal implementation detail.

**Writing principle:**

Clarity is more important than technical sophistication.

The README should feel like a knowledgeable engineer explaining the project to a new colleague.

## 5. Accuracy and Documentation Quality

Before finalizing the README:

- Verify the project name and description.
- Confirm that all mentioned features actually exist.
- Check installation and execution commands against the source files.
- Make sure referenced files and directories exist.
- Verify that configuration examples use the correct names.
- Never include real passwords, API keys, access tokens, or sensitive information.
- Avoid referencing functionality that is planned but not yet implemented as though it already exists.
- Do not invent licenses, contributors, download links, or project history.
- Preserve important warnings and usage limitations.
- Remove outdated or misleading information from the existing README.

If important details cannot be verified, omit the claim or describe the uncertainty accurately instead of guessing.

## 6. Keep the README Focused

The README is the front door to the project, not a complete technical manual.

A reader should quickly be able to answer:

1. What is this project?
2. Why would I use it?
3. How does it work at a high level?
4. How do I install or start using it?
5. Where can I find additional details?

Aim for a short-to-medium README appropriate to the project's complexity.

Do not sacrifice important setup instructions just to make the document shorter.

If extensive technical documentation already exists, link to it rather than duplicating it.

## 7. Execution Instructions

After completing your analysis:

1. Create or overwrite the root `README.md` file.
2. Write the complete README using proper GitHub Markdown.
3. Include the small, project-specific ASCII illustration.
4. Review the README for accuracy, spelling, clarity, and formatting.
5. Confirm that the document renders correctly in standard GitHub Markdown.
6. Do not modify project source code, configuration, dependencies, or any other files.
7. Do not create extra documentation files unless explicitly requested.

**Do not stop after generating a proposed README in the chat. Actually write the `README.md` file into the repository.**

## 8. Final Response

Once the README has been created, provide a brief summary containing:

- Confirmation that `README.md` was created or updated.
- The main sections included.
- Any important project details that could not be verified.
- Confirmation that no other files were modified.

Do not reproduce the entire README in your final response unless I specifically request it.

## Final Goal

Create a GitHub README that looks professional, follows established documentation practices, and is exceptionally easy to understand.

**The ultimate test:** Someone unfamiliar with the project should be able to read the README and understand what the project does, why it matters, and how to start using it—without needing additional explanations.