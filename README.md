# Understanding Memory Bank

## Memory Bank Structure

The extension creates and manages these core files in the memory-bank folder:

## Current File Structure

memory-bank/
├── projectbrief.md
├── productContext.md
├── systemPatterns.md
├── techContext.md

Integration: Works with other tools to enhance memory retention and workflow continuity

- projectbrief.md: Core project goals

- productContext.md: Problem and functionality 
- systemPatterns.md: Architecture and design patterns 
- techContext.md: Tech stack and constraints 

- activeContext.md: Current work focus 

- progress.md: Completed and pending tasks  

## Core Files (Required)

### projectbrief.md
- Foundation document that shapes all other files
- Created at project start if it doesn't exist
- Defines core requirements and goals
- Source of truth for project scope

### productContext.md
- Why this project exists
- Problems it solves
- How it should work
- User experience goals

### activeContext.md
- Current work focus
- Recent changes
- Next steps
- Active decisions and considerations

### systemPatterns.md
- System architecture
- Key technical decisions
- Design patterns in use
- Component relationships

### techContext.md
- Technologies used
- Development setup
- Technical constraints
- Dependencies

### progress.md
- What works
- What's left to build
- Current status
- Known issues

## Additional Context
Create additional files/folders within memory-bank/ when they help organize:
- Complex feature documentation
- Integration specifications
- API documentation
- Testing strategies
- Deployment procedures

## Using with Cursor AI

Once the MCP server is running, you can use AI Memory with Cursor in two ways:
- Direct interaction with Cursor AI: Cursor will automatically access the memory bank context when you chat with it.
- Using /memory commands: Type commands like /memory status in the Cursor chat to interact with your memory bank.

Available commands:
- /memory status: Check the status of the memory bank
- /memory list: List all memory bank files
- /memory read <filename>: Read a specific memory bank file

# Core Workflows
## Plan Mode
Start --> Read Memory Back --> File complete?  
If yes --> Verify context --> Develop Strategy --> Present Approach 
If no --> Create plan --> Document in Chat

## Act Mode
Start --> Check memory back --> Update docuemntation --> Update .cursorrule if needed --> Execute Task --> Document Changes

## Documentation Updates

Memory Bank updates occur when:
- Discovering new project patterns
- After implementing significant changes
- When user requests with update memory bank (MUST review ALL files)
- When context needs clarification

Update Process --> Review all files --> Document Current State --> Clarify Next Steps --> Update .cursorrule 

## Dashboard

Run the AI Memory: Open Dashboard command to open a dashboard interface for viewing and managing your memory bank files.

## Troubleshooting MCP Connections

If you experience issues connecting to the MCP server from Cursor:

- Check server status: Ensure the server is running by visiting http://localhost:7331/health in your browser. You should see {"status":"ok ok"}.

- Port conflicts: If port 7331 is in use, the extension will try port 7332. Check the extension output to see which port was actually used.

- Manual config update: Run the AI Memory: Update Cursor MCP Config command to manually update the Cursor configuration.

- Connection issues: If you see "Client closed" errors:
    - Make sure no firewalls are blocking localhost connections
    - Try restarting the MCP server with AI Memory: Start MCP again
    - Check the extension's output panel for error messages

# How to use the memory bank

B1: Initialize the memory bank

B2: How to run this project

B2.1: Install dependencies
$ pnpm install

B2.2: Run the project
$ pnpm dev

B2.3: Build the project
$ pnpm build