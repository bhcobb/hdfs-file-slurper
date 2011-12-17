1.  Move command line arguments to properties file
2.  Look into a way to stop Hadoop aborting file copy mid-stream when JVM shutdown is signalled (since we want to wait until
existing transfers are complete before allowing VM shutdown to complete).  See `org.apache.hadoop.fs.FileSystem.ClientFinalizer`.
3.  Look at using Java 7's WatchService to notify us for inbound file creation as an optimiztion for when the source file system is local
4.  Stream data to a script rather than execute it for each file being transfered