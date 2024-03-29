#### Title: "Node.js and Build Tools Installation Guide with Optional OS Upgrades"

  <details>
  <summary>1. Get Debian/Ubuntu:</summary>
  
  1. [Install WSL Debian on Windows](https://github.com/brettjrea/Windows_WSL_Debian)
  
  2. [Install WSL Ubuntu on Windows](https://github.com/brettjrea/Windows_WSL_Ubuntu)
  
  3. [Install VSCode with Remote Pack on Windows](https://github.com/brettjrea/Windows_VSC_Remote_Pack)
  
  </details>

  <details>
  <summary>2. Optional OS upgrades:</summary>
  
  1. [Upgrade Debian Bullseye to Buster](https://github.com/brettjrea/Debian_Bullseye_Upgrade_Script)
  
  2. [Upgrade Ubuntu Focal to Jammy](https://github.com/brettjrea/Ubuntu_Jammy_Upgrade_Script)
  
  </details>
  
  <details>
  <summary>3. Node.js tools:</summary>  
  1. [Install NVM](https://github.com/brettjrea/Debian_Install_NVM) - Node Version Manager
  
  2. [Install NVS](https://github.com/brettjrea/Debian_Install_NVS) - Node Version Switcher (added 02/23 it is a cross-platform node based successor/replacement for NVM)
  
  </details>
  
  <details>     
  <summary>4. Build tools:</summary>       
  
  1. [Install common build tools.](https://github.com/brettjrea/Debian_Install_Common_Build_Tools)
  
  </details>
  
  <details>   
  <summary>5. Add a Backend:</summary> 
  
  1. [Install Strapi.io backend](https://github.com/brettjrea/Debian_Strapi_Backend_API)
  
  </details>
  
  <details>   
  <summary>6. Add a Frontend:</summary> 
  
  1. [Install Gatsby frontend](https://github.com/brettjrea/Debian_Gatsby_Frontend_Client)
  
  </details>
  
  <details>   
  <summary>7. Configure Process Manager:</summary> 
  
  1. [Configure PM2 Process Manager](https://github.com/brettjrea/Debian_Configure_PM2)
  
  </details>
  
  <details>   
  <summary>8. Add GitHub CLI:</summary> 
  
  1. [Install GitHub CLI](https://github.com/brettjrea/Debian_Install_GitHub_CLI)
  
  </details>
  
  
---
### GitHub CLI

This is a script to install GitHub CLI on Debian-based systems using the install-github-cli.sh script. To use the script, copy and paste the following commands into your terminal:

```
sudo apt upgrade -y && sudo apt update -y && sudo apt autoremove -y &&
sudo apt install wget -y &&
sudo apt-get install --reinstall ca-certificates -y &&
wget https://raw.githubusercontent.com/brettjrea/Debian_Install_GitHub_CLI/main/install-github-cli.sh &&
chmod +x install-github-cli.sh &&
./install-github-cli.sh &&
sudo apt autoremove -y &&
sudo apt clean -y
```
 
### Authentication and Configuration

gh auth login: Authenticate to GitHub with your credentials.

gh config set editor <editor>: Set your preferred text editor for Git commands.

gh config set prompt <style>: Customize the shell prompt for GitHub CLI.

### Repository Management

gh repo create <name> [--public|--private]: Create a new GitHub repository with the given name and visibility.

gh repo clone <repo> [-- <git-clone-args>]: Clone a GitHub repository locally with optional Git clone arguments.

gh repo view <repo>: View a GitHub repository in the browser.

gh repo fork <repo> [--clone|--remote-name=<name>]: Fork a GitHub repository to your account with optional cloning or custom remote name.

gh repo delete <repo> [--yes]: Delete a GitHub repository with optional confirmation.

### Pull Request Management

gh pr create: Create a new pull request in the current repository.

gh pr checkout <number>: Check out the branch for the given pull request number.

gh pr view <number>: View a pull request in the browser.

gh pr merge <number> [--merge-method=<merge-method>]: Merge a pull request with optional merge method.

### Issue Management

gh issue create: Create a new issue in the current repository.

gh issue list [--assignee=<login>|--label=<label>|--state=<state>|--author=<login>|--mention=<login>]: List issues in the current repository with optional filters.

gh issue view <number>: View an issue in the browser.

gh issue close <number>: Close an issue.

### Workflow Management

gh workflow list: List the workflows in the current repository.

gh workflow view <name>: View details of a workflow in the current repository.

gh workflow run <name> [--ref=<ref>]: Manually trigger a workflow in the current repository with optional ref.
 
---
This is not an exhaustive list of all available commands, but these are some of the most commonly used ones. You can get a full list of commands and their descriptions by running gh help.
