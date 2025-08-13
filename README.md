# Cross-platform developer setup

  ## Chezmoi – Manage Your Dotfiles Securely and Effortlessly 
  1. What is Chezmoi?
      - Chezmoi is a cross-platform command-line tool that helps you manage your personal configuration files (“dotfiles”) across multiple machines. It ensures consistency, security, and ease of updates.
  3. Key Features:    
      - Cross-platform: Works on Linux, macOS, and Windows.
      - Version control friendly: Integrates seamlessly with Git.
      - Encryption support: Securely store sensitive data (like API keys) using GPG, age, or other encryption tools.
      - Templating: Use variables and templates to adapt configs to different machines.
      - Idempotency: Running chezmoi apply brings any machine into the desired state without overwriting local changes unexpectedly.
  
  4. How it Works:
      - Initialize chezmoi in your home directory.
      - Add your dotfiles to chezmoi’s source state (chezmoi add ~/.bashrc).
      - Commit the source state to Git (optionally encrypting secrets).
      - Apply on any machine to replicate your setup (chezmoi apply).
      
  5. Benefits:
      - Consistency across all devices.
      - Safer than just copying files—secrets stay encrypted.
      - Automation reduces setup time for new machines.
      
  6. How i use this:
      
      I keep my .zshrc, .gitconfig, and personal scripts in chezmoi, store them in a private Git repo, and with one command, I can set up a brand-new laptop exactly like my main workstation.

  ## Mise – The Front-end for Your Dev Environment
  
  1. What Is Mise?
     - Mise is a cross-platform command-line tool version manager that elegantly replaces tools like asdf, nvm, pyenv, rbenv, and more. It also handles environment variable sets and task execution.

  2. Core Pillars:
      - Dev Tools Management
         - Handles installation and switching of language runtimes and tools—Node.js, Python, Ruby, Go, Terraform, and many others. It automatically switches versions based on mise.toml in your project or parent directories.
    
      - Environment Handling
        - Manages environment variable sets per project directory, serving as a modern and streamlined alternative to tools like direnv.
    
      - Task Running Capability
        - Enables structured task execution with features similar to make or npm scripts—context-aware and integrated into the mise ecosystem.

  3. Use Case Summary
        
      - In my dev work, I use mise to define my toolchain per project. One command sets up Node, Python, and environment variables automatically. No more manual installs or context-switching headaches.
      
