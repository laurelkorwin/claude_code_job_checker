# Claude Code Job Checker
This repo provides some custom slash commands for Claude Code that will help a user set career goals and search a predefined list of career pages for jobs that meet those goals.

Running the custom /set_career_goals command will prompt Claude to guide the user to download their LinkedIn profile / resume, and ask the user about desired roles, location and salary. All this information will be saved in a custom career profile file.

Running the custom /check_jobs command will prompt Claude to go through a list of company career pages (defined in `company_websites.md`) to look for open jobs matching the user's profile. Jobs will be saved in company specific files in the `jobs` folder.

# To run (highest level instructions, intended for general users, on Macs)
1. **Open a terminal window**
   - You can do this by pressing ⌘ + space and typing "terminal" then hitting enter
2. **Download the code here to your computer**
   - In that terminal window, copy this: `git clone https://github.com/laurelkorwin/claude_code_job_checker.git` and hit enter
3. **Install Claude Code**
   - In your terminal window, copy this: `brew install anthropics/claude/claude-code` and hit enter
   - If that doesn't work, visit the official site [here](https://www.anthropic.com/claude-code) and follow the instructions (these might be trickier, you can use Claude in browser for help)
4. **Login with Claude in the terminal**
   - In your terminal window, type `claude auth login` and hit enter. Follow the prompts in your browser to authenticate with claude
5. **Make sure you're in the directory (read: folder) with the code you downloaded**
   - Assuming you're in the same terminal you used to clone, you should be able to type `cd claude_code_job_checker`
   - If you run into any trouble with this, go to Claude in the browser and say "I am in a terminal window, trying to cd into the claude_code_job_checker directory on my Mac. Please guide me through troubleshooting how to do so."
6. **Add the Playwright MCP**
   - In your terminal window, type `claude mcp add playwright npx @playwright/mcp@latest` and hit enter
   - Note: this adds a tool that Claude Code needs to be able to reliably "see" the things you want it to see on the jobs websites. It means it will be able to open websites on its own, so don't be alarmed if browser sessions pop up! They should auto-close.
7. **Fire up Claude Code**
   - In your terminal window, just type `claude` and hit enter
8. **Use the custom commands!**
   - First, type `/set_career_goals` and have Claude interview / guide you through the process to create your career profile
   - Add whatever websites you want Claude to check to the `company_websites.md` folder (formatting examples given)
   - Next, run the `/check_jobs` command whenever you want Claude to check your website list!
  
# Some notes & words to the wise
**Permissions**
You will notice at first that Claude Code will pause and ask you for your permissions to do things like use certain tools, write to files, etc. You can hit enter to allow it to do so once, or the down arror & enter to allow that particular action all the time, or two down errors & enter to tell it to do something different. 

The "easiest" thing from a user perspective is to let it do everything w/o permissions, but this means you give it leeway to make mistakes and maybe do stuff you don't want -- so try running things a few times to get a sense for what it's asking and whether you feel comfortable with it. Personally, I "allow all" on a project by project and task by task basis -- there are things I like to look at all the time, and things I don't much care about.

**Tweaks, bugs, changes**
The "logic" for the two custom commands are in plain English, so if you notice Claude doing something weird, you can edit the text or tweak the steps as you like!

You could also totally add new commands if you want (for example, to "tweak" your resume to a particular job listing) -- just add a new .md file with instructions in the `commands` folder.


# Credit where credit is due!
Inspired by [this repo](https://github.com/WomenDefiningAI/claudecode-writer/tree/main) from WomenDefiningAI for the custom slash commands.
