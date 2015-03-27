(*) logback.xml-configuration.patch
Basic logback configuration to write the log to a file. After applying this,
you'll probably want to adjust the paths that are debugged and the file name.

(*) serviceengine_host.patch
Patches ServiceEngine.java to use "localhost" as the hostname, without doing
a lookup (or the reverse DNS resolution, which fails if you don't have the
right network setup).
