# 命令df

###名称
>df 显示磁盘剩余空间（display free disk space）

###用法
>df [-b | -h | -H | -k | -m | -g | -P] [-ailn] [-t] [-T type] [file | filesystem ...]


###描述 
     The df utility displays statistics about the amount of free disk space on the specified filesystem or on the filesystem of which file is a part.  Values are
     displayed in 512-byte per block counts.  If neither a file or a filesystem operand is specified, statistics for all mounted filesystems are displayed (sub-
     ject to the -t option below).

     已下是可用选项

     -a      Show all mount points, including those that were mounted with the MNT_IGNORE flag.

     -b      Use (the default) 512-byte blocks.  This is only useful as a way to override an BLOCKSIZE specification from the environment.

     -g      Use 1073741824-byte (1-Gbyte) blocks rather than the default.  Note that this overrides the BLOCKSIZE specification from the environment.

     -H      "Human-readable" output.  Use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte in order to reduce the number of digits to
             three or less using base 10 for sizes.

     -h      "Human-readable" output.  Use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte in order to reduce the number of digits to
             three or less using base 2 for sizes.

     -i      Include statistics on the number of free inodes. This option is now the default to conform to Version 3 of the Single UNIX Specification (``SUSv3'')
             Use -P to suppress this output.

     -k      Use 1024-byte (1-Kbyte) blocks, rather than the default.  Note that this overrides the BLOCKSIZE specification from the environment.

     -l      Only display information about locally-mounted filesystems.

     -m      Use 1048576-byte (1-Mbyte) blocks rather than the default.  Note that this overrides the BLOCKSIZE specification from the environment.

     -n      Print out the previously obtained statistics from the filesystems.  This option should be used if it is possible that one or more filesystems are in
             a state such that they will not be able to provide statistics without a long delay.  When this option is specified, df will not request new statis-
             tics from the filesystems, but will respond with the possibly stale statistics that were previously obtained.

     -P      Use (the default) 512-byte blocks.  This is only useful as a way to override an BLOCKSIZE specification from the environment.

     -T      Only print out statistics for filesystems of the specified types.  More than one type may be specified in a comma separated list.  The list of
             filesystem types can be prefixed with ``no'' to specify the filesystem types for which action should not be taken.  For example, the df command:

                   df -T nonfs,mfs

             lists all filesystems except those of type NFS and MFS.  The lsvfs(1) command can be used to find out the types of filesystems that are available on
             the system.

     -t      If used with no arguments, this option is a no-op (Mac OS X alread
