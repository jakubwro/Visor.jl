# Change Log

## 0.2.0 (3 December, 2023)

- Renamed functions:
  - is_shutdown=>isshutdown
  - is_request=>isrequest
  - if_restart=>ifrestart

- Add `handler` keyword arg to supervise. `handler` value is a callback function for handling process lifecycles events. Currently manages events are task exceptions and `ProcessFatal`.
  
- Removed `supervisor_shutdown` in case of a `ProcessFatal` exception. This implies that the other processes continue to run despite the process that thrown `ProcessFatal` will never restart.

- Log a warn message when starting a process task throws a MethodError exception.

- New function `isprocstarted`: check if process task is running.
  
- @isshutdown macro.

## 0.1.0 (November 13, 2023)

- Initial release.