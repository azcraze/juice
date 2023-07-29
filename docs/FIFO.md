# FIFO Help

Simple Scheduling Cog<br/><br/>Named after the simplest scheduling algorithm: First In First Out

# fifoclear
 - Usage: `?fifoclear `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Debug command to clear all current fifo data

# fifo
 - Usage: `?fifo `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Base command for handling scheduling of tasks

## fifo wakeup
 - Usage: `?fifo wakeup `

Debug command to fix missed executions.<br/><br/>If you see a negative "Next run time" when adding a trigger, this may help resolve it.<br/>Check the logs when using this command.

## fifo addtrigger
 - Usage: `?fifo addtrigger `
 - Aliases: `trigger`

Add a new trigger for a task from the current server.

### fifo addtrigger cron
 - Usage: `?fifo addtrigger cron <task_name> [optional_tz=None] <cron_str> `

Add a cron "time of day" trigger to the specified task<br/><br/>See https://crontab.guru/ for help generating the cron_str

### fifo addtrigger date
 - Usage: `?fifo addtrigger date <task_name> <datetime_str> `

Add a "run once" datetime trigger to the specified task

### fifo addtrigger interval
 - Usage: `?fifo addtrigger interval <task_name> <interval_str> `

Add an interval trigger to the specified task

### fifo addtrigger relative
 - Usage: `?fifo addtrigger relative <task_name> <time_from_now> `

Add a "run once" trigger at a time relative from now to the specified task

## fifo set
 - Usage: `?fifo set <task_name> <author_or_channel> `

Sets a different author or in a different channel for execution of a task.

## fifo resume
 - Usage: `?fifo resume [task_name=None] `

Provide a task name to resume execution of a task.<br/><br/>Otherwise resumes execution of all tasks on all servers<br/>If the task isn't currently scheduled, will schedule it

## fifo details
 - Usage: `?fifo details <task_name> `

Provide all the details on the specified task name

## fifo list
 - Usage: `?fifo list [all_servers=False] `

Lists all current tasks and their triggers.<br/><br/>Do `?fifo list True` to see tasks from all servers

## fifo delete
 - Usage: `?fifo delete <task_name> `

Deletes a task from this server's task list

## fifo cleartriggers
 - Usage: `?fifo cleartriggers <task_name> `
 - Aliases: `cleartrigger`

Removes all triggers from specified task<br/><br/>Useful to start over with new trigger

## fifo checktask
 - Usage: `?fifo checktask <task_name> `
 - Aliases: `checkjob and check`

Returns the next 10 scheduled executions of the task

## fifo add
 - Usage: `?fifo add <task_name> <command_to_execute> `

Add a new task to this server's task list

## fifo printschedule
 - Usage: `?fifo printschedule `

Print the current schedule of execution.<br/><br/>Useful for debugging.

## fifo pause
 - Usage: `?fifo pause [task_name=None] `

Provide a task name to pause execution of a task<br/><br/>Otherwise pauses execution of all tasks on all servers

