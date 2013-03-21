scala_akka
==========

Sample scala + akka application using sbt


Out of Memory Error
===================

If you see a permGen memory error:

    [error] java.util.concurrent.ExecutionException: java.lang.OutOfMemoryError: PermGen space
    [error] Use 'last' for the full log.
    
You will need to up the memory in the jvm perm gen space:

    export SBT_OPTS="-XX:+CMSClassUnloadingEnabled -XX:PermSize=256M -XX:MaxPermSize=512M"
