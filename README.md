# 增强schemasync
1、支持中文注释，2、支持过滤表，3、支持过滤特定DDL  <Br/>
  <Br/>
yum install python-devel -y  <Br/>
pip install mysql-python pymysql schemaobject schemasync  <Br/>

  <Br/>
替换lib64/python2.7/site-packages/schemasync里的文件  <Br/>


[root@GZ sql]# schemasync --help  <Br/>
Usage:   <Br/>
                schemasync [options] <source> <target>  <Br/>
                source/target format: mysql://user:pass@host:port/database  <Br/>
  <Br/>
                        A MySQL Schema Synchronization Utility  <Br/>

Options:  <Br/>
  -h, --help            show this help message and exit  <Br/>
  -V, --version         show version and exit.  <Br/>
  -r, --revision        increment the migration script version number if a  <Br/>
                        file with the same name already exists.  <Br/>
  -a, --sync-auto-inc   sync the AUTO_INCREMENT value for each table.  <Br/>
  -c, --sync-comments   sync the COMMENT field for all tables AND columns  <Br/>
  -D, --no-date         removes the date from the file format  <Br/>
  --charset=CHARSET     set the connection charset, default: utf8  <Br/>
  --tag=TAG             tag the migration scripts as <database>_<tag>. Valid  <Br/>
                        characters include [A-Za-z0-9-_]  <Br/>
  --output-directory=OUTPUT_DIRECTORY  <Br/>
                        directory to write the migration scrips. The default  <Br/>
                        is current working directory. Must use absolute path  <Br/>
                        if provided.  <Br/>
  --log-directory=LOG_DIRECTORY  <Br/>
                        set the directory to write the log to. Must use  <Br/>
                        absolute path if provided. Default is output  <Br/>
                        directory. Log filename is schemasync.log  <Br/>
   --table=TABLE         sync the special table  <Br/>
   --mode=MODE           default 0:all schema change;1:ignore drop  <Br/>
                        table;2:ignore drop column;3:ignore drop table and  <Br/>
                        column;100:only drop table and column  <Br/>
    <Br/>
    mode为3时过滤drop table 和drop column  <Br/>
   mode为100时只产生drop table 和drop column  <Br/>
  ![Image text](https://github.com/zjjxxlgb/Xschemasync/blob/master/sycsql2.png)  <Br/>
