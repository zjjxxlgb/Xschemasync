# 增强schemasync，
1、支持中文注释，2、支持过滤表，3、支持过滤特定DDL

yum install python-devel -y
pip install mysql-python pymysql schemaobject schemasync


替换lib64/python2.7/site-packages/schemasync里的文件


[root@GZ sql]# schemasync --help
Usage: 
                schemasync [options] <source> <target>
                source/target format: mysql://user:pass@host:port/database

                        A MySQL Schema Synchronization Utility

Options:
  -h, --help            show this help message and exit
  -V, --version         show version and exit.
  -r, --revision        increment the migration script version number if a
                        file with the same name already exists.
  -a, --sync-auto-inc   sync the AUTO_INCREMENT value for each table.
  -c, --sync-comments   sync the COMMENT field for all tables AND columns
  -D, --no-date         removes the date from the file format
  --charset=CHARSET     set the connection charset, default: utf8
  --tag=TAG             tag the migration scripts as <database>_<tag>. Valid
                        characters include [A-Za-z0-9-_]
  --output-directory=OUTPUT_DIRECTORY
                        directory to write the migration scrips. The default
                        is current working directory. Must use absolute path
                        if provided.
  --log-directory=LOG_DIRECTORY
                        set the directory to write the log to. Must use
                        absolute path if provided. Default is output
                        directory. Log filename is schemasync.log
   --table=TABLE         sync the special table
   --mode=MODE           default 0:all schema change;1:ignore drop
                        table;2:ignore drop column;3:ignore drop table and
                        column;100:only drop table and column
  
  
