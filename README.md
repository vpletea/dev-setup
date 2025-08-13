# dev-setup

  ## Chezmoi – Manage Your Dotfiles Securely and Effortlessly 
  1. What is Chezmoi? Chezmoi is a cross-platform command-line tool that helps you manage your personal configuration files (“dotfiles”) across multiple machines. It ensures consistency, security, and ease of updates.
  2. Key Features
      
      Cross-platform: Works on Linux, macOS, and Windows.
      
      Version control friendly: Integrates seamlessly with Git.
      
      Encryption support: Securely store sensitive data (like API keys) using GPG, age, or other encryption tools.
      
      Templating: Use variables and templates to adapt configs to different machines.
      
      Idempotent apply: Running chezmoi apply brings any machine into the desired state without overwriting local changes unexpectedly.
      
  3. How it Works
      
      Initialize chezmoi in your home directory.
      
      Add your dotfiles to chezmoi’s source state (chezmoi add ~/.bashrc).
      
      Commit the source state to Git (optionally encrypting secrets).
      
      Apply on any machine to replicate your setup (chezmoi apply).
      
  4. Benefits
      
      Consistency across all devices.
      
      Safer than just copying files—secrets stay encrypted.
      
      Automation reduces setup time for new machines.
      
  5. Example Use Case
      
      “I keep my .zshrc, .gitconfig, and personal scripts in chezmoi, store them in a private Git repo, and with one command, I can set up a brand-new laptop exactly like my main workstation.”

  ## Mise – The Front-end for Your Dev Environment
  

1. What Is Mise?

Mise is a polyglot tool version manager that elegantly replaces tools like asdf, nvm, pyenv, rbenv, and more. It also handles environment variable sets and task execution, positioning itself as a unified interface for managing your entire dev setup.
mise.jdx.dev
2. Core Pillars

```
Dev Tools Management
Handles installation and switching of language runtimes and tools—Node.js, Python, Ruby, Go, Terraform, and many others. It automatically switches versions based on mise.toml in your project or parent directories.
mise.jdx.dev+1

Environment Handling
Manages environment variable sets per project directory, serving as a modern and streamlined alternative to tools like direnv.
mise.jdx.dev

Task Running Capability
Enables structured task execution with features similar to make or npm scripts—context-aware and integrated into the mise ecosystem.
mise.jdx.dev

```

1. Workflow Overview
    
    Install & activate mise, using one of the supported methods:
    
    ```
     curl <https://mise.run> | sh
    
     Homebrew, npm, Scoop, winget, apt/yum, Docker, or compiling from source
     mise.jdx.dev
    
    ```
    
    Set tool versions using mise use, which installs and activates the tool:
    
    mise use node@22
    
    This adds the tool to your mise.toml, making it “active.”
    mise.jdx.dev+1
    
    Run tools/tasks in the proper context:
    
    ```
     mise exec (alias: mise x) to run a command with the specified tool versions and env
    
     mise run to launch tasks defined in your config files
     mise.jdx.dev+1
    
    ```
    
    Configuration Hierarchy:
    
    ```
     Global: ~/.config/mise/config.toml
    
     Project-level: mise.toml in current and parent directories
    
     Local (private): mise.local.toml for settings you don’t push to version control
     mise.jdx.dev+1
    
    ```
    
    Backends & Plugins:
    
    ```
     Leverages modern backends like aqua, ubi (Universal Binary Installer), npm, cargo, etc., for fast and secure installations.
     mise.jdx.dev
    
     Plugins are still supported but discouraged unless necessary. If possible, target tools for registry inclusion via backend systems instead.
     mise.jdx.dev
    
    ```
    
2. Benefits at a Glance
Feature	Advantage
Unified Tooling	No need for multiple version managers—everything in one tool
Speed & UX	Faster than asdf, designed for simplicity and clarity
mise.jdx.dev
Context-Aware	Auto-switching based on project directory context
Task & Env Integration	Replace make and direnv—simplifies running tasks and managing envs
Flexible Configuration	Layered configs (global → project → local) for intelligent overrides
3. Use Case Summary
    
    “In my dev work, I use mise to define my toolchain per project. One command sets up Node, Python, and environment variables automatically. No more manual installs or context-switching headaches.”
  
