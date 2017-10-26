# Java logging and log levels

When considering logging and log levels, use this guidelines from JCL:
* error - Other runtime errors or unexpected conditions. Expect these to be immediately visible on a status console
* warn - Use of deprecated APIs, poor use of API, 'almost' errors, other runtime situations that are undesirable or unexpected, but not necessarily "wrong". Expect these to be immediately visible on a status console
* info - Interesting runtime events (startup/shutdown). Expect these to be immediately visible on a console, so be conservative and keep to a minimum
* debug - detailed information on the flow through the system. Expect these to be written to logs only
* trace - more detailed information. Expect these to be written to logs only
