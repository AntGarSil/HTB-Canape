Write up for HackTheBox Canape challenge
----

1) Can git clone from the web server
2) Get source code.  Can see its vulnerable to RCE via python pickle deserialization
3) RCE is in exploit.py
4) Backup 'passwords' couchdb database using https://github.com/danielebailo/couchdb-dump.  Couchdb databases can be enumerated by going to http://localhost:5984/_all_dbs
5) Credentials in plaintext in the DB  - ssh -p 65535 homer@10.10.10.70
6) Sudoers allows us to run /usr/bin/pip install *
7) Read privileged file contents with below:
 sudo /usr/bin/pip install -r /root/root.txt
