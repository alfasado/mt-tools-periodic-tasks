# About mt-tools-periodic-tasks for Movable Type

## MT::Tool::RunTasks

Do run_tasks but do not work_periodically.
You can run_tasks specify the tasks ID(optional).

### Example

Execute from the command line.

    cd /path/to/mt
    perl ./tools/run-tasks --task FuturePost,CleanTemporaryFiles

### Example - Executing from Cron

Execute run FuturePost once a day(at 2:00 am).

    0 2 * * * cd /path/to/mt; perl ./tools/run-tasks --task FuturePost

## MT::Tool::RunWorkers

Do work_periodically but do not run_tasks.

### Example

    cd /path/to/mt
    perl ./tools/run-workers

### Example - Executing from Cron

Execute run workers every hour.

    0 * * * * cd /path/to/mt; perl ./tools/run-workers

### Example - Run in daemon mode

Run workers in daemon mode.

    cd /path/to/mt
    perl ./tools/run-workers --daemon
