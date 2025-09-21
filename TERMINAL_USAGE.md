# Python Web Terminal - Usage Guide

## 🚀 Features

### Standard File & Directory Operations
- `ls [path]` - List directory contents
- `cd <dir>` - Change directory
- `pwd` - Print current directory  
- `mkdir <name>` - Create directory
- `rm <file>` - Remove file/directory
- `rmdir <dir>` - Remove empty directory
- `touch <file>` - Create empty file
- `cat <file>` - Display file contents
- `cp <src> <dst>` - Copy file
- `mv <src> <dst>` - Move/rename file

### System Information & Monitoring
- `sysinfo` - Display comprehensive system information
- `ps` - List running processes
- `top` - Show top processes
- `kill <pid>` - Kill process by ID
- `df` - Show disk usage
- `du [path]` - Show directory size
- `ifconfig` - Network configuration
- `ping <host>` - Ping a host

### Utilities & Tools
- `history` - Show command history
- `help` - List all available commands
- `clear` - Clear terminal screen
- `whoami` - Show current user
- `date` - Show current date/time
- `uptime` - Show system uptime
- `echo <text>` - Display text
- `find <pattern>` - Find files
- `grep <pattern> <file>` - Search in files
- `wget <url>` - Download from URL
- `curl <url>` - Make HTTP request
- `tar <options>` - Archive operations
- `chmod <perm> <file>` - Change permissions

### 🤖 AI-Powered Natural Language Commands

Instead of memorizing commands, use natural language:

**File Operations:**
- "create a folder called test"
- "make a new file named config.txt"
- "delete the file readme.txt"
- "copy main.py to backup.py"
- "move documents to archive folder"
- "show me the contents of config.txt"

**Navigation:**
- "go to the home directory"
- "navigate to the documents folder"
- "go back one level"
- "what directory am I in?"

**System Information:**
- "show me system information"
- "what processes are running?"
- "check disk usage"
- "display command history"

**Complex Operations:**
- "create a folder called projects and move main.py into it"
- "find all files containing error"

### ⌨️ Keyboard Shortcuts

- **Enter** - Execute command
- **↑/↓ Arrows** - Navigate command history
- **Tab** - Auto-complete commands
- **Click anywhere** - Focus terminal input

### 🎨 Terminal Features

- **Real-time auto-completion** - Start typing and get suggestions
- **Command history** - Access previous commands with arrow keys
- **Syntax highlighting** - Different colors for different output types
- **Responsive design** - Works on desktop and mobile
- **Matrix-style theme** - Classic terminal aesthetics with modern touches

## 🚀 Deployment Instructions

### Option 1: Deploy on Lovable (Recommended)
1. Open your [Lovable Project](https://lovable.dev/projects/43b6455b-cfaf-4844-ac3b-ba68d3b522b9)
2. Click "Share" → "Publish"
3. Your terminal will be live at the provided URL

### Option 2: Deploy to Vercel
1. Push your code to GitHub
2. Connect your repository to [Vercel](https://vercel.com)
3. Deploy with one click

### Option 3: Deploy to Netlify
1. Drag and drop your `dist` folder to [Netlify](https://netlify.com)
2. Or connect your GitHub repository for continuous deployment

### Option 4: Local Development
```bash
# Clone the repository
git clone <your-repo-url>
cd python-web-terminal

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 🔧 Technical Architecture

### Frontend Stack
- **React 18** - Modern UI framework
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **Vite** - Fast build tool

### Core Modules
- **Terminal.tsx** - Main terminal interface with keyboard handling
- **commandProcessor.ts** - Handles all command execution
- **systemInfo.ts** - Simulates system monitoring (CPU, memory, disk)
- **aiCommandInterpreter.ts** - Natural language processing

### Design System
- **Matrix Green Theme** - Classic terminal aesthetics
- **JetBrains Mono Font** - Professional monospace typography
- **Responsive Layout** - Works on all screen sizes
- **Terminal Glow Effects** - Subtle lighting for authenticity

## 📁 File System Simulation

The terminal includes a simulated file system with:
- `/home/user/` - User home directory
- `/home/user/documents/` - Sample documents folder
- `/home/user/downloads/` - Downloads folder  
- `/home/user/projects/` - Projects folder with sample Python file
- System directories: `/bin`, `/etc`, `/var`

## 🎯 Use Cases

- **Learning Tool** - Practice Linux/Unix commands safely
- **Development Environment** - Simulate server interactions
- **Educational Demo** - Teach command line concepts
- **Portfolio Project** - Showcase terminal skills
- **Web Integration** - Embed terminal functionality in web apps

## 🛠️ Customization

### Adding New Commands
Edit `src/utils/commandProcessor.ts`:
```typescript
case 'mycommand':
  return this.myCustomCommand(args, currentDir);
```

### Adding Natural Language Patterns
Edit `src/utils/aiCommandInterpreter.ts`:
```typescript
{
  patterns: [/your regex pattern here/i],
  command: 'your command template'
}
```

### Styling Changes
Modify `src/index.css` for colors and themes:
```css
--terminal-success: 120 100% 75%; /* Green color */
--terminal-error: 0 84% 60%;     /* Red color */
```

## 📝 Notes

- All file operations are simulated (no real file system access)
- System information is randomly generated for demonstration
- Perfect for learning, demos, and web integration
- No backend required - runs entirely in the browser
- Fully responsive and mobile-friendly

## 🆘 Support

Type `help` in the terminal for a complete command reference, or try natural language commands like "show me help" or "what commands are available?"

---

**Built with ❤️ using React, TypeScript, and Tailwind CSS**