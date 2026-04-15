Chapter 6: Process Management (Linux)

🧠 What is a Process?

A process is simply a program that is currently running in the system.

Each process has:

PID (Process ID) → Unique identifier

Priority (Nice value) → Determines execution importance

State → Running, sleeping, stopped, etc.

🔍 Viewing Processes

🔹 ps – Show Processes

ps

ps aux

Explanation:

Displays running processes

ps aux shows detailed info (user, CPU, memory, PID)

🔹 Filter Specific Process

ps aux | grep firefox

Explanation:

Searches for a specific process by name

📊 Monitoring Processes

🔹 top – Real-Time Monitoring

top

Explanation:

Displays live system performance

Shows CPU, memory usage, and active processes

Useful Keys:

q → Quit

h → Help

k → Kill a process

⚡ Process Priority

🔹 nice – Start with Priority

nice -n -10 program

nice -n 10 program

Explanation:

Sets priority when starting a process

Range: -20 (highest) → +19 (lowest)

🔹 renice – Change Running Process Priority

renice 10 1234

Explanation:

Changes priority of an existing process using PID

❌ Stopping Processes

🔹 kill – Stop by PID

kill 1234

kill -9 1234

Explanation:

Terminates a process using PID

Common Signals:

-15 → Normal termination (default)

-9 → Force kill

🔹 killall – Stop by Name

killall firefox

killall -9 chrome

Explanation:

Kills all processes with a given name

🔄 Background & Foreground Processes

🔹 Run in Background

leafpad file.txt &

Explanation:

Runs process in background

Terminal remains usable

🔹 bg – Resume in Background
bg

Explanation:

Sends a stopped process to background

🔹 fg – Bring to Foreground

fg

Explanation:

Brings background process to foreground

⏰ Scheduling Tasks

🔹 at – Run Once in Future

at 7:20am

at> /root/script.sh

Explanation:

Schedules a one-time task

Examples:
at now + 20 minutes

at tomorrow

🧾 Quick Revision Table
Command	            Purpose
ps	                Show processes
top	                Live monitoring
nice	              Set priority
renice	            Change priority
kill	              Stop process (PID)
killall	            Stop process (name)
&  	                Run in background
bg	                Background process
fg	                Foreground process
at	                Schedule task

💡 Pro Tip

Understanding process management is very important in cybersecurity & system administration because:

-Helps detect malicious processes

-Allows control over system performance

-Useful in penetration testing environments like Kali Linux
